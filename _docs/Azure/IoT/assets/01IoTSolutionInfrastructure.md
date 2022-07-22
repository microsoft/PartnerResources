---
layout: page
title: 01 IoT Solution Infrastructure
permalink: /azure/iot/assets/01IoTSolutionInfrastructure
tags: 
 - azure
 - iot
---

# Implement the IoT solution infrastructure (10 - 15%)

* [AZ-220: Microsoft Azure IoT Developer Exam](https://docs.microsoft.com/en-us/learn/certifications/exams/az-220)
* [Microsoft Certified: Azure IoT Developer Specialty](https://docs.microsoft.com/en-us/learn/certifications/azure-iot-developer-specialty)
* [Microsoft Tech Community "Learn IoT" Conversation Space](https://aka.ms/iottechcommunity/learniot) - Where you can discuss IoT learning resources and homework questions 

## Skills Measured:
### Create and configure an IoT Hub
* Create an IoT Hub
* Register a device
* Configure a device twin
* Configure IoT Hub tier and scaling

### Build device messaging and communication
* Build messaging solutions by using SDKs (device and service)
* Implement device-to-cloud communication
* Implement cloud-to-device communication
* Configure file upload for devices

### Configure physical IoT devices
* Recommend an appropriate protocol based on device specifications
* Configure device networking, topology, and connectivity

## Homework:
### [AZ-220 IoT Labs](https://microsoftlearning.github.io/AZ-220-Microsoft-Azure-IoT-Developer/Instructions/Labs/LAB_AK_01-getting-started-with-azure.html) 
* [Lab 01: Getting Started with Azure](https://microsoftlearning.github.io/AZ-220-Microsoft-Azure-IoT-Developer/Instructions/Labs/LAB_AK_01-getting-started-with-azure.html)
<br />Exercise 1: Explore the Azure Portal and Dashboard
<br />Exercise 2: Create an Azure Dashboard and Resource Group

* [Lab 02: Getting Started with Azure IoT Services](https://microsoftlearning.github.io/AZ-220-Microsoft-Azure-IoT-Developer/Instructions/Labs/LAB_AK_02-getting-started-with-azure-iot-services.html)
<br />Exercise 1: Naming Resources with Unique Names
<br />Exercise 2: Create an IoT Hub using the Azure portal
<br />Exercise 3: Examine the IoT Hub Service
<br />Exercise 4: Create a Device Provisioning Service using the Azure portal
<br />Exercise 5: Examine the Device Provisioning Service

* [Lab03: Setup the Development Environment](https://microsoftlearning.github.io/AZ-220-Microsoft-Azure-IoT-Developer/Instructions/Labs/LAB_AK_03-set-up-the-development-environment.html)
<br />Exercise 1: Install Developer Tools and Products
<br />Exercise 2: Install Dev Tool Extensions
<br />Exercise 3: Set Up Course Lab Files and Alternative Tools

* [Lab04: Connect an IoT Device to Azure](https://microsoftlearning.github.io/AZ-220-Microsoft-Azure-IoT-Developer/Instructions/Labs/LAB_AK_04-connect-iot-device-to-azure.html)
<br />Exercise 1: Verify Lab Prerequisites
<br />Exercise 2: Create Azure IoT Hub Device ID using Azure CLI
<br />Exercise 3: Configure and Test a Simulated Device (C#)

### [Online Workshop Series: Build End-to-End IoT Solutions](https://aka.ms/IoT-online-workshop) - 6-part webinar series on building solutions with Azure IoT
* Part 1: [Transform your business with IoT](https://www.youtube.com/watch?v=_BCS7gwR5yA&list=PL1ljc761XCiZMLoKOWZ8YVq_u9DacV7sy&index=1) – To better understand the basics of IoT and available training resources. Describes Azure IoT components and explains how you combine them to create value for enterprises, enabling digital feedback loops for solutions that extend beyond telemetry with analytics and edge solutions that provide real-time status.
* Part 2: [Devices and device communication](https://www.youtube.com/watch?v=ATdfz3nXzb0&list=PL1ljc761XCiZMLoKOWZ8YVq_u9DacV7sy&index=2) - Learn how to set up the development environment used throughout this series, including how to connect an IoT device with temperature and humidity sensors to Azure. After this session, follow the Hands on Labs found here: https://aka.ms/Training/LearnAzureIoT. In the labs, you’ll configure a simulated device to connect to Azure IoT Hub. Then you’ll run the simulated device to send telemetry messages and verify that device telemetry is being received.

## Resources
* [IoT Hub Documentation](https://docs.microsoft.com/en-us/azure/iot-hub/)
* [IoT Technical Community](https://techcommunity.microsoft.com/t5/internet-of-things-iot/ct-p/IoT)
* [“Building IoT Solutions with Azure” Developer Guide](https://discover.Microsoft.com/azure-iot-building-solutions-dev-guide)
* [Microsoft Learn IoT Learning Paths](http://aka.ms/mslearniot)
* [Azure IoT Reference Architecture Guide](https://docs.Microsoft.com/azure/architecture/reference-architectures/iot)
* Create an IoT Hub:
<br />- [Use Azure Portal](https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-create-through-portal)
<br />- [Use Azure IoT Tools for VS Code](https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-create-use-iot-toolkit)
<br />- [Use Azure PowerShell](https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-create-using-powershell)
<br />- [Use Azure Cloud Shell (CLI)](https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-create-using-cli)
<br />- [Use the Resource Provider REST API](https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-rm-rest)
<br />- [Use an ARM Template from Azure PowerShell](https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-rm-template-powershell)
<br />- [Use an ARM Template from .NET](https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-rm-template-powershell)
* [Comparing IoT Hub and Event Hubs](https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-compare-event-hubs)
* [Chosing the right IoT Hub Tier](https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-scaling)
* [Overview of Device Management with IoT Hub](https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-device-management-overview)
* [Sending Device Telemetry to IoT Hub](https://docs.microsoft.com/en-us/azure/iot-hub/quickstart-send-telemetry-cli)
* [Device Twins Tutorial](https://docs.microsoft.com/en-us/azure/iot-hub/tutorial-device-twins)
* [IoT Hub query language for device and module twins, jobs, and message routing](https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-query-language)
* [Device-to-cloud communication guidance](https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-d2c-guidance)
* [Cloud-to-device communications guidance](https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-c2d-guidance)
* [IoT Hub SDKs](https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-sdks)
* [Understanding IoT Message Routing](https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-messages-d2c)
* [Azure IoT Hub Pricing](https://azure.microsoft.com/en-us/pricing/details/iot-hub/)
* [Choose a Communication Protocol](https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-protocols)
* [IoT Hub Endpoints](https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-endpoints)
* [IoT Technical Case Studies](https://microsoft.github.io/techcasestudies/#technology=IoT&sortBy=featured)
* [Blog: Benefits of using the Azure IoT SDKs, and pitfalls to avoid if you don’t](https://azure.microsoft.com/en-us/blog/benefits-of-using-the-azure-iot-sdks-in-your-azure-iot-solution/)

NOTE: In most cases, exams do NOT cover preview features, and some features will only be
added to an exam when they are GA (General Availability).

_10-15% of the AZ-220 exam will measure your ability to setup the IoT solution infrastructure._

The Microsoft Global Partner Solutions (GPS) Technical Team, IoT Product Group, IoT Advocates, and Microsoft Worldwide Learning have collaborated to create this guide to help you prepare for the Microsoft Azure IoT Developer exam!

## Skills Measured: Setup the Azure IoT Hub Solution Infrastructure

### [Create and configure an IoT hub](https://docs.microsoft.com/en-us/azure/iot-hub/?wt.mc_id=eventspg_16482_webpage_reactor) 
* [Create an IoT hub](https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-create-through-portal#create-an-iot-hub?wt.mc_id=eventspg_16482_webpage_reactor)
* [Register a device](https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-create-through-portal#register-a-new-device-in-the-iot-hub?wt.mc_id=eventspg_16482_webpage_reactor)
* [Configure a device twin](https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-device-twins?wt.mc_id=eventspg_16482_webpage_reactor)
* [Configure IoT Hub tier and scaling](https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-scaling?wt.mc_id=eventspg_16482_webpage_reactor)

### [Build device messaging and communication](https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-messaging?wt.mc_id=eventspg_16482_webpage_reactor) 
* [Build messaging solutions by using SDKs (device and service)](https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-sdks?wt.mc_id=eventspg_16482_webpage_reactor)
* [Implement device-to-cloud communication](https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-d2c-guidance?wt.mc_id=eventspg_16482_webpage_reactor)
* [Implement cloud-to-device communication](https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-c2d-guidance?wt.mc_id=eventspg_16482_webpage_reactor)
* [Configure file upload for devices](https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-file-upload?wt.mc_id=eventspg_16482_webpage_reactor)
* [Optimize message size and scaling for IoT Hub](https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-quotas-throttling?wt.mc_id=eventspg_16482_webpage_reactor)
* [Connect to IoT Hub by using Transport Layer Security (TLS) server certificates](https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-tls-support?wt.mc_id=eventspg_16482_webpage_reactor)

### [Configure physical IoT devices](https://docs.microsoft.com/en-us/azure/iot-develop/concepts-overview-connection-options?wt.mc_id=eventspg_16482_webpage_reactor)
* [Recommend an appropriate protocol or gateway based on device specifications](https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-protocols?wt.mc_id=eventspg_16482_webpage_reactor)
* [Configure device networking, topology, and connectivity](https://docs.microsoft.com/en-us/azure/iot-hub/tutorial-connectivity?wt.mc_id=eventspg_16482_webpage_reactor)
* [Add IoT Plug and Play capabilities to a device in a model-driven solution](https://docs.microsoft.com/en-us/azure/iot-develop/overview-iot-plug-and-play?wt.mc_id=eventspg_16482_webpage_reactor)

*NOTE: In most cases, exams do NOT cover preview features, and some features will only be added to an exam when they are GA (General Availability).*

## Microsoft Learn - Related Learning Paths

### [Create Azure IoT services in the Azure portal](https://docs.microsoft.com/en-us/learn/paths/create-azure-iot-services-azure-portal/?wt.mc_id=eventspg_16482_webpage_reactor) (4 Modules)
Become familiar with the Azure portal to the Azure resources that are available for an IoT solution. Learners will step through the process of creating IoT Hub and Device Provisioning Service resources.

### [Implement IoT device communication by using the Azure IoT SDKs](https://docs.microsoft.com/en-us/learn/paths/implement-iot-device-communication-by-using-azure-iot-sdks/?wt.mc_id=eventspg_16482_webpage_reactor) (4 Modules)
Learn about the IoT Hub service properties and limitations, the IoT device lifecycle, Azure IoT developer tools, and then you will implement communication between an IoT device and IoT Hub.

## Other Helpful Resources

* [Azure IoT Blogs](https://azure.microsoft.com/en-us/blog/topics/internet-of-things/?wt.mc_id=eventspg_16482_webpage_reactor)
* [Azure IoT Hub Pricing](https://azure.microsoft.com/en-us/pricing/details/iot-hub/?wt.mc_id=eventspg_16482_webpage_reactor)
* [Azure IoT Reference Architecture](https://docs.microsoft.com/en-us/azure/architecture/reference-architectures/iot?wt.mc_id=eventspg_16482_webpage_reactor)
* [Choose a Communication Protocol](https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-protocols?wt.mc_id=eventspg_16482_webpage_reactor)
* [Chosing the right IoT Hub Tier](https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-scaling?wt.mc_id=eventspg_16482_webpage_reactor)
* [Comparing IoT Hub and Event Hubs](https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-compare-event-hubs?wt.mc_id=eventspg_16482_webpage_reactor)
* [IoT Hub query language for device and module twins, jobs, and message routing](https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-query-language?wt.mc_id=eventspg_16482_webpage_reactor)
* [IoT Hub Endpoints](https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-endpoints?wt.mc_id=eventspg_16482_webpage_reactor)
* [Message enrichments for device-to-cloud IoT Hub messages](https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview?wt.mc_id=eventspg_16482_webpage_reactor)
* [Microsoft Tech Community - IoT](https://techcommunity.microsoft.com/t5/internet-of-things-iot/ct-p/IoT?wt.mc_id=eventspg_16482_webpage_reactor) - Blogs and conversation spaces
* [YouTube - Microsoft IoT Developers](https://www.youtube.com/channel/UCL7wy-iy_V76xxPnrIzGOZQ?wt.mc_id=eventspg_16482_webpage_reactor)

Happy studies!
