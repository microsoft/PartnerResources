# AZ-220 Provision and manage devices (20-25%)

* [AZ-220: Microsoft Azure IoT Developer Exam](https://docs.microsoft.com/en-us/learn/certifications/exams/az-220)
* [Microsoft Certified: Azure IoT Developer Specialty](https://docs.microsoft.com/en-us/learn/certifications/azure-iot-developer-specialty)
* [Microsoft Tech Community "Learn IoT" Conversation Space](https://aka.ms/iottechcommunity/learniot) - Where you can discuss IoT learning resources and homework questions 

## Skills Measured:
### Implement the Device Provisioning Service (DPS)
* Create a Device Provisioning Service
* Create a new enrollment in DPS
* Manage allocation policies by using Azure Functions
* Link an IoT Hub to the DPS

### Manage the device lifecycle
* Provision a device by using DPS
* Deprovision an autoenrollment
* Decommission (disenroll) a device

### Manage IoT devices by using IoT Hub
* Manage devices list in the IoT Hub device registry
* Modify device twin tags and properties
* Trigger an action on a set of devices by using IoT Hub Jobs and Direct Methods
* Set up Automatic Device Management of IoT devices at scale

### Build a solution by using IoT Central
* Define a device type in Azure IoT Central
* Configure rules and actions in Azure IoT Central
* Define the operator view
* Add and manage devices from IoT Central
* Monitor devices
* Custom and industry-focused application templates
* Monitor application health using metrics

## Homework:
### [AZ-220 IoT Labs](https://microsoftlearning.github.io/AZ-220-Microsoft-Azure-IoT-Developer) 
* Module 3: Device Provisioning at Scale 
  * [Lab 05: Individual Enrollment of a Device in DPS](https://microsoftlearning.github.io/AZ-220-Microsoft-Azure-IoT-Developer/Instructions/Labs/LAB_AK_05-individual-enrollment-of-device-in-dps.html)
 <br />Exercise 1: Verify Lab Prerequisites
 <br />Exercise 2: Create new individual enrollment (Symmetric keys) in DPS
 <br />Exercise 3: Configure Simulated Device
 <br />Exercise 4: Test the Simulated Device
 <br />Exercise 5: Retire the Device
 
  * [Lab 06: Automatically provision IoT devices securely and at scale with DPS](https://microsoftlearning.github.io/AZ-220-Microsoft-Azure-IoT-Developer/Instructions/Labs/LAB_AK_06-automatic-enrollment-of-devices-in-dps.html)
 <br />Exercise 1: Verify Lab Prerequisites
 <br />Exercise 2: Generate and Configure X.509 CA Certificates using OpenSSL
 <br />Exercise 3: Create Group Enrollment (X.509 Certificate) in DPS
 <br />Exercise 4: Configure simulated device with X.509 certificate
 <br />Exercise 5: Handle device twin desired property Changes
 <br />Exercise 6: Test the Simulated Device
 <br />Exercise 7: Retire Group Enrollment

* Module 8: Device Management
  * [Lab 15: Remotely monitor and control devices with Azure IoT Hub](https://microsoftlearning.github.io/AZ-220-Microsoft-Azure-IoT-Developer/Instructions/Labs/LAB_AK_15-remotely-monitor-and-control-devices.html)
 <br />Exercise 1: Verify Lab Prerequisites
 <br />Exercise 2: Write Code to Send and Receive Telemetry
 <br />Exercise 3: Create a Second App to Receive Telemetry
 <br />Exercise 4: Write Code to Invoke a Direct Method
 <br />Exercise 5: Write Code for Device Twins

  * [Lab 16: Automate IoT Device Management with Azure IoT Hub](https://microsoftlearning.github.io/AZ-220-Microsoft-Azure-IoT-Developer/Instructions/Labs/LAB_AK_16-automatic-device-management.html)
 <br />Exercise 1: Verify Lab Prerequisites
 <br />Exercise 2: Write code to simulate device that implements firmware update
 <br />Exercise 3: Test firmware update on a single device

* Module 11: Build with IoT Central
  * [Lab 20: Build with IoT Central](https://microsoftlearning.github.io/AZ-220-Microsoft-Azure-IoT-Developer/Instructions/Labs/LAB_AK_20-build-with-iot-central.html)
 <br />Exercise 1: Create and Configure Azure IoT Central
 <br />Exercise 3: Monitor a Simulated Device
 <br />Exercise 4: Create a free Azure Maps account
 <br />Exercise 5: Create a Programming Project for a Real Device
 <br />Exercise 6: Test Your IoT Central Device
 <br />Exercise 7: Create multiple devices

### Sign up for [Online Workshop Series: Build End-to-End IoT Solutions](https://aka.ms/IoT-online-workshop)
* Device provisioning at scale - April 30th

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

## Resources
* [IoT Hub Documentation](https://docs.microsoft.com/en-us/azure/iot-hub/)
* [IoT Technical Community](https://techcommunity.microsoft.com/t5/internet-of-things-iot/ct-p/IoT)
* [“Building IoT Solutions with Azure” Developer Guide](https://discover.Microsoft.com/azure-iot-building-solutions-dev-guide)
* [Microsoft Learn IoT Learning Paths](http://aka.ms/mslearniot)
* [Azure IoT Reference Architecture Guide](https://docs.Microsoft.com/azure/architecture/reference-architectures/iot)
* [What is IoT Hub Device Provisioning Service?](https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps)
* [IoT Hub Device Provisioning Service concepts](https://docs.microsoft.com/en-us/azure/iot-dps/concepts-service)
* Setup IoT Hub Device Provisioning Service
  * [With the Azure Portal](https://docs.microsoft.com/en-us/azure/iot-dps/quick-setup-auto-provision)
  * [With Azure Cloud Shell/Azure CLI](https://docs.microsoft.com/en-us/azure/iot-dps/quick-setup-auto-provision-cli)
  * [With an Azure Resource Manager template](https://docs.microsoft.com/en-us/azure/iot-dps/quick-setup-auto-provision-rm)
* [How to provision a single simulated device](https://docs.microsoft.com/en-us/azure/iot-dps/quick-create-simulated-device-symm-key)
* [How to provision legacy devices using Symmetric key attestation](https://docs.microsoft.com/en-us/azure/iot-dps/how-to-legacy-device-symm-key)
* [How to provision for multitenancy](https://docs.microsoft.com/en-us/azure/iot-dps/how-to-provision-multitenant)
* [How to deprovision devices that were previously auto-provisioned](https://docs.microsoft.com/en-us/azure/iot-dps/how-to-unprovision-devices)
* [How to disenroll a device from Azure IoT Hub Device Provisioning Service](https://docs.microsoft.com/en-us/azure/iot-dps/how-to-revoke-device-access-portal)
* [How to roll X.509 device certificates](https://docs.microsoft.com/en-us/azure/iot-dps/how-to-roll-certificates)
* [How to reprovision devices](https://docs.microsoft.com/en-us/azure/iot-dps/how-to-reprovision)
* [Custom allocation policies with Azure Functions](https://docs.microsoft.com/en-us/azure/iot-dps/how-to-use-custom-allocation-policies)
* [Azure IoT Hub Device Provisioning at Scale](https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-auto-device-config)
* [Use Azure IoT Hub Device Provisioning Service auto-provisioning to register the MXChip IoT DevKit with IoT Hub](https://docs.microsoft.com/en-us/azure/iot-dps/how-to-connect-mxchip-iot-devkit)
* [Understand and use device twins in IoT Hub](https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-device-twins)
* [Overview of Device Management with IoT Hub](https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-device-management-overview)
* [Understand the Identity Registry in your IoT Hub](https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-identity-registry)
* [Invoke a direct method on a device](https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-direct-methods)
* [Schedule jobs on multiple devices](https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-jobs)
* [Azure IoT Central](https://azure.microsoft.com/en-us/services/iot-central/)
* [Azure IoT Central SaaS Platform](https://apps.azureiotcentral.com/)

NOTE: In most cases, exams do NOT cover preview features, and some features will only be
added to an exam when they are GA (General Availability).
