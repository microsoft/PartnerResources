---
layout: page
title: LAB5 – Create content libraries
permalink: /azure/infrastructure/azure-vmware-solution/avs-labs/lab-5
tags: 
 - azure
 - infrastructure
 - AVS
---

# LAB5 – Create content libraries

[Content
libraries](https://docs.vmware.com/en/VMware-vSphere/6.7/com.vmware.vsphere.vm_admin.doc/GUID-254B2CE8-20A8-43F0-90E8-3F6776C2C896.html)
store and manage content in the form of library items. A single library item
consists of one or more files used to deploy virtual machines. These files can
be virtual machine templates or ISO images.

In this lab you are going to create a local content library, stored in the SDDC
vSAN storage and a remote one using Azure Blob Storage.

## Create a local content library

1. Access vCenter and in the drop-down menu select **Content
   Libraries**.

    ![content libraries]({{ site.baseurl }}/assets/avs-labs/lab-5/content-libraries.png)

2. Select the **Add** button to create a new content library.

    ![add content libraries]({{ site.baseurl }}/assets/avs-labs/lab-5/add-content-library.png)

3. Enter the name for the library and select the AVS vCenter Server. Click
   Next.

    ![name content library]({{ site.baseurl }}/assets/avs-labs/lab-5/name-content-library.png)

4. Under **Configure content library**, select **Local content library**. You
   can keep **Enable Published** un-checked.

5. In **Add Storage** select the vSAN datastore (**vsanDatastore**)

    ![add storage]({{ site.baseurl }}/assets/avs-labs/lab-5/add-storage.png)

6. Click **Next**, verify the data and click **Finish**.

7. The new library will appear, select it and in the **Actions** menu select
   **Import item**. ![import item]({{ site.baseurl }}/assets/avs-labs/lab-5/import-item.png)

8. Enter the URL of the Photon OS OVA (below) or any other OVA/ISO you might
   have and click **Import**.
   <https://packages.vmware.com/photon/4.0/GA/ova/photon-hw13-uefi-4.0-1526e30ba0.ova>

    ![import url]({{ site.baseurl }}/assets/avs-labs/lab-5/import-url.png)

9. You may get a note about the SSL certificate that signed the OVA file is not
   trusted. Choose the **Action \> Continue** when asked “SSL certificate from
   server packages.vmware.com cannot be trusted. Do you want to proceed?”
  
   ![import action continue]({{ site.baseurl }}/assets/avs-labs/lab-5/import-action-continue.png)

   Then choose **Proceed Anyway**

   ![proceed anyway]({{ site.baseurl }}/assets/avs-labs/lab-5/proceed-anyway.png)

10. After the OVA has been imported it will be available in the **Templates**
    area.

    ![templates]({{ site.baseurl }}/assets/avs-labs/lab-5/templates.png)

## Next Steps

[Back to Table of Content]({{ site.baseurl }}/azure/infrastructure/azure-vmware-solution/avs-labs#table-of-contents)

[Lab 6](lab-6)
