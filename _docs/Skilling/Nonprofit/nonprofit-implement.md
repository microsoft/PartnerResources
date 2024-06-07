---
layout: page
title: Your first customer implementation of Microsoft Cloud for Nonprofit
sorttitle: 02
description: Nonprofits need trusted services partners with Microsoft Cloud expertise and industry focus to advise, build, deliver, and support their digital transformation journey.
updated: 2023-02-08
permalink: /skilling/nonprofit/nonprofit-implement
tags:
- learning plan
- industry
- nonprofit
---

# Your first customer implementation of Microsoft Cloud for Nonprofit

Nonprofits need trusted services partners with Microsoft Cloud expertise and industry focus to advise, build, deliver, and support their digital transformation journey.

In addition to a standard deployment and configuration of Fundraising and Engagement or Volunteer Management we encourage you to review this section to ensure successful delivery and identify other opportunities to add value or speed up your customer’s time to value.

## Success by Design
For prescriptive guidance for designing, building, and deploying a Dynamics 365 solution see the [Success by Design Learning Path](https://learn.microsoft.com/en-us/training/paths/use-success-design).

This guidance comes with [20+ examples and templates available on GitHub](https://github.com/MicrosoftDocs/mslearn-developer-tools-power-platform/tree/master/fasttrack/) created by our own FastTrack team to use with your customer to prepare and execute your implementation.

With Success by Design, you can engage with project teams through strategic workshops that are aligned to key project stages with clear goals, actions, and deliverables. Each workshop has been designed with specific goals and maps to relevant success measures for the project. A workshop is essentially an alignment exercise that allows the solution architect to assess if best practices are being followed and identify and highlight issues or potential risks that can derail the project.

## Data migration
When implementing a new fundraising or volunteer management solution it is often necessary to consolidate data that has accumulated in several systems over time. The effort needed to identify, assess, prepare, validate, and load this data is frequently underestimated and is a common driver for delays in delivering value to the customer.

To deliver high value quickly, prioritize the shortest path to getting key users functional the new solutions by decoupling the full scope of data migration from the target launch date. Consider the following strategies when planning for data migration:
 - Establish data migration as a distinct work stream of the project
 - Distinguish data that is needed in Dataverse from data that can be stored in Azure
 - Distinguish data needed for day 1 operations in Dataverse from records or aggregations that could be loaded in the future
 - Organize efforts such that data can be loaded in waves as they are ready

Review the [Create a data migration strategy for Dynamics 365 solutions](https://learn.microsoft.com/en-us/training/modules/data-migration) module of Success by Design for more information and links to useful templates.

## Common system integrations
The Fundraising and Engagement and Volunteer Management solutions included with Microsoft Cloud for Nonprofit build upon Microsoft Cloud technologies (e.g., Dynamics 365, Power Platform, Teams, and SharePoint) that are designed to work together through configuration while also providing the most powerful tools available for advanced integrations.

### Platform integrations
To learn more about configuration-based integrations:
 - Integrate with Exchange to track [email, appointments, contacts, and tasks]()
 - Integrate with Teams [chat](https://learn.microsoft.com/en-us/dynamics365/sales/teams-integration/enable-teams-chat), [meetings](https://learn.microsoft.com/en-us/dynamics365/sales/teams-integration/enable-teams-meeting-integration), [calls](https://learn.microsoft.com/en-us/dynamics365/sales/configure-microsoft-teams-dialer), and [records](https://learn.microsoft.com/en-us/dynamics365/sales/teams-integration/enable-record-linking)
 - Manage documents through integration with [OneDrive](https://learn.microsoft.com/en-us/power-platform/admin/enable-onedrive-for-business?context=%2Fdynamics365%2Fcontext%2Fsales-context), [OneNote](https://learn.microsoft.com/en-us/power-platform/admin/set-up-onenote-integration-in-dynamics-365?context=%2Fdynamics365%2Fcontext%2Fsales-context), and [SharePoint](https://learn.microsoft.com/en-us/dynamics365/sales/connect-with-sharepoint?tabs=SE)
 - Integrate [LinkedIn Sales Insights](https://learn.microsoft.com/en-us/dynamics365/sales/install-lsi-solution)

### Integration with accounting systems
To learn more about how to plan, design, and implement integrations between customer engagement and financial systems see:
 - Integrating [Dynamics 365 Business Central with Dynamics 365 Sales](https://learn.microsoft.com/en-us/dynamics365/business-central/admin-prepare-dynamics-365-for-sales-for-integration)
 - Integrating [Dynamics 365 Business Central with Dataverse](https://learn.microsoft.com/en-us/dynamics365/business-central/admin-common-data-service)
 - Integrating [Dynamics 365 Finance and operations apps with Power Platform](https://learn.microsoft.com/en-us/dynamics365/fin-ops-core/dev-itpro/power-platform/overview)
 - The [Integrate finance and operations apps with Microsoft Power Platform](https://learn.microsoft.com/en-us/training/paths/integrate-finance-operations-apps-power-platform/) learning path

## Adding capabilities through ISV solutions
Many of our ISV partners have offerings designed to integrate with Microsoft Cloud for Nonprofit solutions.

Fundraising and Engagement:
 - Online donation pages and donor portals
 - Donor intelligence
 
Volunteer Management:
 - Background screening services
 
For more information visit [Nonprofit & IGO offers on AppSource](https://appsource.microsoft.com/en-US/marketplace/apps?exp=ubp8&page=1&industry=nonprofit).
