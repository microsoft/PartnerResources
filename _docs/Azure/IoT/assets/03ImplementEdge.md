---
layout: page
title: 03 Implement Edge
permalink: /azure/iot/assets/03ImplementEdge
tags: 
 - azure
 - iot
---

# AZ-220 Implement Edge (15-20%)

* [AZ-220: Microsoft Azure IoT Developer Exam](https://docs.microsoft.com/en-us/learn/certifications/exams/az-220)
* [Microsoft Certified: Azure IoT Developer Specialty](https://docs.microsoft.com/en-us/learn/certifications/azure-iot-developer-specialty)

## Skills Measured: Implement IoT Edge

### [Set up an IoT Edge device](https://docs.microsoft.com/azure/iot-edge?wt.mc_id=eventspg_16482_webpage_reactor?wt.mc_id=eventspg_16482_webpage_reactor) 
* [Create a device identity in IoT Hub](https://docs.microsoft.com/azure/iot-edge/quickstart-linux?wt.mc_id=eventspg_16482_webpage_reactor)
* [Set up an IoT device for IoT Edge](https://docs.microsoft.com/azure/iot-edge/how-to-create-iot-edge-device?wt.mc_id=eventspg_16482_webpage_reactor)
* [Install container runtime on IoT devices](https://docs.microsoft.com/azure/iot-edge/how-to-install-iot-edge?wt.mc_id=eventspg_16482_webpage_reactor)
* [Configure container startup options to interact with the host system](https://docs.microsoft.com/azure/iot-edge/how-to-access-host-storage-from-module?wt.mc_id=eventspg_16482_webpage_reactor)
* [Update IoT Edge runtime](https://docs.microsoft.com/azure/iot-edge/how-to-update-iot-edge?wt.mc_id=eventspg_16482_webpage_reactor)
* [Provision IoT Edge devices by using the device provisioning service](https://docs.microsoft.com/azure/iot-edge/how-to-auto-provision-x509-certs?wt.mc_id=eventspg_16482_webpage_reactor)

### [Deploy an IoT Edge device](https://docs.microsoft.com/azure/iot-edge/how-to-create-iot-edge-device?wt.mc_id=eventspg_16482_webpage_reactor) 
* [Create and implement a deployment manifest](https://docs.microsoft.com/azure/iot-edge/module-composition?wt.mc_id=eventspg_16482_webpage_reactor)
* [Create a deployment for a single IoT Edge device](https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring?wt.mc_id=eventspg_16482_webpage_reactor)
* [Create a deployment to target multiple devices](https://docs.microsoft.com/azure/iot-edge/how-to-deploy-at-scale?wt.mc_id=eventspg_16482_webpage_reactor)
* [Create a continuous deployment by using Azure DevOps](https://docs.microsoft.com/azure/iot-edge/how-to-continuous-integration-continuous-deployment?wt.mc_id=eventspg_16482_webpage_reactor)

### [Develop IoT Edge modules](https://docs.microsoft.com/azure/iot-edge/how-to-vs-code-develop-module?wt.mc_id=eventspg_16482_webpage_reactor) 
* [Create and customize an IoT Edge module](https://docs.microsoft.com/azure/iot-edge/how-to-vs-code-develop-module?wt.mc_id=eventspg_16482_webpage_reactor)
* [Deploy a custom IoT Edge module to an IoT Edge device](https://docs.microsoft.com/azure/iot-edge/how-to-deploy-modules-portal?wt.mc_id=eventspg_16482_webpage_reactor)
* [Publish an IoT Edge module to Azure Container Registry](https://azure.microsoft.com/services/container-registry/#documentation?wt.mc_id=eventspg_16482_webpage_reactor)
* [Define module configuration](https://docs.microsoft.com/azure/iot-edge/how-to-configure-module-build-options?wt.mc_id=eventspg_16482_webpage_reactor)
* [Configure IoT Edge module routing](https://docs.microsoft.com/azure/iot-edge/module-development?wt.mc_id=eventspg_16482_webpage_reactor)
* [Configure environment for IoT Edge development](https://docs.microsoft.com/azure/iot-edge/module-development?wt.mc_id=eventspg_16482_webpage_reactor)

### [Configure an IoT Edge device](https://docs.microsoft.com/azure/iot-edge/tutorial-machine-learning-edge-05-configure-edge-device?wt.mc_id=eventspg_16482_webpage_reactor)
* [Select an appropriate gateway pattern](https://docs.microsoft.com/azure/iot-edge/iot-edge-as-gateway?wt.mc_id=eventspg_16482_webpage_reactor)
* [Deploy an IoT gateway by using IoT Hub and IoT Edge](https://docs.microsoft.com/azure/iot-edge/how-to-connect-downstream-iot-edge-device?wt.mc_id=eventspg_16482_webpage_reactor)
* [Configure IoT Edge certificates](https://docs.microsoft.com/azure/iot-edge/how-to-manage-device-certificates?wt.mc_id=eventspg_16482_webpage_reactor)
* [Implement and configure offline support (including local storage)](https://docs.microsoft.com/azure/iot-edge/offline-capabilities?wt.mc_id=eventspg_16482_webpage_reactor)
* [Create a layered hierarchy of IoT Edge devices](https://docs.microsoft.com/azure/iot-edge/tutorial-nested-iot-edge?wt.mc_id=eventspg_16482_webpage_reactor)
* [Interact with the IoT Edge security manager](https://docs.microsoft.com/azure/iot-edge/iot-edge-security-manager?wt.mc_id=eventspg_16482_webpage_reactor)

*NOTE: In most cases, exams do NOT cover preview features, and some features will only be added to an exam when they are GA (General Availability).*

## Microsoft Learn - Related Learning Paths

### [Deploy Azure IoT Edge devices and modules](https://docs.microsoft.com/learn/paths/deploy-azure-iot-edge-devices-modules/?wt.mc_id=eventspg_16482_webpage_reactor) (5 Modules)

Learn about the benefits provided by Azure IoT Edge, the IoT Edge runtime environment, IoT Edge device deployments, and IoT Edge gateway device patterns and capabilities.

### [Develop and deploy custom IoT Edge modules](https://docs.microsoft.com/learn/paths/develop-deploy-custom-iot-edge-modules/?wt.mc_id=eventspg_16482_webpage_reactor) (4 Modules)

Learn about programming for the IoT Edge runtime environment, the tools and processes that are used to develop custom IoT Edge modules, and the support that IoT Edge provides for extended offline scenarios.

## Quick Reference: Key Concepts and Terminology
* Azure IoT Edge is made up of three components:
  * *IoT Edge Runtime* - Runs on each IoT Edge device and manages the modules deployed to each device.
  <br />System Modules
    * *IoT Edge security daemon* - Starts each time an IoT Edge device boots and bootstraps the device by starting the IoT Edge agent.
    * *IoT Edge agent* - Manages deployment and monitoring of modules on the IoT Edge device, including the IoT Edge hub. 
    * *IoT Edge hub* - Handles communications between modules on the IoT Edge device, and between the device and IoT Hub

  * *IoT Edge Modules* - Containers that run Azure services, third-party services, or your own code. Modules are deployed to IoT Edge devices and execute locally on those devices.
    * *Module image* - A package containing the software that defines a module.
    * *Module instance* - The specific unit of computation running the module image on an IoT Edge device. The module instance is started by the IoT Edge runtime.
    * *Module identity* - A piece of information (including security credentials) stored in IoT Hub, that is associated to each module instance.
    * *Module twin* - A JSON document stored in IoT Hub, that contains state information for a module instance, including metadata, configurations, and conditions. 
    * SDKs to develop custom modules in multiple languages (C#, C, Python, Java, Node.JS)
  
  * *Cloud-based Interface* - Enables you to remotely monitor and manage IoT Edge devices.
  
* Module Twin Properties of Edge Runtime Modules:
  * Desired and Reported properties
  * EdgeAgent properties
  * EdgeHub properties

## Other Helpful Resources

* [Azure IoT Blogs](https://azure.microsoft.com/blog/topics/internet-of-things/?wt.mc_id=eventspg_16482_webpage_reactor)
* [Azure IoT Edge for Linux on Windows](https://docs.microsoft.com/azure/iot-edge/iot-edge-for-linux-on-windows)
* [Azure IoT Hub Pricing](https://azure.microsoft.com/pricing/details/iot-hub/?wt.mc_id=eventspg_16482_webpage_reactor)
* [Azure IoT Edge Security](https://docs.microsoft.com/azure/iot-edge/security?wt.mc_id=eventspg_16482_webpage_reactor)
* [Azure IoT Reference Architecture](https://docs.microsoft.com/azure/architecture/reference-architectures/iot?wt.mc_id=eventspg_16482_webpage_reactor)
* [End-to-end solution using Azure Machine Learning and IoT Edge](https://docs.microsoft.com/azure/iot-edge/tutorial-machine-learning-edge-01-intro?wt.mc_id=eventspg_16482_webpage_reactor)
* [Microsoft Tech Community - IoT](https://techcommunity.microsoft.com/t5/internet-of-things-iot/ct-p/IoT?wt.mc_id=eventspg_16482_webpage_reactor) - Blogs and conversation spaces
* [Tutorial: Create a hierarchy of IoT Edge devices](https://docs.microsoft.com/azure/iot-edge/tutorial-nested-iot-edge?wt.mc_id=eventspg_16482_webpage_reactor)
* [What is Azure IoT Edge?](https://docs.microsoft.com/azure/iot-edge/about-iot-edge?wt.mc_id=eventspg_16482_webpage_reactor)
* [YouTube - Microsoft IoT Developers](https://www.youtube.com/channel/UCL7wy-iy_V76xxPnrIzGOZQ?wt.mc_id=eventspg_16482_webpage_reactor)

Happy studies!
