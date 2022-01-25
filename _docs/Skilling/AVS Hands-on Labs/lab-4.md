---
layout: page
title: AVS HOL LAB4 – Enable Internet Access to Azure VMware Solution
permalink: /skilling/infrastructure/avs-hands-on-labs-lab-4
redirect_from:
- /azure/infrastructure/azure-vmware-solution/hands-on-labs/lab-4
tags: 
 - azure
 - infrastructure
 - AVS
 - skilling
---

# AVS HOL LAB4 – Enable Internet Access to Azure VMware Solution

> This step has been performed part of pre-provisioning the lab environment.  
>
> However, it is still helpful to understand the steps that has been taken.

After you have deployed AVS Private Cloud. You can enable Internet Access from
your AVS workloads to the Internet by following the steps below. This operation
will take between 15-20 minutes.

Using an Internet Browser go to Azure Portal (<https://portal.azure.com>), then
search for “Azure VMware Solution”. Click on the instance you have previously
deployed, then under **Manage**, click on **Connectivity,** and select
**Settings**.

1. Under **Internet enabled**, you’ll see that it is **Disabled** by default.

    ![enable connectivity]({{ site.baseurl }}/assets/avs-hands-on-labs/lab-4/enable-connectivity.png)

2. Select **Enabled** and click **Save** button.

    ![save connectivity]({{ site.baseurl }}/assets/avs-hands-on-labs/lab-4/save-connectivity.png)

3. As mentioned, it will take between 15-20 minutes to apply the changes.

    ![applying changes]({{ site.baseurl }}/assets/avs-hands-on-labs/lab-4/applying-changes.png)

4. AVS Private Cloud properties cannot be modified during that time, as you
   notice in the message below (that you will see if you click on **Refresh**
   button)

    ![connectivity in read only]({{ site.baseurl }}/assets/avs-hands-on-labs/lab-4/read-only.png)

5. After the configuration change has been applied you will be able to access
   to Internet from VMs deployed on AVS Private Cloud, and this is what you’ll
   see when the operation is completed.

    ![changes complete]({{ site.baseurl }}/assets/avs-hands-on-labs/lab-4/changes-complete.png)

**After you complete this step, you should be able to access Internet from VMs
running on AVS Private Cloud.**

## Next Steps

[Back to Table of Content]({{ site.baseurl }}/azure/infrastructure/azure-vmware-solution/hands-on-labs#table-of-contents)

[Lab 5](lab-5)
