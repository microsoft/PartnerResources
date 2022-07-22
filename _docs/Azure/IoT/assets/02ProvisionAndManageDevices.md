---
layout: page
title: 02 Provision and Manage Devices
permalink: /azure/iot/assets/02ProvisionAndManageDevices
tags: 
 - azure
 - iot
---

# AZ-220 Provision and manage devices (15-20%)

* [AZ-220: Microsoft Azure IoT Developer Exam](https://docs.microsoft.com/en-us/learn/certifications/exams/az-220)
* [Microsoft Certified: Azure IoT Developer Specialty](https://docs.microsoft.com/en-us/learn/certifications/azure-iot-developer-specialty)

The Microsoft Global Partner Solutions (GPS) Technical Team, IoT Product Group, IoT Advocates, and Microsoft Worldwide Learning have collaborated to create this guide to help you prepare for the Microsoft Azure IoT Developer exam!

## Skills Measured: Provision and Manage Devices

### [Set up the device provisioning service](https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps?wt.mc_id=eventspg_16482_webpage_reactor) 
* [Create a device provisioning service](https://docs.microsoft.com/en-us/azure/iot-dps/quick-setup-auto-provision?wt.mc_id=eventspg_16482_webpage_reactor)
* [Create a new enrollment in the device provisioning service](https://docs.microsoft.com/en-us/azure/iot-dps/how-to-manage-enrollments?wt.mc_id=eventspg_16482_webpage_reactor)
* [Link an IoT hub to the device provisioning service](https://docs.microsoft.com/en-us/azure/iot-dps/quick-setup-auto-provision#link-the-iot-hub-and-your-device-provisioning-service?wt.mc_id=eventspg_16482_webpage_reactor)

### [Manage the device lifecycle](https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-device-management-overview?wt.mc_id=eventspg_16482_webpage_reactor) 
* [Provision a device by using the device provisioning service](https://docs.microsoft.com/en-us/azure/iot-dps/how-to-manage-enrollments?wt.mc_id=eventspg_16482_webpage_reactor)
* [Deprovision an auto-enrollment](https://docs.microsoft.com/en-us/azure/iot-dps/how-to-unprovision-devices?wt.mc_id=eventspg_16482_webpage_reactor)
* [Decommission (disenroll) a device](https://docs.microsoft.com/en-us/azure/iot-dps/how-to-revoke-device-access-portal?wt.mc_id=eventspg_16482_webpage_reactor)

### [Manage IoT devices by using IoT Hub](https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-device-management-overview?wt.mc_id=eventspg_16482_webpage_reactor)
* [Manage devices list in the IoT Hub device registry](https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-identity-registry?wt.mc_id=eventspg_16482_webpage_reactor)
* [Modify device twin tags and properties](https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-device-twins?wt.mc_id=eventspg_16482_webpage_reactor)
* [Specify a set of devices to manage by using IoT Hub Automatic Device Management](https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-automatic-device-management?wt.mc_id=eventspg_16482_webpage_reactor)
* [Implement and manage configuration on a set of devices by using IoT Hub Automatic Device Management](https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-automatic-device-management?wt.mc_id=eventspg_16482_webpage_reactor)
* [Control access to device functionality by using module identities and module twins](https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twins?wt.mc_id=eventspg_16482_webpage_reactor)

### [Manage IoT devices by using Azure IoT Central](https://docs.microsoft.com/en-us/azure/iot-central/core/overview-iot-central-operator?wt.mc_id=eventspg_16482_webpage_reactor) 
* [Create and manage device templates by using Azure IoT Central and Digital Twins Definition Language (DTDL)](https://docs.microsoft.com/en-us/azure/iot-central/core/howto-set-up-template?wt.mc_id=eventspg_16482_webpage_reactor)
* [Configure rules, actions, and commands in Azure IoT Central](https://docs.microsoft.com/en-us/azure/iot-central/core/howto-configure-rules?wt.mc_id=eventspg_16482_webpage_reactor)
* [Add, enroll, and manage devices by using Azure IoT Central](https://docs.microsoft.com/en-us/azure/iot-central/core/howto-manage-devices?wt.mc_id=eventspg_16482_webpage_reactor)
* [Manage Azure IoT Central applications, including security, tenants, customization, and visualizations](https://docs.microsoft.com/en-us/azure/iot-central/core/overview-iot-central-admin?wt.mc_id=eventspg_16482_webpage_reactor)
* [Manage data integration, including data ingress, data export, and data transformation](https://docs.microsoft.com/en-us/azure/iot-central/core/howto-map-data?wt.mc_id=eventspg_16482_webpage_reactor)
* [Configure and manage Azure IoT Central jobs](https://docs.microsoft.com/en-us/azure/iot-central/core/howto-manage-devices-in-bulk?wt.mc_id=eventspg_16482_webpage_reactor)
* [Manage Azure IoT Central by using APIs](https://docs.microsoft.com/en-us/azure/iot-central/core/overview-iot-central-api-tour?wt.mc_id=eventspg_16482_webpage_reactor)

*NOTE: In most cases, exams do NOT cover preview features, and some features will only be added to an exam when they are GA (General Availability).*

## Quick Reference: Key Concepts and Terminology
* Device Provisioning Service (DPS) Features: 
  * **Secure attestation support** for X.509 and TPM-based identities
  * A configurable, updatable **enrollment list** containing the complete record of devices/groups of devices that may at some point register
  * **Multiple allocation policies** to control how DPS assigns devices to IoT hubs in support of your scenarios: Lowest latency, evenly weighted distribution (default), and static configuration via the enrollment list
  * **Monitoring and diagnostics logging** to make sure everything is working properly
  * **Multi-hub support** allows DPS to assign devices to more than one IoT hub (including across subscriptions and regions), assigned by multiple allocation policies
  * **Cross-region support** allows DPS to assign devices to IoT hubs in other regions
  * **Encryption for data at rest** allows data in DPS to be encrypted and decrypted transparently using 256-bit AES encryption
  * **Cross-platform support**
  <br />- A variety of operating systems
  <br />- SDKs across multiple languages
  <br />- HTTPS, AMQP, and MQTT protocol support (Service SDK is HTTPS only)
* *Service Operations Endpoint* – Used for managing DPS and the enrollment list
* *Device Provisioning Endpoint* – Single address used for all provisioning, shared across all customers and DPS instances
* *Linked IoT Hubs* – Target Azure IoT Hub instances for the DPS
* *Allocation Policy* – As previously mentioned, the mapping of device to target Azure IoT Hub
* *Enrollment* – The record of a device or group of devices that may register against the DPS
* *Registration* – The record of a successful registration/provisioning of a device
* *Operations* – The billing unit for DPS; one successfully completed request
* *ID Scope* – Differentiates various DPS instances and tenants at the fixed, shared target endpoints
* *Registration ID* – Uniquely identifies a device in the DPS instance
* *Device ID* – Uniquely identifies a device in the associated IoT Hub instance
* *Attestation mechanism* – the way a device proves its identity to the DPS
  * *X.509 Certificates* – Digital identity based on private/public key pairs and a chain of trust; issued by a certificate authority (CA)
  <br />Certificate rules:
  <br />- Chain must be trusted
  <br />- Group or individual enrollment
  <br />- Individual overrides group
  * TPM nonce challenge
  <br />*Trusted Platform Module (TPM)* – a specification for storing keys or the interface for communicating with an HSM acting as a TPM; two hardware keys for the TPM:
  <br />- *Endorsement key (EK)* – unique identifier for the TPM; read-only, injected by the manufacturer
  <br />- *Storage root key (SRK)* – protects the TPM secrets; generated when a user takes ownership of the TPM
  * Symmetric key
* *Hardware security module (HSM)* – used for secure, hardware-based storage of device secrets
* *Individual Enrollments* - An Individual enrollment is an entry for a single device that may register. Individual enrollments may use either X.509 certificates or SAS tokens (from a physical or virtual TPM) as attestation mechanisms. 
* *Group Enrollments* - An Enrollment group is an entry for a group of devices that share a common attestation mechanism of X.509 certificates, signed by the same signing certificate, which can be the root certificate or the intermediate certificate, used to produce device certificate on physical device.

## Microsoft Learn - Related Learning Paths

### [Provision IoT devices at scale by using the Device Provisioning Service](https://docs.microsoft.com/en-us/learn/paths/provision-iot-devices-scale-use-device/?wt.mc_id=eventspg_16482_webpage_reactor) (5 Modules)
Learn about the Device Provisioning Service properties and capabilities, device attestation mechanisms, device provisioning lifecycle tasks, and you will implement device enrollment (and disenrollment) using individual and group enrollment processes.

### [Manage IoT devices by using IoT Hub and apps](https://docs.microsoft.com/en-us/learn/paths/use-iot-hub-apps-manage-iot-devices/?wt.mc_id=eventspg_16482_webpage_reactor) (5 Modules)
Learn about device management patterns and the capabilities for device management, including bulk device management, that can be implemented using features of IoT Hub and by developing code.

### [Build low touch IoT solutions by using Azure IoT Central](https://docs.microsoft.com/en-us/learn/paths/build-low-touch-iot-solutions-by-using-azure-iot-central/?wt.mc_id=eventspg_16482_webpage_reactor) (4 Modules)
Learn about the Azure IoT Central application platform and the support that it provides to companies with limited budgets and technical resources who are interested in developing, managing, and maintaining IoT solutions.

## Other Helpful Resources

* [Azure IoT Blogs](https://azure.microsoft.com/en-us/blog/topics/internet-of-things/?wt.mc_id=eventspg_16482_webpage_reactor)
* [Azure IoT Hub Pricing](https://azure.microsoft.com/en-us/pricing/details/iot-hub/?wt.mc_id=eventspg_16482_webpage_reactor)
* [Azure IoT Reference Architecture](https://docs.microsoft.com/en-us/azure/architecture/reference-architectures/iot?wt.mc_id=eventspg_16482_webpage_reactor)
* [Best practices for device configuration within an IoT solution](https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-configuration-best-practices)
* [Export IoT data to Azure Data Explorer](https://docs.microsoft.com/en-us/azure/iot-central/core/howto-export-to-azure-data-explorer?wt.mc_id=eventspg_16482_webpage_reactor)
* [How to deprovision devices that were previously auto-provisioned](https://docs.microsoft.com/en-us/azure/iot-dps/how-to-unprovision-devices?wt.mc_id=eventspg_16482_webpage_reactor)
* [How to disenroll a device from Azure IoT Hub Device Provisioning Service](https://docs.microsoft.com/en-us/azure/iot-dps/how-to-revoke-device-access-portal)
* [How to provision a single simulated device](https://docs.microsoft.com/en-us/azure/iot-dps/quick-create-simulated-device-symm-key?wt.mc_id=eventspg_16482_webpage_reactor)
* [How to provision for multitenancy](https://docs.microsoft.com/en-us/azure/iot-dps/how-to-provision-multitenant?wt.mc_id=eventspg_16482_webpage_reactor)
* [How to provision legacy devices using Symmetric key attestation](https://docs.microsoft.com/en-us/azure/iot-dps/how-to-legacy-device-symm-key?wt.mc_id=eventspg_16482_webpage_reactor)
* [How to reprovision devices](https://docs.microsoft.com/en-us/azure/iot-dps/how-to-reprovision?wt.mc_id=eventspg_16482_webpage_reactor)
* [How to roll X.509 device certificates](https://docs.microsoft.com/en-us/azure/iot-dps/how-to-roll-certificates?wt.mc_id=eventspg_16482_webpage_reactor)
* [Import and export IoT Hub device identities in bulk](https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-bulk-identity-mgmt?wt.mc_id=eventspg_16482_webpage_reactor)
* [Invoke a direct method on a device](https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-direct-methods?wt.mc_id=eventspg_16482_webpage_reactor)
* [IoT Hub Device Provisioning Service concepts](https://docs.microsoft.com/en-us/azure/iot-dps/concepts-service?wt.mc_id=eventspg_16482_webpage_reactor)
* [Microsoft Tech Community - IoT](https://techcommunity.microsoft.com/t5/internet-of-things-iot/ct-p/IoT?wt.mc_id=eventspg_16482_webpage_reactor) - Blogs and conversation spaces
* [Schedule jobs on multiple devices](https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-jobs?wt.mc_id=eventspg_16482_webpage_reactor)
* [Transform data externally for IoT Central](https://docs.microsoft.com/en-us/azure/iot-central/core/howto-transform-data?wt.mc_id=eventspg_16482_webpage_reactor)
* [YouTube - Microsoft IoT Developers](https://www.youtube.com/channel/UCL7wy-iy_V76xxPnrIzGOZQ?wt.mc_id=eventspg_16482_webpage_reactor)

Happy studies!
