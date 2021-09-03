---
layout: page
title: LAB13B – Configure Alerts and Notifications
permalink: /azure/infrastructure/azure-vmware-solution/hands-on-labs/lab-13
tags: 
 - azure
 - infrastructure
 - AVS
---

# LAB13B – Configure Alerts and Notifications

In this lab you'll learn how to configure [Azure Action
Groups](https://docs.microsoft.com/en-us/azure/azure-monitor/alerts/action-groups)
in [Microsoft Azure
Alerts](https://docs.microsoft.com/en-us/azure/azure-monitor/alerts/alerts-overvie)
to receive notifications of triggered events that you define. You'll also learn
about using [Azure Monitor
Metrics](https://docs.microsoft.com/en-us/azure/azure-monitor/essentials/data-platform-metrics)
to gain deeper insights into your Azure VMware Solution Private Cloud.

## Supported metrics and activities

The following metrics are visible through Azure Monitor Metrics.

| **Signal name**                                                         | **Signal type** | **Monitor service** |
| ----------------------------------------------------------------------- | --------------- | ------------------- |
| Datastore Disk Total Capacity                                           | Metric          | Platform            |
| Percentage Datastore Disk Used                                          | Metric          | Platform            |
| Percentage CPU                                                          | Metric          | Platform            |
| Average Effective Memory                                                | Metric          | Platform            |
| Average Memory Overhead                                                 | Metric          | Platform            |
| Average Total Memory                                                    | Metric          | Platform            |
| Average Memory Usage                                                    | Metric          | Platform            |
| Datastore Disk Used                                                     | Metric          | Platform            |
| All Administrative operations                                           | Activity Log    | Administrative      |
| Register Microsoft.AVS resource provider. (Microsoft.AVS/privateClouds) | Activity Log    | Administrative      |
| Create or update a PrivateCloud. (Microsoft.AVS/privateClouds)          | Activity Log    | Administrative      |
| Delete a PrivateCloud. (Microsoft.AVS/privateClouds)                    | Activity Log    | Administrative      |

## Configure an alert rule

1. From your Azure VMware Solution Private Cloud, select **Monitoring** \>
   **Alerts**, and then **New alert rule**.

   ![new alert rule]({{ site.baseurl }}/assets/avs-hands-on-labs/lab-13/d28fc9d3274d9eeabf50d70b6761592b.png)

   A new configuration screen opens where you'll:

   - Define the Scope

   - Configure a Condition

   - Set up the Action Group

   - Define the Alert rule details

   ![create alert rule]({{ site.baseurl }}/assets/avs-hands-on-labs/lab-13/ce071106649f23f9d87ce16274a4d221.png)

2. Under **Scope**, select the target resource you want to monitor. By default,
   the Azure VMware Solution Private Cloud from where you opened the Alerts
   menu has been defined.

3. Under **Condition**, select **Add condition**, and in the window that opens,
   selects the signal you want to create for the alert rule.

   In this example, you've selected **Percentage Datastore Disk Used**, which
   is relevant from an [Azure VMware Solution SLA](https://aka.ms/avs/sla)
   perspective.

   ![Screenshot that shows the Configure signal logic window with predefined
   signal names.]({{ site.baseurl }}/assets/avs-hands-on-labs/lab-13/6d1cefa2d8f0d370d3c0445ffb6869e1.png)

4. Define the logic that will trigger the alert and then select **Done**.

   In our example, only the **Threshold** and **Frequency of evaluation** have
   been adjusted.

   ![Screenshot that shows the information for the selected signal
   logic.]({{ site.baseurl }}/assets/avs-hands-on-labs/lab-13/aebd148dc13f1383e8cd083aa05f2300.png)

5. Under **Actions**, select **Add action groups**. The action group defines
   *how* the notification is received and *who* receives it. You can receive
   notifications by email, SMS, [Azure Mobile App Push
   Notification](https://azure.microsoft.com/features/azure-portal/mobile-app/)
   or voice message.

   ![Screenshot that shows the existing action groups and where to create a new
   action group.]({{ site.baseurl }}/assets/avs-hands-on-labs/lab-13/e7ef5799bf8a6212b64f91606dd0cab5.png)

6. In the window that opens, select **Create action group**.

   Tip

   You can also use an existing action group.

   ![Screenshot that shows the action groups to select for the
   alert.]({{ site.baseurl }}/assets/avs-hands-on-labs/lab-13/01642094b03ca180914e12304f35095b.png)

7. In the window that opens, on the **Basics** tab, give the action group a
   name and a display name.

8. Select the **Notifications** tab, select a **Notification Type** and
   **Name**. Then select **OK**.

   This example is based on email notification.

   ![Screenshot that shows the email, SMS message, push, and voice settings for
   the alert.]({{ site.baseurl }}/assets/avs-hands-on-labs/lab-13/520f475a29624a258bb0f9b61ab934c6.png)

9. (Optional) Configure the **Actions** if you want to take proactive actions
   and receive notification on the event. Select an available **Action type**
   and then select **Review + create**.

   - Automation Runbooks

   - Azure Functions – for custom event-driven serverless code execution

   - ITSM – to integrate with a service provider like ServiceNow to create a
     ticket

   - Logic App - for more complex workflow orchestration

   - Webhooks - to trigger a process in another service

     ![Screenshot that shows the Create action group window with a focus on
     the Action type drop-down.]({{ site.baseurl }}/assets/avs-hands-on-labs/lab-13/6248cf7442c5d1bdfe46c5cb93e80e83.png)

10. Under the **Alert rule details**, provide a name, description, resource
    group to store the alert rule, the severity. Then select **Create alert
    rule**.

    ![Screenshot that shows the details for the alert
    rule.]({{ site.baseurl }}/assets/avs-hands-on-labs/lab-13/a5e134e4db680d3b7187ff18ea1c12c1.png)

    The alert rule is visible and can be managed from the Azure portal.

    ![Screenshot that shows the new alert rule in the Rules
    window.]({{ site.baseurl }}/assets/avs-hands-on-labs/lab-13/3d0171d6ca769e58be513ea4bc77cf45.png)

    As soon as a metric reaches the threshold as defined in an alert rule, the
    **Alerts** menu is updated and made visible.

    ![Screenshot that shows the alert after reaching the threshold
    defined.]({{ site.baseurl }}/assets/avs-hands-on-labs/lab-13/00ab76d73ed506e5346496f6c80ea91d.png)

    Depending on the configured Action Group, you'll receive a notification
    through the configured medium. In our example, you’ve configured email.

    ![Screenshot of an Azure Monitor Alert with the error string, and the date
    and time event was triggered.]({{ site.baseurl }}/assets/avs-hands-on-labs/lab-13/5604ea99cce70203bb08f528d640182f.png)

## Work with metrics

1. From your Azure VMware Solution Private Cloud, select **Monitoring** \>
   **Metrics**. Then select the metric you want from the drop-down.

   ![Screenshot that shows the Metrics window and a focus on the Metric
   drop-down.]({{ site.baseurl }}/assets/avs-hands-on-labs/lab-13/a768f47c87b8ad2bdcf4613e6b2dabc6.png)

2. You can change the diagram's parameters, such as the **Time range** or the
   **Time granularity**.

   Other options are:

   - **Drill into Logs** and query the data in the related Log Analytics
     workspace

   - **Pin this diagram** to an Azure Dashboard for convenience.

     ![Screenshot that shows the time range and time granularity options for
     metric.]({{ site.baseurl }}/assets/avs-hands-on-labs/lab-13/0218b28502ff09fd5d1e717d27a3ea2b.png)

## Next Steps

[Back to Table of Content]({{ site.baseurl }}/azure/infrastructure/azure-vmware-solution/hands-on-labs#table-of-contents)

[Lab 14](lab-14)
