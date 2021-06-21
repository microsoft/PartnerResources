---
layout: page
title: Lab Environment
tags: 
 - azure
 - infrastructure
 - AVS
---

# Lab Environment

## Pre-provisioned Azure VMware Solution Environment

The deployment of the Azure VMware Solution takes at least 2 hours to complete.
Since it is not practical to wait that long in this training, an AVS environment
has been pre-deployed for you. You will build on top of its foundation during
the lab exercises.

The AVS pre-provisioned environment has been configured with these components
and settings (as you see in the architecture diagram):

1. Internet Access (outbound connectivity from AVS to the Internet)

2. Public IP Addresses - 10 IPs (inbound connectivity from Internet to AVS)

3. Azure VM used as Jumpbox (used for AVS management and as DNS Forwarder)

4. Azure VNet with its corresponding Subnets and connectivity to AVS through an
   Azure Express Route Virtual Network Gateway.

## Lab Architecture Diagram

![lab-architecture-diagram](media/lab-environment/lab-architecture-diagram.png)


## On-Premises Connectivity

For testing purposes, you can connect the provided lab environment with your
on-premises environment through Site-to-Site VPN to the Azure vWAN Hub, and that
will allow on-premises connectivity to Azure VMware Solution. This is a
self-paced exercise, and instructions are out of the scope of this lab guide.
However, the following are some resources you can use to establish the VPN
connectivity.

It’s important to mention that Express Route to on-premises is the recommended
method to perform integrations and migrations through VMware HCX. The VPN
approach is just for testing purposes.

### Resources

[Create an IPSec tunnel into Azure VMware Solution - Azure VMware Solution \|
Microsoft
Docs](https://docs.microsoft.com/en-us/azure/azure-vmware/create-ipsec-tunnel)

[Connect to Azure VMware Solution (AVS) using VPN - Microsoft Tech
Community](https://techcommunity.microsoft.com/t5/azure-migration/connect-to-azure-vmware-solution-avs-using-vpn/ba-p/1670603)

[Site-to-Site VPN between NSX-T and Azure VMware Solution – Part 1 –
vElements.net](http://www.velements.net/2021/01/21/site-to-site-vpn-between-nsx-t-and-azure-vmware-solution-part-1/)

[Site-to-Site VPN between NSX-T and Azure VMware Solution – Part 2 –
vElements.net](http://www.velements.net/2021/02/12/site-to-site-vpn-between-nsx-t-and-azure-vmware-solution-part-2/)

### Architecture Diagram

![on-premises-connectivity](media/lab-environment/on-premises-connectivity.png)

## Next Steps

[Back to Table of Content](toc.md#table-of-contents)

[Lab Objectives](lab-objectives.md)