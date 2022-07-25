---
layout: page
title: 04 Implement Business Integration
permalink: /azure/iot/assets/04ImplementBusinessIntegration
tags: 
 - azure
 - iot
---

# AZ-220 Implement Business Integration (5-10%)

* [AZ-220: Microsoft Azure IoT Developer Exam](https://docs.microsoft.com/en-us/learn/certifications/exams/az-220)
* [Microsoft Certified: Azure IoT Developer Specialty](https://docs.microsoft.com/en-us/learn/certifications/azure-iot-developer-specialty)

The Microsoft Global Partner Solutions (GPS) Technical Team, IoT Product Group, IoT Advocates, and Microsoft Worldwide Learning have collaborated to create this guide to help you prepare for the Microsoft Azure IoT Developer exam!

## Skills Measured: Implement Business Integration

### [Integrate with upstream and downstream systems](https://docs.microsoft.com/azure/iot-fundamentals/iot-services-and-technologies?wt.mc_id=eventspg_16482_webpage_reactor) 

* [Set up input and output connections to support native Azure services and to enable third-party services](https://docs.microsoft.com/azure/event-grid/publish-iot-hub-events-to-logic-apps?wt.mc_id=eventspg_16482_webpage_reactor)
* [Set up IoT Hub routing to support downstream Azure resources](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-endpoints?wt.mc_id=eventspg_16482_webpage_reactor)

### [Develop an IoT solution that uses Azure Digital Twins](https://docs.microsoft.com/azure/digital-twins/?wt.mc_id=eventspg_16482_webpage_reactor)

* [Create models and digital twins](https://docs.microsoft.com/azure/digital-twins/concepts-models?wt.mc_id=eventspg_16482_webpage_reactor)
* [Map IoT device data to digital twin models and relationships](https://docs.microsoft.com/azure/digital-twins/concepts-twins-graph?wt.mc_id=eventspg_16482_webpage_reactor)
* [Ingest IoT device messages, and translate messages to digital twins](https://docs.microsoft.com/azure/digital-twins/how-to-ingest-iot-hub-data?wt.mc_id=eventspg_16482_webpage_reactor)
* [Configure routes and endpoints to trigger business logic and data processing](https://docs.microsoft.com/azure/digital-twins/concepts-route-events?wt.mc_id=eventspg_16482_webpage_reactor)
* [Manage and query the Azure Digital Twins graph](https://docs.microsoft.com/azure/digital-twins/concepts-query-language?wt.mc_id=eventspg_16482_webpage_reactor)
* [Update properties on Azure Digital Twins entities in the graph](https://docs.microsoft.com/azure/digital-twins/how-to-manage-graph?wt.mc_id=eventspg_16482_webpage_reactor)
* [Monitor and troubleshoot Azure Digital Twins](https://docs.microsoft.com/azure/digital-twins/how-to-monitor-diagnostics?wt.mc_id=eventspg_16482_webpage_reactor)

*NOTE: In most cases, exams do NOT cover preview features, and some features will only be added to an exam when they are GA (General Availability).*

## Microsoft Learn - Related Learning Paths

### [Develop Data Insights and Business Integrations](https://docs.microsoft.com/learn/paths/develop-data-insights-business-integrations?wt.mc_id=eventspg_16482_webpage_reactor) (5 Modules)

Learn about the tools and services that can be used to develop data insights and implement business integration, including Azure Event Grid, Azure Logic Apps, and Azure Time Series Insights.

### [Extend IoT Solutions by Using Azure Digital Twins](https://docs.microsoft.com/learn/paths/extend-iot-solutions-by-using-azure-digital-twins?wt.mc_id=eventspg_16482_webpage_reactor) (4 Modules)

Learn about the features and capabilities of Azure Digital Twins service, how to configure, build, and manage an Azure Digital Twins environment, and how to integrate IoT and Azure Digital Twins solutions.

## Quick Reference: Key Concepts and Terminology
* What is Azure Digital Twins?
  * Azure Digital Twins is a platform as a service (PaaS) offering for creating digital representations of real-world things, places, business processes, and people. 
  * Build twin graphs that represent entire environments using twin types called models
  * Use them to gain insights to drive better products, optimize operations and costs, and create breakthrough customer experiences. 
  * Models are defined in a JSON-like language called [Digital Twins Definition Language (DTDL)](https://github.com/Azure/opendigitaltwins-dtdl/blob/master/DTDL/v2/dtdlv2.md), and they describe twins in terms of their state properties, telemetry events, commands, components, and relationships.
  * Visualize your Azure Digital Twins graph in [Azure Digital Twins Explorer](https://docs.microsoft.com/en-us/azure/digital-twins/concepts-azure-digital-twins-explorer), which provides the following interface for interacting with your graph
  * Data in your Azure Digital Twins model can be [routed to downstream Azure services](https://docs.microsoft.com/en-us/azure/digital-twins/overview#output-to-adx-tsi-storage-and-analytics) for additional analytics or storage using event routes with [Event Hub](https://docs.microsoft.com/en-us/azure/event-hubs/event-hubs-about), [Event Grid](https://docs.microsoft.com/en-us/azure/event-grid/overview), or [Service Bus](https://docs.microsoft.com/en-us/azure/service-bus-messaging/service-bus-messaging-overview) to drive your desired data flows.
* A complete solution using Azure Digital Twins may contain the following parts:
  * The Azure Digital Twins service instance - Stores your twin models and your twin graph with its state, and orchestrates event processing.
  * One or more client apps that drive the Azure Digital Twins instance by configuring models, creating topology, and extracting insights from the twin graph.
  * One or more external compute resources to process events generated by Azure Digital Twins, or connected data sources such as devices. One common way to provide compute resources is via [Azure Functions](https://docs.microsoft.com/en-us/azure/azure-functions/functions-overview).
  * An IoT hub to provide device management and IoT data stream capabilities.
  * Downstream services to handle tasks such as workflow integration (like Logic Apps, cold storage, Azure Data Explorer, time series integration, or analytics).
* Elements of a Model - A DTDL model interface may contain zero, one, or many of each of the following fields:
  * *Property* - Properties are data fields that represent the state of an entity (like the properties in many object-oriented programming languages). Properties have backing storage and can be read at any time. For more information, see Properties and telemetry below.
  * *Telemetry* - Telemetry fields represent measurements or events, and are often used to describe device sensor readings. Unlike properties, telemetry is not stored on a digital twin; it is a series of time-bound data events that need to be handled as they occur. For more information, see Properties and telemetry below.
  * *Relationship* - Relationships let you represent how a digital twin can be involved with other digital twins. Relationships can represent different semantic meanings, such as contains ("floor contains room"), cools ("hvac cools room"), isBilledTo ("compressor is billed to user"), etc. Relationships allow the solution to provide a graph of interrelated entities. Relationships can also have properties of their own. For more information, see Relationships below.
  * *Component* - Components allow you to build your model interface as an assembly of other interfaces, if you want. An example of a component is a frontCamera interface (and another component interface backCamera) that are used in defining a model for a phone. You must first define an interface for frontCamera as though it were its own model, and then you can reference it when defining Phone. Use a component to describe something that is an integral part of your solution but doesn't need a separate identity, and doesn't need to be created, deleted, or rearranged in the twin graph independently. If you want entities to have independent existences in the twin graph, represent them as separate digital twins of different models, connected by relationships. 

## Other Helpful Resources

* [Azure Digital Twins Explorer](https://docs.microsoft.com/azure/digital-twins/concepts-azure-digital-twins-explorer?wt.mc_id=eventspg_16482_webpage_reactor)
* [Azure Digital Twins Data Ingress and Egress](https://docs.microsoft.com/azure/digital-twins/concepts-data-ingress-egress?wt.mc_id=eventspg_16482_webpage_reactor)
* [Azure Event Grid](https://docs.microsoft.com/azure/event-grid/overview?wt.mc_id=eventspg_16482_webpage_reactor)
* [Azure IoT Blogs](https://azure.microsoft.com/blog/topics/internet-of-things?wt.mc_id=eventspg_16482_webpage_reactor)
* [Azure IoT Hub Pricing](https://azure.microsoft.com/pricing/details/iot-hub/?wt.mc_id=eventspg_16482_webpage_reactor)
* [Azure IoT Reference Architecture](https://docs.microsoft.com/azure/architecture/reference-architectures/iot?wt.mc_id=eventspg_16482_webpage_reactor)
* [Comapre IoT Hub and Event Hubs](https://docs.microsoft.com/azure/iot-hub/iot-hub-compare-event-hubs?wt.mc_id=eventspg_16482_webpage_reactor)
* [Compare Message Routing and Event Grid for IoT Hub](https://docs.microsoft.com/azure/iot-hub/iot-hub-event-grid-routing-comparison?wt.mc_id=eventspg_16482_webpage_reactor)
* [Industrial IoT Patterns with IoT Central](https://docs.microsoft.com/azure/iot-central/core/concepts-iiot-architecture?wt.mc_id=eventspg_16482_webpage_reactor)
* [Microsoft Tech Community - IoT](https://techcommunity.microsoft.com/t5/internet-of-things-iot/ct-p/IoT?wt.mc_id=eventspg_16482_webpage_reactor) - Blogs and conversation spaces
* [Simplify Downstream Processing with Azure IoT Hub Message Enrichments](https://www.youtube.com/watch?v=nU1v5mqr_ig?wt.mc_id=eventspg_16482_webpage_reactor)
* [Use Workflows to Integrate Your IoT Central Application with Other Cloud Services](https://docs.microsoft.com/en-us/azure/iot-central/core/howto-configure-rules-advanced?wt.mc_id=eventspg_16482_webpage_reactor)
* [What is an Ontology?](https://docs.microsoft.com/azure/digital-twins/concepts-ontologies?wt.mc_id=eventspg_16482_webpage_reactor)
* [YouTube - Microsoft IoT Developers](https://www.youtube.com/channel/UCL7wy-iy_V76xxPnrIzGOZQ?wt.mc_id=eventspg_16482_webpage_reactor)

Happy studies!
