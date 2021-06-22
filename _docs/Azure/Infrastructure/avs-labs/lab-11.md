---
layout: page
title: LAB11B – Scale an AVS Cluster
tags: 
 - azure
 - infrastructure
 - AVS
---

# LAB11B – Scale an AVS Cluster

This Labs requires enough available quota to be able to scale. If you do not
have the quota, you will still be able to experience the portal experience and
learn from that. You can request quota by creating a [new support
request](https://docs.microsoft.com/en-us/azure/azure-vmware/enable-azure-vmware-solution),
but that’s outside of the scope of this lab.

## Add a new cluster

1. On the overview page of an existing Private Cloud, under **Manage**, select
   **Scale Private Cloud**. Next, select **+ Add a cluster**.

   ![select add a cluster](assets/lab-11/005d388c9c101888b1ad631422db6bb4.png)

2. In the **Add cluster** page, use the slider to select the number of hosts.
   Click **Save**, then the deployment of the new cluster will begin.

   ![select the number of hosts](assets/lab-11/2be4a5197e1bf9c9da1898d65dd3a4f4.png)

## Scale a cluster

1. On the overview page of an existing Private Cloud, select **Scale Private
   Cloud** and select the pencil icon to edit the cluster.

   ![overview](assets/lab-11/41c72df09118cc693272f9317d6c86ef.png)

2. In the **Edit Cluster** page, use the slider to select the number of hosts.
   Click **Save**, then the addition of hosts to the cluster begins.

   ![edit cluster.](assets/lab-11/dc19789bf264f2eca99ebbfc0b0072d6.png)

## Next Steps

[Back to Table of Content](index.md#table-of-contents)

[Lab 12](lab-12.md)
