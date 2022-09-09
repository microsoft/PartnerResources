---
nav_exclude: true
layout: page
title: Creating Custom Health Probes with Azure Container Apps
description: This series will give you a comprehensive introduction Azure Container Apps.
permalink: /skilling/Azure Container Apps/3-terraform
updated: 2022-08-22
showbreadcrumb: false
tags:
 - workshop1
 - appdev1
 - modernize1
---

# Hands-On: Creating Custom Health Probes with Azure Container Apps

Health probes in Azure Container Apps are based on [Kubernetes Health Probes](https://kubernetes.io/docs/tasks/configure-pod-container/configure-liveness-readiness-startup-probes/). You can set up probes using either TCP or HTTP(S) exclusively.

Container Apps support the following probes:

*   **Liveness**: Reports the overall health of your replica.
*   **Readiness**: Signals that a replica is ready to accept traffic.
*   **Startup**: Delay reporting on a liveness or readiness state for slower apps with a startup probe.

For a full listing of the specification supported in Azure Container Apps, refer to [Azure REST API specs](https://github.com/Azure/azure-rest-api-specs/blob/main/specification/app/resource-manager/Microsoft.App/stable/2022-03-01/CommonDefinitions.json#L119-L236).

## HTTP probes

HTTP probes allow you to implement custom logic to check the status of application dependencies before reporting a healthy status. Configure your health probe endpoints to respond with an HTTP status code greater than or equal to `200` and less than `400` to indicate success. Any other response code outside this range indicates a failure.

The following example demonstrates how to implement a liveness endpoint in JavaScript.

```
const express = require('express');
const app = express();

app.get('/liveness', (req, res) => {
  let isSystemStable = false;

  // check for database availability
  // check filesystem structure
  //  etc.

  // set isSystemStable to true if all checks pass

  if (isSystemStable) {
    res.status(200); // Success
  } else {
    res.status(503); // Service unavailable
  }
})
```

## Deploying Health Probes

The following code listing shows how you can define health probes for your containers.

The `...` placeholders denote omitted code. Refer to [Container Apps ARM template API specification](https://docs.microsoft.com/en-us/azure/container-apps/azure-resource-manager-api-spec) for full ARM template details.

Both deployments below will deploy a simple NGINX image with liveness probes,

### ARM Template Deployment

```
{
  ...
  "containers":[
    {
      "image":"nginx",
      "name":"web",
      "probes": [
        {
          "type": "liveness",
          "httpGet": {
            "path": "/health",
            "port": 8080,
            "httpHeaders": [
              {
                "name": "Custom-Header",
                "value": "liveness probe"
              }]
          },
          "initialDelaySeconds": 7,
          "periodSeconds": 3
        },
        {
          "type": "readiness",
          "tcpSocket": {
            "port": 8081
          },
          "initialDelaySeconds": 10,
          "periodSeconds": 3
        },
        {
          "type": "startup",
          "httpGet": {
            "path": "/startup",
            "port": 8080,
            "httpHeaders": [
              {
                "name": "Custom-Header",
                "value": "startup probe"
              }]
          },
          "initialDelaySeconds": 3,
          "periodSeconds": 3
        }]
    }]
  ...
}
```

### YAML Deployment Template

```
...
containers:
  - image: nginx
    name: web
    probes:
      - type: liveness
        httpGet:
          path: "/health"
          port: 8080
          httpHeaders:
            - name: Custom-Header
              value: "liveness probe"
        initialDelaySeconds: 7
        periodSeconds: 3
      - type: readiness
        tcpSocket:
          port: 8081
        initialDelaySeconds: 10
        periodSeconds: 3
      - type: startup
        httpGet:
          path: "/startup"
          port: 8080
          httpHeaders:
            - name: Custom-Header
              value: "startup probe"
        initialDelaySeconds: 3
        periodSeconds: 3
```

The optional failureThreshold setting defines the number of attempts Container Apps tries if the probe if execution fails. Attempts that exceed the failureThreshold amount cause different results for each probe.

## Default configuration

Container Apps offers default probe settings if no probes are defined. If your app takes an extended amount of time to start, **which is very common in Java,** you often need to customize the probes so your container won't crash.

The following example demonstrates how to configure the liveness and readiness probes in order to extend the startup times.

```
"probes": [
       {
        "type": "liveness",
        "failureThreshold": 3,
        "periodSeconds": 10,
        "successThreshold": 1,
        "tcpSocket": {
          "port": 80
        },
        "timeoutSeconds": 1
       },
       {
         "type": "readiness",
         "failureThreshold": 48,
         "initialDelaySeconds": 3,
         "periodSeconds": 5,
         "successThreshold": 1,
         "tcpSocket": {
           "port": 80
          },
          "timeoutSeconds": 5
       }
```

## Next steps

Seeing more and more concepts from underlying Kubernetes becoming available in Azure Container Apps is excellent. Health-probes are mission-critical for Kubernetes to address self-healing concepts and proper traffic routing capabilities. I’m curious to see how the product team balances highly demanded features like health-probes and the - desired - simplicity of configuring apps when deploying them to Azure Container Apps. The upcoming weeks and months will show how complex real-world deployment manifests for applications in Azure Container Apps will become.

