---
layout: page
title: AVS Hands-on Labs - Lab Environment
permalink:  /skilling/infrastructure/avs-hands-on-labs-lab-environment
redirect_from:
- /azure/infrastructure/azure-vmware-solution/hands-on-labs/lab-environment
tags: 
 - azure
 - infrastructure
 - AVS
 - skilling
---

# AVS Hands-on Labs - Lab Environment

## Azure VMware Solution Environment

The deployment of the Azure VMware Solution takes at least 2 hours to complete.
If you are doing this on your own, visit the [appendix section](appendixes)
for instructions on how to configure the environment. However, If you are
in a Microsoft organized event, usually it is pre-deployed for you with the
following components and settings.

1. Internet Access (outbound connectivity from AVS to the Internet)
2. Public IP Addresses - 10 IPs (inbound connectivity from Internet to AVS)
3. Azure VM used as Jumpbox (used for AVS management and as DNS Forwarder)
4. Azure VNet with its corresponding Subnets and connectivity to AVS through an
   Azure Express Route Virtual Network Gateway.

## Lab Architecture Diagram

![lab-architecture-diagram]({{ site.baseurl }}/assets/avs-hands-on-labs/lab-environment/lab-architecture-diagram.png)

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

![on-premises-connectivity]({{ site.baseurl }}/assets/avs-hands-on-labs/lab-environment/on-premises-connectivity.png)

## Next Steps

[Back to Table of Content]({{ site.baseurl }}/azure/infrastructure/azure-vmware-solution/hands-on-labs#table-of-contents)

[Lab Objectives](lab-objectives)