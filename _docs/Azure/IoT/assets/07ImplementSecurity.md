---
layout: page
title: 07 Implement Security
permalink: /azure/iot/assets/07ImplementSecurity
tags: 
 - azure
 - iot
---

# AZ-220 Implement Security (10-15%)

* [AZ-220: Microsoft Azure IoT Developer Exam](https://docs.microsoft.com/en-us/learn/certifications/exams/az-220)
* [Microsoft Certified: Azure IoT Developer Specialty](https://docs.microsoft.com/en-us/learn/certifications/azure-iot-developer-specialty)

## Skills Measured:
### [Implement security for IoT devices and services](https://docs.microsoft.com/azure/architecture/framework/iot/iot-security?wt.mc_id=eventspg_16482_webpage_reactor)

* [Implement device and gateway security, including shared access keys, key rotation, managed identities, Hardware Security Modules (HSMs), and Trusted Platform Modules (TPMs)](https://docs.microsoft.com/azure/iot-fundamentals/iot-security-deployment?wt.mc_id=eventspg_16482_webpage_reactor)
* [Implement secure connections, including access control, authentication, shared access policies, and TLS](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-security?wt.mc_id=eventspg_16482_webpage_reactor)
* [Implement secure networking, including IP filtering and private endpoints](https://docs.microsoft.com/azure/iot-hub/virtual-network-support?wt.mc_id=eventspg_16482_webpage_reactor)

### [Implement Microsoft Defender for IoT](https://docs.microsoft.com/azure/defender-for-iot/organizations/overview?wt.mc_id=eventspg_16482_webpage_reactor) 

* [Configure a Defender for IoT agent-based solution](https://docs.microsoft.com/azure/defender-for-iot/device-builders/tutorial-configure-agent-based-solution?wt.mc_id=eventspg_16482_webpage_reactor)
* [Install and configure Defender-IoT-micro-agents (security agents)](https://docs.microsoft.com/azure/defender-for-iot/device-builders/concept-security-module?wt.mc_id=eventspg_16482_webpage_reactor)
* [Configure built-in and custom alerts for IoT Hub](https://docs.microsoft.com/azure/defender-for-iot/device-builders/concept-security-alerts?wt.mc_id=eventspg_16482_webpage_reactor)

*NOTE: In most cases, exams do NOT cover preview features, and some features will only be added to an exam when they are GA (General Availability).*

## Microsoft Learn - Related Learning Paths

### [Enhance IoT solution security by using Azure Defender for IoT](https://docs.microsoft.com/learn/paths/enhance-iot-solution-security-by-using-azure-defender/?wt.mc_id=eventspg_16482_webpage_reactor) (4 Modules)

Learn about security considerations that apply at each level of the solution and the Azure services and tools that can be configured to address security concerns from the ground up.
  
## Quick Reference: Key Concepts and Terminology
* Three widely used authentication types are X.509 certificates, Trusted Platform Modules (TPM), and symmetric keys.
  * ***X.509 certificate*** - A type of digital identity you can use for authentication. The X.509 certificate standard is documented in IETF RFC 5280. In Azure IoT, there are two ways to authenticate certificates:
    * Thumbprint. A thumbprint algorithm is run on a certificate to generate a hexadecimal string. The generated string is a unique identifer for the certificate.
    * CA authentication based on a full chain. A certificate chain is a hierarchical list of all certificates needed to authenticate an end-entity (EE) certificate. To authenticate an EE certificate, it's necessary to authenticate each certificate in the chain including a trusted root CA.
    
    **Pros for X.509**
      * X.509 is the most secure authentication type supported in Azure IoT.
      * X.509 allows a high level of control for purposes of certificate management.
      * Many vendors are available to provide X.509 based authentication solutions.
    
    **Cons for X.509**
      * Many customers may need to rely on external vendors for their certificates.
      * Certificate management can be costly and adds to total solution cost.
      * Certificate life-cycle management can be difficult if logistics are not well thought out.

  * ***Trusted Platform Module (TPM)*** - A standard for securely generating and storing cryptographic keys, also known as ISO/IEC 11889. TPM also refers to a virtual or physical I/O device that interacts with modules that implement the standard. A TPM device can exist as discrete hardware, integrated hardware, a firmware-based module, or a software-based module. There are two key differences between TPMs and symmetric keys:
      * TPM chips can also store X.509 certificates.
      * TPM attestation in DPS uses the TPM endorsement key (EK), a form of asymmetric authentication. With asymmetric authentication, a public key is used for encryption, and a separate private key is used for decryption. In contrast, symmetric keys use symmetric authentication, where the private key is used for both encryption and decryption.

    **Pros for TPM**
      * TPMs are included as standard hardware on many Windows devices, with built-in support for the operating system.
      * TPM attestation is easier to secure than shared access signature (SAS) token-based symmetric key attestation.
      * You can easily expire and renew, or roll, device credentials. DPS automatically rolls the IoT Hub credentials whenever a TPM device is due for reprovisioning.

    **Cons for TPM**
      * TPMs are complex and can be difficult to use.
      * Application development with TPMs is difficult unless you have a physical TPM or a quality emulator.
      * You may have to redesign the board of your device to include a TPM in the hardware.
      * If you roll the EK on a TPM, it destroys the identity of the TPM and creates a new one. Although the physical chip stays the same, it has a new identity in your IoT solution.

  * ***Symmetric key*** - The same key is used to encrypt and decrypt messages. As a result, the same key is known to both the device and the service that authenticates it. Azure IoT supports SAS token-based symmetric key connections. Symmetric key authentication requires significant owner responsibility to secure the keys and achieve an equal level of security with X.509 authentication. If you use symmetric keys, the recommended practice is to protect the keys by using a hardware security module (HSM).

    **Pros for symmetric key**
      * Using symmetric keys is the simplest, lowest cost way to get started with authentication.
      * Using symmetric keys streamlines your process because there's nothing extra to generate.
    
    **Cons for symmetric key**
      * Symmetric keys take a significant degree of effort to secure the keys. The same key is shared between device and cloud, which means the key must be protected in two places. In contrast, the challenge with TPM and X.509 certificates is proving possession of the public key without revealing the private key.
      * Symmetric keys make it easy to follow poor security practices. A common tendency with symmetric keys is to hard code the unencrypted keys on devices. While this practice is convenient, it leaves the keys vulnerable. You can mitigate some risk by securely storing the symmetric key on the device. However, if your priority is ultimately security rather than convenience, use X.509 certificates or TPM for authentication.   
      
## Other Helpful Resources

* [Azure IoT Blogs](https://azure.microsoft.com/blog/topics/internet-of-things?wt.mc_id=eventspg_16482_webpage_reactor)
* [Azure IoT Reference Architecture](https://docs.microsoft.com/azure/architecture/reference-architectures/iot?wt.mc_id=eventspg_16482_webpage_reactor)
* [Control access to Azure IoT Hub Device Provisioning Service (DPS)](https://docs.microsoft.com/azure/iot-dps/concepts-control-access-dps?wt.mc_id=eventspg_16482_webpage_reactor)
* [Control access to IoT Hub using Shared Access Signatures](https://docs.microsoft.com/azure/iot-hub/iot-hub-dev-guide-sas?wt.mc_id=eventspg_16482_webpage_reactor)
* [Internet of Things (IoT) Security Best Practices](https://docs.microsoft.com/azure/iot-fundamentals/iot-security-best-practices?wt.mc_id=eventspg_16482_webpage_reactor)
* [Microsoft Tech Community - IoT](https://techcommunity.microsoft.com/t5/internet-of-things-iot/ct-p/IoT?wt.mc_id=eventspg_16482_webpage_reactor) - Blogs and conversation spaces
* [Microsoft Azure Well-Architected Framework for IoT: Security](https://docs.microsoft.com/azure/architecture/framework/iot/iot-security?wt.mc_id=eventspg_16482_webpage_reactor)
* [Network security for IoT Central using private endpoints](https://docs.microsoft.com/azure/iot-central/core/concepts-private-endpoints?wt.mc_id=eventspg_16482_webpage_reactor)
* [Security recommendations for Azure Internet of Things (IoT) deployment](https://docs.microsoft.com/azure/iot-fundamentals/security-recommendations?wt.mc_id=eventspg_16482_webpage_reactor)
* [Security Standards for Azure IoT Edge](https://docs.microsoft.com/azure/iot-edge/security?wt.mc_id=eventspg_16482_webpage_reactor)
* [TLS Support for Azure IoT Hub Device Provisioning Service (DPS)](https://docs.microsoft.com/azure/iot-dps/tls-support?wt.mc_id=eventspg_16482_webpage_reactor)
* [YouTube - Microsoft IoT Developers](https://www.youtube.com/channel/UCL7wy-iy_V76xxPnrIzGOZQ?wt.mc_id=eventspg_16482_webpage_reactor?wt.mc_id=eventspg_16482_webpage_reactor)

Happy studies!
