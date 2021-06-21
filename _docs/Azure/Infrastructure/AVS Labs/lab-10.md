---
layout: page
title: LAB10 – Connect from Azure Application Gateway to AVS hosted workload
tags: 
 - azure
 - infrastructure
 - AVS
---

# LAB10 – Connect from Azure Application Gateway to AVS hosted workload

This lab shows you the steps to use Application Gateway in front of a web server
farm to protect a web app running on Azure VMware Solution. This will allow
using Azure Application Gateway as layer 7 web traffic load balancer that lets
you manage traffic to your web applications that are hosted inside AVS Private
Cloud. You can refer to the original article: [Use Azure Application Gateway to
protect your web apps on Azure VMware Solution - Azure VMware Solution \|
Microsoft
Docs](https://docs.microsoft.com/en-us/azure/azure-vmware/protect-azure-vmware-solution-with-application-gateway)

An additional possible step is configuring Azure Traffic Manager to direct
traffic between three Azure Application Gateways spanning several Azure VMware
Solution regions. As explained in this article: [Deploy Traffic Manager to
balance Azure VMware Solution workloads - Azure VMware Solution \| Microsoft
Docs](https://docs.microsoft.com/en-us/azure/azure-vmware/deploy-traffic-manager-balance-workloads)

So, let’s start the steps of configuring a VM hosted in Azure VMware Solution
Private Cloud in the Backend Pool of Application Gateway:

1. Go to Azure Portal, search for “Application Gateways”, click on
   **Application Gateways**.  

   ![](media/lab-10/91704fd24fb6ae2769577abf1f89dd88.png)

2. Click on Add in Application gateways pane, to create a new Application
   Gateway instance in case you don’t have an existing one.  

   ![](media/lab-10/e533e7faaeac01a7db52fba6107ccf67.png)

3. Fill out the main fields at the **Basics** section to start creating a new
   Application Gateway, such as **Subscription**, **Resource Group**, **Name**,
   **Region**, **Tier**, **Virtual Network** and **Subnet**. Keep the same
   values in the other pre-populated fields.

   1. Note that the **Region** of the Application Gateway needs to be in the
      same region of the **vNet** that’s connected to AVS Private Cloud. In
      the example below it is **South Central US**.

   2. Note that in this lab the **vNet** exists and is called **AVS-vNET** and
      the **subnet** for Application Gateway has also been created and called
      **AppGateway** which should show up in the drop-down list.

      ![Graphical user interface, application Description automatically
      generated](media/lab-10/b4126c4488c7718bfce168424f5e22dd.png)

4. Move to **Frontends** section and create a new **Public** IP as you notice
   in the screenshot below. A suggested name is **AVS-AppGateway-PublicIP**.  

   ![](media/lab-10/0b986e361fc979794b8a68c156fe5836.png)

5. Move to **Backends** section. Click on **Add a backend pool** to create a
   new Backend pool, you can name it: **AVS-AppGateway-BackendPool**. Next is
   to populate the **IP**s of the web server farm VMs hosted in AVS Private
   Cloud. You can get the IPs from **vCenter** portal, or from the VMs directly
   by running **ipconfig** command in Windows or **ifconfig** command in Linux
   based operating systems.  

   The IP Address you see in the screenshot below should be the same as the IP
   of PhotoOS VM that you deployed in the earlier lab.

   ![](media/lab-10/d8b2dd2fdc6921f005161933a8a6932c.png)

6. Next, move to **Configuration** section, where you need to click **Add
   Routing rule** to map the Frontend with the Backend pool:

   ![](media/lab-10/c09b65af992bbb223dd7afb24a3934dc.png)

7. Give the rule a name, i.e.: **AVS-AppGateway-RoutingRule**.

   1. Under the **Listener** section, add a **name** for the listener, i.e.:
      **HTTP-Listener**,

   2. Select **Frontend IP**: **Public**, select the **Protocol**: **HTTP**
      (for demo purposes), specify the **Port**: **80**. Keep **Additional
      settings** as is. ![Graphical user interface, text, application, email
      Description automatically
      generated](media/lab-10/22af4c437b33f0bd8371588d177b2d01.png)

   3. Move to **Backend targets** section, select **Target type: Backend
      pool**, then select the created backend pool in the **Backend target**.
      Then create HTTP settings as in the next step.  
      ![Graphical user interface, text, application Description automatically
      generated](media/lab-10/d7c0e90d28cfaf1eed7fba57acbf8989.png)

   4. Adding **HTTP settings** by giving them a **name**, i.e.:
      **HTTP-Settings**, selecting **Backend protocol: HTTP**, and **Backend
      port: 80**. Keep other settings as is. Click **Add** button, to finish
      the HTTP settings.  

      ![](media/lab-10/9757ad2026637cd1a053e2c6d97c699e.png)

   5. After adding the Listener and the Backend targets, you should land again
      at **Add** **a Routing rule** pane. The last step at the **Add** **a
      Routing rule** pane is to click **Add** button to finish that wizard.

8. Now, move to **Review + Create** section and click on **Create** button, as
   you see in the screenshot below.

   ![](media/lab-10/6d58cdd5447d101537d07eec452cbea3.png)

9. Creating an Application Gateway takes about 15 minutes to complete.

   ![](media/lab-10/add9d657fe5efd98c1c52992109c08c4.png)

10. Go to the created Applicate Gateway by clicking on its name as shown in the
    previous step, i.e., **AVS-AppGateway**. Notice the **Frontend public IP
    address**. Copy **IP** value. **  
    **![Graphical user interface, text, application Description automatically
    generated](media/lab-10/abeea0fa5ad55e6394e833a2c0b637a9.png)

11. Open a new Internet browser (Edge/Chrome) tab and put the IP in the address
    bar with ‘**http://**’ prefix,  
    i.e.: [**http://20.188.90.231**](http://20.188.90.231)

    **Notice now that you can access the web application hosted at the web
    server farm that is hosted in AVS Private Cloud**, in this case it’s the
    default **Nginx** page.

    ![](media/lab-10/188b322eee121ec8f65ededf507140f4.png)

## Next Steps

[Back to Table of Content](toc.md#table-of-contents)

[Lab 11](lab-11.md)
