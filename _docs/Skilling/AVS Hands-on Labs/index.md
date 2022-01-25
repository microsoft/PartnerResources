---
layout: page
title: AVS Hands-on Labs
permalink: /skilling/infrastructure/avs-hands-on-labs
redirect_from:
 - /azure/infrastructure/azure-vmware-solution/hands-on-labs
showbreadcrumb: false
tags: 
 - azure
 - infrastructure
 - AVS
 - skilling
---

# AVS Hands-on Labs

## Table of Contents

[Before the Training](avs-hands-on-labs-before-the-training)

[Before the Training]({{ site.baseurl }}/azure/infrastructure/azure-vmware-solution/hands-on-labs/before-the-training)

- [Microsoft Learn Module]({{ site.baseurl }}/azure/infrastructure/azure-vmware-solution/hands-on-labs/before-the-training#microsoft-learn-module)
- [Capacity Planning (optional)]({{ site.baseurl }}/azure/infrastructure/azure-vmware-solution/hands-on-labs/before-the-training#capacity-planning-optional)

[Expected Time Needed Per Lab]({{ site.baseurl }}/azure/infrastructure/azure-vmware-solution/hands-on-labs/expected-time-needed-per-lab#expected-time-needed-per-lab)

- [Important Notes]({{ site.baseurl }}/azure/infrastructure/azure-vmware-solution/hands-on-labs/expected-time-needed-per-lab#important-notes)

[Lab Environment]({{ site.baseurl }}/azure/infrastructure/azure-vmware-solution/hands-on-labs/lab-environment#lab-environment)

- [Azure VMware Solution Environment]({{ site.baseurl }}/azure/infrastructure/azure-vmware-solution/hands-on-labs/lab-environment#azure-vmware-solution-environment)

- [Lab Architecture Diagram]({{ site.baseurl }}/azure/infrastructure/azure-vmware-solution/hands-on-labs/lab-environment#lab-architecture-diagram)
  
- [On-Premises Connectivity]({{ site.baseurl }}/azure/infrastructure/azure-vmware-solution/hands-on-labs/lab-environment#on-premises-connectivity)
  
- [Resources]({{ site.baseurl }}/azure/infrastructure/azure-vmware-solution/hands-on-labs/lab-environment#resources)
  
- [Architecture Diagram]({{ site.baseurl }}/azure/infrastructure/azure-vmware-solution/hands-on-labs/lab-environment#architecture-diagram)

[Lab Objectives]({{ site.baseurl }}/azure/infrastructure/azure-vmware-solution/hands-on-labs/lab-objectives)

[LAB1 – Azure VMware Solution Deployment]({{ site.baseurl }}/azure/infrastructure/azure-vmware-solution/hands-on-labs/lab-1)

[LAB2 – Configure Private Cloud access    7]({{ site.baseurl }}/azure/infrastructure/azure-vmware-solution/hands-on-labs/lab-2)

- [Jumpbox deployment]({{ site.baseurl }}/azure/infrastructure/azure-vmware-solution/hands-on-labs/lab-2#jumpbox-deployment)

- [Azure Bastion configuration]({{ site.baseurl }}/azure/infrastructure/azure-vmware-solution/hands-on-labs/lab-2#azure-bastion-configuration)

- [Access the Private Cloud – Animation]({{ site.baseurl }}/azure/infrastructure/azure-vmware-solution/hands-on-labs/lab-2#access-the-private-cloud--animation)

- [Access the Private Cloud]({{ site.baseurl }}/azure/infrastructure/azure-vmware-solution/hands-on-labs/lab-2#access-the-private-cloud)

[LAB3 – Initial NSX-T configuration]({{ site.baseurl }}/azure/infrastructure/azure-vmware-solution/hands-on-labs/lab-3#lab3--initial-nsx-t-configuration)

- [Create DHCP Server from Azure portal]({{ site.baseurl }}/azure/infrastructure/azure-vmware-solution/hands-on-labs/lab-3#create-dhcp-server-from-azure-portal)
- [Create NSX network segment from Azure portal]({{ site.baseurl }}/azure/infrastructure/azure-vmware-solution/hands-on-labs/lab-3#create-nsx-network-segment-from-azure-portal)
- [Configure DNS from Azure portal]({{ site.baseurl }}/azure/infrastructure/azure-vmware-solution/hands-on-labs/lab-3#configure-dns-from-azure-portal)
  - [Step 1 - Configure a default DNS zone and FQDN zone]({{ site.baseurl }}/azure/infrastructure/azure-vmware-solution/hands-on-labs/lab-3#step-1---configure-a-default-dns-zone-and-fqdn-zone)
  - [Step 2 - Configure DNS service]({{ site.baseurl }}/azure/infrastructure/azure-vmware-solution/hands-on-labs/lab-3#step-2---configure-dns-service)
  - [Step 3 - Configure DNS Forwarder]({{ site.baseurl }}/azure/infrastructure/azure-vmware-solution/hands-on-labs/lab-3#step-3---configure-dns-forwarder)

[LAB4 – Enable Internet Access to Azure VMware Solution]({{ site.baseurl }}/azure/infrastructure/azure-vmware-solution/hands-on-labs/lab-4)

[LAB5 – Create content libraries    26]({{ site.baseurl }}/azure/infrastructure/azure-vmware-solution/hands-on-labs/lab-5)

[LAB6 – Deploy a virtual machine on Azure VMware Solution]({{ site.baseurl }}/azure/infrastructure/azure-vmware-solution/hands-on-labs/lab-6)

[LAB7 – Access Azure Storage Account through Azure Private Endpoint]({{ site.baseurl }}/azure/infrastructure/azure-vmware-solution/hands-on-labs/lab-7)

[LAB8 – Enable Public IP for AVS]({{ site.baseurl }}/azure/infrastructure/azure-vmware-solution/hands-on-labs/lab-8)

[LAB9 – Assign Public IP to virtual machine on Azure VMware Solution]({{ site.baseurl }}/azure/infrastructure/azure-vmware-solution/hands-on-labs/lab-9)

[LAB10 – Connect from Azure Application Gateway to AVS hosted workload]({{ site.baseurl }}/azure/infrastructure/azure-vmware-solution/hands-on-labs/lab-10)

[LAB11B – Scale an AVS Cluster]({{ site.baseurl }}/azure/infrastructure/azure-vmware-solution/hands-on-labs/lab-11)

- [Add a new cluster]({{ site.baseurl }}/azure/infrastructure/azure-vmware-solution/hands-on-labs/lab-11#add-a-new-cluster)
- [Scale a cluster](lab-11#scale-a-cluster)

[LAB12B – Configure HCX (HoL)]({{ site.baseurl }}/azure/infrastructure/azure-vmware-solution/hands-on-labs/lab-12)

[LAB13B – Configure Alerts and Notifications]({{ site.baseurl }}/azure/infrastructure/azure-vmware-solution/hands-on-labs/lab-13)

- [Supported metrics and activities]({{ site.baseurl }}/azure/infrastructure/azure-vmware-solution/hands-on-labs/lab-13#supported-metrics-and-activities)
- [Configure an alert rule]({{ site.baseurl }}/azure/infrastructure/azure-vmware-solution/hands-on-labs/lab-13#configure-an-alert-rule)
- [Work with metrics](lab-13#work-with-metrics)

[LAB14B – Create a remote content library in Azure Blob Storage]({{ site.baseurl }}/azure/infrastructure/azure-vmware-solution/hands-on-labs/lab-14)

[APPENDIX 1 – Azure VMware Solution Deployment]({{ site.baseurl }}/azure/infrastructure/azure-vmware-solution/hands-on-labs/appendixes#appendix-1--azure-vmware-solution-deployment)

[APPENDIX 2 – Configure AVS Networking from NSX-T Manager]({{ site.baseurl }}/azure/infrastructure/azure-vmware-solution/hands-on-labs/appendixes#appendix-2--configure-avs-networking-from-nsx-t-manager)

[APPENDIX 3 - Deploy VMware Photon OS OVA from URL]({{ site.baseurl }}/azure/infrastructure/azure-vmware-solution/hands-on-labs/appendixes#appendix-3---deploy-vmware-photon-os-ova-from-url)

[APPENDIX 4 – Configure DNS Forwarding through Conditional Forwarders]({{ site.baseurl }}/azure/infrastructure/azure-vmware-solution/hands-on-labs/appendixes#appendix-4--configure-dns-forwarding-through-conditional-forwarders)
