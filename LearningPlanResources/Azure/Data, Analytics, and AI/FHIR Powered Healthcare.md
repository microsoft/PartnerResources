---
layout: default
title: FHIR Powered Healthcare
parent: Data Analytics and AI
grand_parent: Azure
---

# Learning Plan Resources for FHIR Powered Healthcare

Fast Healthcare Interoperability Resources (FHIR) is a next generation standards framework created by HL7 (hl7.org/fhir).  FHIR combines the best features of HL7’s v2, HL7 v3 and CDA product lines while leveraging the latest web standards and applying a tight focus on implementability.

Microsoft’s FHIR solutions are built from a set of modular components that can easily be assembled into working systems that solve real world clinical and administrative problems at a fraction of the price of existing alternatives.  FHIR is suitable for use in a wide variety of contexts mobile phone apps, cloud communications, EHR-based data sharing, server communication in large institutional healthcare providers, and much more.

In the **[FHIR Powered Healthcare | What The Hack](https://microsoft.github.io/WhatTheHack/027-FHIRPoweredHealthcare/)** workshop, you will be guided through a sequence of challenges to implement [Microsoft Health Architectures](https://microsoft.github.io/health-architectures/) to extract, transform and load patient data into a FHIR Compliant store.  You will deploy an event-driven serverless architecture to ingest HL7v2 messages and publish FHIR CUD events to an Event Hub.  Topic subscribers to these events can then trigger downstream post-processing workflows whenever new medical event is published.  Once the FHIR and legacy health data are ingested into the FHIR Server, you will then write JavaScript code to connect and read these data via the FHIR service to explore FHIR patient records.

Learning resources for the [FHIR Powered Healthcare hack](https://microsoft.github.io/WhatTheHack/027-FHIRPoweredHealthcare/) is broken down as follows:
* Fundamentals, Associate, Expert, Specialist: content categorized in increasing level of complexity
* Certifications: relevant Microsoft exams or certifications
* Community resources: user groups, events, blogs


## Keeping Up

* [Blog Post: Microsoft Cloud for Healthcare is transforming the healthcare journey](https://cloudblogs.microsoft.com/industry-blog/health/2020/10/28/microsoft-cloud-for-healthcare-is-transforming-the-healthcare-journey/)
* [Blog Post: Real world examples and ideas from Microsoft Health Team members](https://microsoft.github.io/health-architectures/Posts.html)
* [Blog: Azure API for FHIR moves to general availability](https://azure.microsoft.com/en-us/blog/azure-api-for-fhir-moves-to-general-availability/)
* [Twitter: Health_IT](https://twitter.com/Health_IT)


## Fundamentals

* [Quickstart: Deploy Azure API for FHIR using Azure portal](https://docs.microsoft.com/en-us/azure/healthcare-apis/fhir-paas-portal-quickstart) (Self-Paced) (1 Hour)
    * In this quickstart, you will learn how to deploy Azure API for FHIR using the Azure portal.
* [Quickstart: Deploy Azure IoT Connector for FHIR using Azure portal](https://docs.microsoft.com/en-us/azure/healthcare-apis/iot-fhir-portal-quickstart) (Self-Paced) (1 Hour)
    * Azure IoT Connector for FHIR is an optional feature of Azure API for FHIR that provides the capability to ingest data from Internet of Medical Things (IoMT) devices.
* [Channle 9 Video: Remote Patient Monitoring with Internet of Medical Things (IoMT)](https://channel9.msdn.com/Shows/Internet-of-Things-Show/Remote-Patient-Monitoring-with-Internet-of-Medical-Things-IoMT) (Self Paced) (15 Minutes)
    * Learn more about how to enable scenarios like remote patient monitoring, home health and clinical trials with IoMT and open FHIR (Fast Healthcare Interoperability Resources) standard on Azure.


## Associate

* [Tutorial: Access Azure API for FHIR using Postman](https://docs.microsoft.com/en-us/azure/healthcare-apis/access-fhir-postman-tutorial) (Self Paced) (1 Hour)
    * In this tutorial, you will use Postman to access a FHIR service through REST APIs.
* [Tutorial: Deploy JavaScript app to read data from FHIR service](https://docs.microsoft.com/en-us/azure/healthcare-apis/tutorial-web-app-fhir-server) (Self Paced) (Self Paced) (3 Hours)
    * In this tutorial, you will deploy a small JavaScript app, which reads data from a FHIR service.
* [Tutorial: Receive device data through Azure IoT Hub](https://docs.microsoft.com/en-us/azure/healthcare-apis/device-data-through-iot-hub) (Self Paced) (2 Hours)
    * In this tutorial, you will connect and route device data from Azure IoT Hub to Azure IoT Connector for FHIR.
* [Tutorial: Azure Active Directory SMART on FHIR proxy](https://docs.microsoft.com/en-us/azure/healthcare-apis/use-smart-on-fhir-proxy) (Self Paced) (2 Hours)
    * In this tutorial, you will use the FHIR proxy to enable SMART on FHIR applications with the Azure API for FHIR.


## Expert

* [How to deploy a sandbox/demo environment by deploying FHIR server samples](https://github.com/microsoft/fhir-server-samples) (Self Paced) (4 Hours)
    * Example applications and scenarios that show use of the FHIR Server for Azure and the Azure API for FHIR.
* [How to deploy FHIR, IoMT and HL7v2 Ingest/Convert offerings in the Microsoft Health Architectures](https://github.com/microsoft/health-architectures#getting-started) (Self Paced) (8 Hours)
    * A collection of reference architectures illustrating end-to-end best practices for using the Azure API for FHIR and related technologies.
    * [Ingestion with FHIR](https://microsoft.github.io/health-architectures/Architectures-FHIR-Ingestion.html) to enrich, normalize and unify protected health information (PHI) from on-premise systems into and through Fast Healthcare Interoperability Resources (FHIR).
    * [IoMT FHIR Connector for Azure](https://microsoft.github.io/health-architectures/Architectures-IoMT-Connector.html) enables IoT devices seamless integration with FHIR services.
    * [IoMT Connector for Azure and Microsoft Power BI](https://microsoft.github.io/health-architectures/Architectures-IoMT-PowerBI.html) reference architecture shows the basic components of using Microsoft cloud services to enable Power BI on top of IoMT and FHIR data.
    * [Microsoft Cloud for Healthcare unlocks the power of Microsoft 365, Azure, Dynamics 365, and Power Platform](https://microsoft.github.io/health-architectures/Cloud4Health-Dynamics.html).  It provides trusted and integrated capabilities that deliver automation and efficiency on high-value workflows as well as deep data analysis functionality for both structured and unstructured data, that enable healthcare organizations to turn insight into action.
* [FHIR DevDays US 2020 Virtual Session: FHIR Analytics with Power BI](https://www.youtube.com/watch?v=AqFZTf_gVhU) (Self Paced) (45 Minutes)
    * This FHIR DevDays 2020 virtual session will discuss how you can use data in FHIR service to create analytics around it.  It will focus on how to build Power BI connectors for FHIR.
* [FHIR DevDays US 2020 (Virtual) contents from Michael Hansen](https://github.com/hansenms/FHIRDevDays-Virtual2020) (Self Paced) (Various)
    * This repo contains slides and artifacts for FHIR DevDays 2020 from Michael Hansen (Principal Program Manager, Microsoft Health Cloud and Data).

## Specialist

* [FHIR Powered Healthcare | What The Hack](https://microsoft.github.io/WhatTheHack/027-FHIRPoweredHealthcare/) (Self Paced) (3 Days)


## Certifications

* [HL7® FHIR® Certification](https://www.hl7.org/certification/fhir.cfm?ref=nav)


## Community

* [FHIR Community Forum](http://community.fhir.org/)
* [HL7 Community Events](https://www.hl7.org/events/index.cfm?showallevents&ref=nav)
* [HL7 FHIR Commmunity Events](http://www.hl7.org/FHIRCommunityEvents/)

