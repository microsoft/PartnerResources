---
layout: page
title: AVS HOL LAB9 – Assign Public IP to virtual machine on Azure VMware Solution
permalink: /skilling/infrastructure/avs-hands-on-labs-lab-9
redirect_from: 
- /azure/infrastructure/azure-vmware-solution/hands-on-labs/lab-9
showbreadcrumb: false
tags: 
 - azure
 - infrastructure
 - AVS
 - skilling
---

# AVS HOL LAB9 – Assign Public IP to virtual machine on Azure VMware Solution

Next, you will assign a Public IP address to the virtual machine. You will need
to create a Firewall Policy in the VWAN instance deployed in a previous lab.

1. In the Azure portal, search for and select **Firewall Manager**.

   ![select firewall]({{ site.baseurl }}/assets/avs-hands-on-labs/lab-9/e90833ce038d458a2b5d1fc29864c031.png)

2. To view the available Public IPs that can be used when configuring the
   Firewall Policy. Click on **Virtual Hubs** on the left, then select the
   instance that **vWAN Hub instance** that was created for AVS.

   ![virtual hubs]({{ site.baseurl }}/assets/avs-hands-on-labs/lab-9/926eee7afd7e98d17e370889b04efcfa.png)

   Click on **Public IP Configuration** to view all IPs, copy and take note for
   one of them as you’ll be using in next steps.

   ![public ips]({{ site.baseurl }}/assets/avs-hands-on-labs/lab-9/f9043cde37cbff3bc2822d1ce6a76967.png)

3. Go back to **Firewall Manager** blade, Select **Azure Firewall Policies**
   and then select **Create Azure Firewall Policy**.

   ![azure policies]({{ site.baseurl }}/assets/avs-hands-on-labs/lab-9/e5c087e7b454d672d56262c589f77009.png)

4. Under the **Basics** tab, provide the required details and select **Next:
   DNS Settings**.

5. Under the **DNS** tab, select **Disable**, and then click on **Next: TLS
   inspection**.

6. Under the **TLS inspection** tab, click on **Next: Rules**.

7. Select **Add a rule collection**, provide the below details, and select
   **Add** and then select **Next: Threat intelligence**.

- Name

- Rules collection Type: **DNAT**

- Priority: (i.e., 1000)

- Name of rule

- Source Type: IP Address

- Source: \*

- Protocol: TCP

- Destination port: 80

- Destination Type: IP Address

- Destination: Public IP Address (that was copied from the earlier step –
  Step\#2)

- Translated address: AVS hosted Web Server (Photon OS VM - Nginx Server)
  private IP Address.

- Translated port: AVS hosted Web Server (Photon OS VM - Nginx Server) port
  (i.e.: 80)
  
  ![]({{ site.baseurl }}/assets/avs-hands-on-labs/lab-9/de03674068346dacf8cb19fa7a1db1c1.png)
  
  ![Graphical user interface Description automatically generated with medium
  confidence]({{ site.baseurl }}/assets/avs-hands-on-labs/lab-9/58338a0aa977e2f72aa1056540135bc3.png)

1. Click on Add (![]({{ site.baseurl }}/assets/avs-hands-on-labs/lab-9/2aff104678e54e1ca38eb23eb1208d73.png)) button to add
   the Rule and move to **Review + Create** section. Then click **Create**
   button to create the Azure Firewall Policy. ![Graphical user interface,
   text, application, email Description automatically
   generated]({{ site.baseurl }}/assets/avs-hands-on-labs/lab-9/73c29aae1247e6cde824376b4535ac0a.png)

2. Now, the Azure Firewall **Policy is ready**, next step would be associate it
   with vWan Hub that’s linked to AVS. Go to **Azure Firewall Policies**,
   select the created policy, and click on **Manage associations**, choose
   **Associate hubs**.  
   ![]({{ site.baseurl }}/assets/avs-hands-on-labs/lab-9/b181d1a166428f48e6f9c4b46fd778e3.png)

3. Select the Virtual Hub that is linked to AVS and click on **Add** button.

   ![]({{ site.baseurl }}/assets/avs-hands-on-labs/lab-9/26db8e0d6414481d15c0330a2c2b93bb.png)

4. Wait for few minutes, then the Azure Firewall Policy you created will be
   associated with the virtual Hub that’s linked with AVS.
   ![]({{ site.baseurl }}/assets/avs-hands-on-labs/lab-9/14f5fa2ea95c23301866e3a3b8abace5.png)

5. NOW, is testing time!

   Copy the IP that you initially configured in the Azure Firewall Policy, as
   it is now will be the Public IP of the assigned AVS hosted VM and put it
   your workstation browser address bar. Since that AVS hosted VM has Nginx
   Server deployed, you should be able to see the Nginx Server default page.

   ![]({{ site.baseurl }}/assets/avs-hands-on-labs/lab-9/89d0a7bc6f2ea6de222ed55011d59c57.png)

**As you noticed, you were able to publish a web server hosted on AVS VM
directly to the Internet by assigning it a public IP address through Azure
Firewall Policy.**

## Next Steps

[Back to Table of Content]({{ site.baseurl }}/azure/infrastructure/azure-vmware-solution/hands-on-labs#table-of-contents)

[Lab 10](lab-10)
