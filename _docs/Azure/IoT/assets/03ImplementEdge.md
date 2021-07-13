# AZ-220 Implement Edge (15-20%)

* [AZ-220: Microsoft Azure IoT Developer Exam](https://docs.microsoft.com/en-us/learn/certifications/exams/az-220)
* [Microsoft Certified: Azure IoT Developer Specialty](https://docs.microsoft.com/en-us/learn/certifications/azure-iot-developer-specialty)
* [Microsoft Tech Community "Learn IoT" Conversation Space](https://aka.ms/iottechcommunity/learniot) - Where you can discuss IoT learning resources and homework questions 

## Skills Measured:
### Set up and deploy an IoT Edge device
* Create a device identity in IoT Hub
* Deploy a single IoT device to IoT Edge
* Create a deployment for IoT Edge devices
* Install container runtime on IoT devices
* Define and implement deployment manifest
* Update security daemon and runtime
* Provision IoT Edge devices with DPS
* IoT Edge automatic deployments
* Deploy on constrained devices
* Secure IoT Edge solutions
* Deploy production certificates

### Develop modules
* Create and configure an Edge module
* Deploy a module to an Edge device
* Publish an IoT Edge module to an Azure Container Registry

### Configure an IoT Edge device
* Select and deploy an appropriate gateway pattern
* Implement Industrial IoT solutions with modules like Modbus and OPC
* Implement module-to-module communication
* Implement and configure offline support (including local storage)

## Homework:
### [AZ-220 IoT Labs](https://microsoftlearning.github.io/AZ-220-Microsoft-Azure-IoT-Developer) 
* Module 6: Azure IoT Edge Deployment Process
  * [Lab 11: Introduction to Azure IoT Edge](https://microsoftlearning.github.io/AZ-220-Microsoft-Azure-IoT-Developer/Instructions/Labs/LAB_AK_11-introduction-to-azure-iot-edge.html) 
  <br />Exercise 1: Verify Lab Prerequisites
  <br />Exercise 2: Deploy Azure IoT Edge enabled Linux VM
  <br />Exercise 3: Create IoT Edge Device Identity in IoT Hub using Azure CLI
  <br />Exercise 4: Connect IoT Edge Device to IoT Hub
  <br />Exercise 5: Add Edge Module to Edge Device
  <br />Exercise 6: Deploy Azure Stream Analytics as IoT Edge Module

  * [Lab 12: Setup an IoT Edge Gateway](https://microsoftlearning.github.io/AZ-220-Microsoft-Azure-IoT-Developer/Instructions/Labs/LAB_AK_12-setup-an-iot-edge-gateway.html)
  <br />Exercise 1: Exercise 1: Verify Lab Prerequisites
  <br />Exercise 2: Deploy Azure IoT Edge enabled Linux VM
  <br />Exercise 3: Generate and Configure IoT Edge Device CA Certificates
  <br />Exercise 4: Create IoT Edge Device Identity in IoT Hub using Azure Portal
  <br />Exercise 5: Setup IoT Edge Gateway Hostname
  <br />Exercise 6: Connect IoT Edge Gateway Device to IoT Hub
  <br />Exercise 7: Open IoT Edge Gateway Device Ports for Communication
  <br />Exercise 8: Create Downstream Device Identity in IoT Hub
  <br />Exercise 9: Connect Downstream Device to IoT Edge Gateway
  <br />Exercise 10: Verify Event Flow

* Module 7: Azure IoT Edge Modules
  * [Lab 13: Develop, Deploy and debug a custom module on Azure IoT Edge with VS Code](https://microsoftlearning.github.io/AZ-220-Microsoft-Azure-IoT-Developer/Instructions/Labs/LAB_AK_13-deploy-and-debug-custom-azure-iot-edge-module.html)
  <br />Exercise 1: Verify Lab Prerequisites
  <br />Exercise 2: Install Azure IoT EdgeHub Dev Tool
  <br />Exercise 3: Create Azure Container Registry
  <br />Exercise 4: Create Custom Edge Module in C#
  <br />Exercise 5: Debug in Attach Mode with IoT Edge Simulator
  <br />Exercise 6: Deploy IoT Edge Solution

  * [Lab 14: Run an IoT Edge device in restricted network and offline](https://microsoftlearning.github.io/AZ-220-Microsoft-Azure-IoT-Developer/Instructions/Labs/LAB_AK_14-iot-edge-device-in-restricted-network.html)
  <br />Exercise 1: Verify Lab Prerequisites
  <br />Exercise 2: Deploy Azure IoT Edge enabled Linux VM
  <br />Exercise 3: Setup IoT Edge Parent with Child IoT Devices
  <br />Exercise 4: Configure IoT Edge Device as Gateway
  <br />Exercise 5: Open IoT Edge Gateway Device Inbound Ports using Azure CLI
  <br />Exercise 6: Configure IoT Edge Device Time-to-Live and Message Storage
  <br />Exercise 7: Connect Child IoT Device to IoT Edge Gateway
  <br />Exercise 8: Test Device Connectivity and Offline Support

### Sign up for [Online Workshop Series: Build End-to-End IoT Solutions](https://aka.ms/IoT-online-workshop)
* Work with Azure IoT Edge - May 14th

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


## Resources
* [IoT Edge Documentation](https://docs.microsoft.com/en-us/azure/iot-edge/)
* [IoT Technical Community](https://techcommunity.microsoft.com/t5/internet-of-things-iot/ct-p/IoT)
* [Microsoft Learn IoT Learning Paths](http://aka.ms/mslearniot)
* [Azure IoT Reference Architecture Guide](https://docs.Microsoft.com/azure/architecture/reference-architectures/iot)
* [Quickstart: Deploy your first IoT Edge module to a virtual Windows device](https://docs.microsoft.com/en-us/azure/iot-edge/quickstart)
* [IoT Edge Runtime](https://docs.microsoft.com/en-us/azure/iot-edge/iot-edge-runtime)
* [Install Azure IoT Edge on Windows](https://docs.microsoft.com/en-us/azure/iot-edge/how-to-install-iot-edge-windows)
* [Install the Azure IoT Edge runtime on Linux](https://docs.microsoft.com/en-us/azure/iot-edge/how-to-install-iot-edge-linux)
* [IoT Edge security daemon](https://docs.microsoft.com/en-us/azure/iot-edge/iot-edge-security-manager)
* [Understand Azure IoT Edge modules](https://docs.microsoft.com/en-us/azure/iot-edge/iot-edge-modules)
* [Develop your own IoT Edge modules](https://docs.microsoft.com/en-us/azure/iot-edge/module-development)
* [Learn how to deploy modules and establish routes in IoT Edge](https://docs.microsoft.com/en-us/azure/iot-edge/module-composition)
* [Deploy Azure IoT Edge modules from the Azure portal](https://docs.microsoft.com/en-us/azure/iot-edge/how-to-deploy-modules-portal) (Deployment manifest wizard)
* [Understand IoT Edge automatic deployments for single devices or at scale](https://docs.microsoft.com/en-us/azure/iot-edge/module-deployment-monitoring)
* [Deploy IoT Edge modules at scale using the Azure portal](https://docs.microsoft.com/en-us/azure/iot-edge/how-to-deploy-at-scale)
* [Monitor IoT Edge deployments](https://docs.microsoft.com/en-us/azure/iot-edge/how-to-monitor-iot-edge-deployments)
* Monitor a Deployment with Azure CLI
  * [az IoT Edge deployment show](https://docs.microsoft.com/cli/azure/ext/azure-cli-iot-ext/iot/edge/deployment?view=azure-cli-latest#ext-azure-cli-iot-ext-az-iot-edge-deployment-show) command
  * [az IoT Edge deployment show-metric](https://docs.microsoft.com/cli/azure/ext/azure-cli-iot-ext/iot/edge/deployment?view=azure-cli-latest#ext-azure-cli-iot-ext-az-iot-edge-deployment-show-metric) command
* [Register an Azure IoT Edge device](https://docs.microsoft.com/en-us/azure/iot-edge/how-to-register-device)
* [Install the Azure IoT Edge runtime on Debian-based Linux systems](https://docs.microsoft.com/en-us/azure/iot-edge/how-to-install-iot-edge-linux)
* [Understand extended offline capabilities for IoT Edge devices, modules, and child devices](https://docs.microsoft.com/en-us/azure/iot-edge/offline-capabilities)
* [How an IoT Edge device can be used as a gateway](https://docs.microsoft.com/en-us/azure/iot-edge/iot-edge-as-gateway)
* [Update the IoT Edge security daemon and runtime](https://github.com/MicrosoftDocs/azure-docs/blob/master/articles/iot-edge/how-to-update-iot-edge.md)

NOTE: In most cases, exams do NOT cover preview features, and some features will only be
added to an exam when they are GA (General Availability).
