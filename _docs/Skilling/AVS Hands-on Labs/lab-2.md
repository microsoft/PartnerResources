---
layout: page
title: AVS HOL LAB2 – Configure Private Cloud access
permalink: /skilling/infrastructure/avs-hands-on-labs-lab-2
redirect_from:
- /azure/infrastructure/azure-vmware-solution/hands-on-labs/lab-2
tags: 
 - azure
 - infrastructure
 - AVS
 - skilling
---

# AVS HOL LAB2 – Configure Private Cloud Access

Once the new Private Cloud is deployed, you need to configure access to it. To
achieve it you will need to do a series of task as explained below.

## Jumpbox deployment

> This step has been performed part of pre-provisioning the lab environment.  
>
> However, it is still helpful to understand the steps that has been taken.

To access your training environment the first component you will need is a
Jumpbox, in this case a Windows 10 virtual machine on Azure IaaS. You will
connect this virtual machine to the same Azure VNET created during the Private
Cloud deployment in the default subnet.

In the Azure portal select **Create a new resource** and search for **Windows
10**, select one of the available Windows 10 images and in the next window click
on **Create**.

Fill in all the needed parameters, like name, resource group, region, etc.

![new virtual machine dialog]({{ site.baseurl }}/assets/avs-hands-on-labs/lab-2/new-resource.png)

In **Inbound port rules** select None and then move to the networking pane.

![inbound ports]({{ site.baseurl }}/assets/avs-hands-on-labs/lab-2/inbound-port-rules.png)

Launch the creation of the virtual machine, it will take only a few minutes to
complete and then move to the next section.

## Azure Bastion configuration

> This step has been performed part of pre-provisioning the lab environment.  
>  
> However, it is still helpful to understand the steps that has been taken.

After the Jumpbox is up and running the next step would be to deploy and
configure Azure Bastion.

Bastion is a service in Azure that enables you to connect to a virtual machine
using a browser and the Azure portal. It provides secure and seamless RDP/SSH
connectivity to your virtual machines directly from the Azure portal over TLS.
That way your virtual machines will not need a public IP address, agent, or
special client software.

Bastion provides secure RDP and SSH connectivity to all the VMs in the virtual
network in which it is provisioned and directly peered virtual networks.

The main prerequisite for Bastion is for the VNET to contain a subnet named
**AzureBastionSubnet** with /27 CIDR network address.

You need to create an additional subnet for Bastion in the existing. Browse to
the created VNet and open the **Subnets** pane. Add a new subnet and name it
**AzureBastionSubnet**.

![add subnet]({{ site.baseurl }}/assets/avs-hands-on-labs/lab-2/add-subnet.png)

Now you will create an Azure Bastion host. Go back then to the home screen of
the Azure portal select **Create a new resource**, search for **Bastion,** and
click on **Create**.

![TODO:]({{ site.baseurl }}/assets/avs-hands-on-labs/lab-2/create-bastion.png)

After filling out all the required parameters go to **Review + create** and
launch the deployment.

## Access the Private Cloud – Animation

This animation walks you through the steps of accessing the Jumpbox using Azure
Bastion, then connecting to vCenter and NSX-Manager portals of Azure VMware
Solution.

> The Jumpbox credentials will be provided once you activate the lab
> environment as part of the information to access your lab environment.

![access private cloud]({{ site.baseurl }}/assets/avs-hands-on-labs/lab-2/access-private-cloud.gif)

There is a YouTube video that you can use as a backup to this animation above:  
[Azure VMware Solution (AVS) Access Management Portals using a Jumpbox and Azure
Bastion](https://www.youtube.com/watch?v=EYwakIcxmVI&ab_channel=HusamHilal)

## Access the Private Cloud

These are the detailed instructions of what you’ve seen in the section before
(Animation).

1. Navigate to the Jumpbox virtual machine and from the **Overview** pane click
   on **Connect** and select **Bastion**.
  
   The Jumpbox name could vary, and it’s not exactly as you see in the
   screenshots below. The Jumpbox is the only provided Azure VM in this lab
   environment. You will not need to create a new Jumpbox VM.

![avs jumpbox]({{ site.baseurl }}/assets/avs-hands-on-labs/lab-2/avs-jumpbox.png)

1. Enter the provided username and password used during the deployment of the
   Jumpbox and click **Connect**.
  
   Credentials provided could be different of what you see in the screenshot
   below.

![avs bastion]({{ site.baseurl }}/assets/avs-hands-on-labs/lab-2/avs-bastion.png)

1. A new browser window will open and show the virtual machine desktop. ![A
   picture containing text, monitor, screenshot, computer Description
   automatically generated]({{ site.baseurl }}/assets/avs-hands-on-labs/lab-2/jumpbox-desktop.png)

2. Now lookup the URL for vSphere Web client, you will find this in the AVS
   Private Cloud Identity pane. From the Jumpbox desktop open the Edge browser
   and access your Private Cloud vCenter client.  
  
   ![private ploud identity]({{ site.baseurl }}/assets/avs-hands-on-labs/lab-2/private-cloud-identity.png)  
  
   From this screen you can copy the *cloudadmin@vsphere.local* user password
   as well. Go back to the Bastion tab and access vCenter from Edge browser.

   ![A picture containing text, screenshot, indoor, computer Description
   automatically generated]({{ site.baseurl }}/assets/avs-hands-on-labs/lab-2/vcenter.png)

3. Repeat the operation for NSX-T Manager and verify you can access it.

> See the animation/previous section as it summarizes this section and shows
> you how to access
> AVS management portals via the Jumpbox and through Azure Bastion

## Next Steps

[Back to Table of Content]({{ site.baseurl }}/azure/infrastructure/azure-vmware-solution/hands-on-labs#table-of-contents)

[Lab 3](lab-3)
