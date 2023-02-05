---
layout: page
title: 05 Process and Manage Data
permalink: /azure/iot/assets/05ProcessAndManageData
tags: 
 - azure
 - iot
---

# AZ-220 Process and Manage Data (15-20%)

* [AZ-220: Microsoft Azure IoT Developer Exam](https://docs.microsoft.com/en-us/learn/certifications/exams/az-220)
* [Microsoft Certified: Azure IoT Developer Specialty](https://docs.microsoft.com/en-us/learn/certifications/azure-iot-developer-specialty)

## Skills Measured: Process and Manage Data

### [Configure message routing in Azure IoT Hub](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-messages-d2c?wt.mc_id=eventspg_16482_webpage_reactor)

* [Implement message enrichment in IoT Hub](https://docs.microsoft.com/azure/iot-hub/iot-hub-message-enrichments-overview?wt.mc_id=eventspg_16482_webpage_reactor)
* [Implement routing of IoT device telemetry to endpoints](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-messages-d2c?wt.mc_id=eventspg_16482_webpage_reactor)
* [Implement routing of IoT Hub non-telemetry events to endpoints](https://docs.microsoft.com/azure/iot-hub/iot-hub-non-telemetry-event-schema?wt.mc_id=eventspg_16482_webpage_reactor)
* [Define and test routing queries](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-messages-d2c#testing-routes?wt.mc_id=eventspg_16482_webpage_reactor)
* [Configure IoT Hub as an Azure Event Grid source](https://docs.microsoft.com/azure/iot-hub/iot-hub-event-grid?wt.mc_id=eventspg_16482_webpage_reactor)
* [Reconfigure the default Azure Event Hubs endpoint when there are multiple endpoints](https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-endpoints?wt.mc_id=eventspg_16482_webpage_reactor)

### [Configure stream processing of IoT data ](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-get-started-with-azure-stream-analytics-to-process-data-from-iot-devices?wt.mc_id=eventspg_16482_webpage_reactor)

* [Create Azure Stream Analytics for data, and stream processing by using the Azure portal](https://docs.microsoft.com/azure/stream-analytics/?wt.mc_id=eventspg_16482_webpage_reactor)
* [Process and filter IoT data by using Azure Functions](https://docs.microsoft.com/azure/azure-functions/functions-bindings-event-iot-output?wt.mc_id=eventspg_16482_webpage_reactor)
* [Write user-defined functions and aggregations in Stream Analytics](https://docs.microsoft.com/azure/stream-analytics/functions-overview?wt.mc_id=eventspg_16482_webpage_reactor)
* [Consume Azure Machine Learning functions in Stream Analytics](https://docs.microsoft.com/azure/stream-analytics/machine-learning-udf?wt.mc_id=eventspg_16482_webpage_reactor)
* [Configure Stream Analytics outputs](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-define-outputs?wt.mc_id=eventspg_16482_webpage_reactor)

### [Create Azure Stream Analytics queries](https://docs.microsoft.com/stream-analytics-query/stream-analytics-query-language-reference?wt.mc_id=eventspg_16482_webpage_reactor)

* [Write a Stream Analytics query that runs in IoT Edge](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-edge?wt.mc_id=eventspg_16482_webpage_reactor)
* [Write a Stream Analytics query that runs in the cloud](https://docs.microsoft.com/azure/stream-analytics/stream-analytics-stream-analytics-query-patterns?wt.mc_id=eventspg_16482_webpage_reactor)

### [Process real-time data by using Azure Time Series Insights](https://docs.microsoft.com/azure/time-series-insights/?wt.mc_id=eventspg_16482_webpage_reactor)
*Though Time Series Insights has been deprecated, it is still on this exam for now. It will be removed with a future exam revision.*

* [Create a Time Series Insights environment](https://docs.microsoft.com/azure/time-series-insights/tutorials-set-up-tsi-environment#create-an-azure-time-series-insights-gen2-environment?wt.mc_id=eventspg_16482_webpage_reactor)
* [Connect the IoT hub and the Time Series Insights environment](https://docs.microsoft.com/azure/time-series-insights/how-to-ingest-data-iot-hub?wt.mc_id=eventspg_16482_webpage_reactor)
* [Create a reference data set for a Time Series Insights environment by using the Azure portal](https://docs.microsoft.com/azure/time-series-insights/time-series-insights-add-reference-data-set?wt.mc_id=eventspg_16482_webpage_reactor)
* [Implement Time Series Model hierarchies, types, and instance fields](https://docs.microsoft.com/azure/time-series-insights/concepts-model-overview#time-series-model-hierarchies?wt.mc_id=eventspg_16482_webpage_reactor)
* [Consume data by using Time Series Expression syntax](https://docs.microsoft.com/rest/api/time-series-insights/reference-time-series-expression-syntax?wt.mc_id=eventspg_16482_webpage_reactor)

*NOTE: In most cases, exams do NOT cover preview features, and some features will only be added to an exam when they are GA (General Availability).*

## Microsoft Learn - Related Learning Paths

### [Implement device message processing and data analytics](https://docs.microsoft.com/learn/paths/implement-device-message-processing-data-analytics?wt.mc_id=eventspg_16482_webpage_reactor) (5 Modules)

Learn about the message processing and data analytics capabilities that must be implemented within your Azure IoT solution, and the storage options that are often configured as part of your solution.

## Quick Reference: Key Concepts and Terminology
* Event Concepts:
  * *Events* - What happened
  * *Event sources* - Where the event took place
  * *Topics* - The endpoint where publishers send events
  * *Event subscriptions* - The endpoint or built-in mechanism to route events, sometimes to more than one handler. Subscriptions are also used by handlers to intelligently filter incoming events
  * *Event handlers* - The app or service reacting to the event

* Key Features of Azure Event Grid:
  * *Simplicity* - Point and click to aim events from your Azure resource to any event handler or endpoint
  * *Advanced filtering* - Filter on event type or event publish path to make sure event handlers only receive relevant events
  * *Fan-out* - Subscribe several endpoints to the same event to send copies of the event to as many places as needed
  * *Reliability* - 24-hour retry with exponential backoff to make sure events are delivered
  * *Pay-per-event* - Pay only for the amount you use Event Grid
  * *High throughput* - Build high-volume workloads on Event Grid with support for millions of events per second
  * *Built-in Events* - Get up and running quickly with resource-defined built-in events
  * *Custom Events* - Use Event Grid route, filter, and reliably deliver custom events in your app

* Message Routing or Event Grid: How to Choose
  * What kind of data are you sending to the endpoints?
    * IoT Hub message routing to send telemetry data to other services
    * The IoT Hub integration with Event Grid works with events that occur in the IoT Hub service
  * What endpoints need to receive this information?
    * IoT Hub message routing supports limited number of unique endpoints and endpoint types, but you can build connectors to reroute the data and events to additional endpoints
    * The IoT Hub integration with Event Grid supports a larger variety of endpoint types
  * Does it matter if your data arrives in order?
    * IoT Hub message routing maintains the order in which messages are sent
    * Event Grid does not guarantee that endpoints will receive events in the same order that they occurred

* Azure Stream Analytics (ASA) Data Flow
  * A *job* consists of an input, query, and an output
  * *Input* – ASA can ingest data from Azure Event Hubs, Azure IoT Hub, or Azure Blob Storage
  * *Query* – ASA uses a SQL-like query language that includes support for filtering, sorting, aggregating, joining, and user-defined functions
  * *Output* – ASA can output to many targets
  
* ASA input types
  * *Data stream input* – an unbounded sequence of events over time
  * *Reference data input* – static (or slowly changing) data used for lookups and correlation

* ASA output types
  * *Azure Data Lake Storage Gen1* - Enterprise-wide, hyperscale repository for big data analytic workloads. You can use Data Lake Storage to store data of any size, type, and ingestion speed for operational and exploratory analytics. 
  * *Azure SQL Database* - Output for data that's relational in nature or for applications that depend on content being hosted in a relational database. Stream Analytics jobs write to an existing table in SQL Database. The table schema must exactly match the fields and their types in your job's output. You can also specify Azure SQL Data Warehouse as an output via the SQL Database output option.
  * *Blob storage with Data Lake Storage Gen2* - Designed to service multiple petabytes of information while sustaining hundreds of gigabits of throughput, Data Lake Storage Gen2 allows you to easily manage massive amounts of data with a hierarchical namespace.
  * *Azure Event Hubs* - Highly scalable publish-subscribe event ingestor, can collect millions of events per second. One use of an event hub as output is when the output of a Stream Analytics job becomes the input of another streaming job.
  * *Power BI* - Output for a Stream Analytics job provides a rich visualization experience of analysis results. You can use this capability for operational dashboards, report generation, and metric-driven reporting.
  * *Azure Table* storage - Offers highly available, massively scalable storage, so that an application can automatically scale to meet user demand. Table storage is Microsoft's NoSQL key/attribute store, which you can use for structured data with fewer constraints on the schema. Azure Table storage can be used to store data for persistence and efficient retrieval.
  * *Service Bus queues* - Offer a FIFO message delivery to one or more competing consumers. Typically, messages are received and processed by the receivers in the temporal order in which they were added to the queue. Each message is received and processed by only one message consumer (one-to-one communication method from sender to receiver).
  * *Service Bus topics* - Provide a one-to-many form of communication.
  * *Azure Cosmos DB* - Globally distributed database service that offers limitless elastic scale around the globe, rich query, and automatic indexing over schema-agnostic data models.
  * *Azure Functions* - Serverless compute service that you can use to run code on-demand without having to explicitly provision or manage infrastructure. It lets you implement code that's triggered by events occurring in Azure or partner services, making it a natural output for Azure Stream Analytics. This output adapter enables users to connect Stream Analytics to Azure Functions to run a script or piece of code in response to a variety of events.

* ASA and other Streaming Technologies
  * When to use Azure Stream Analytics
    * Recommended tool for analytics on Azure
    * Dashboards for data visualization
    * Real-time alerts from temporal and spatial patterns or anomalies
    * Basic Extract, Transform, and Load (ETL) work
  * When to use other technologies
    * Apache Kafka connectivity (Azure Event Hubs are a good choice here)
    * In-line query handling in a language besides C# or JavaScript (e. g. Java; Spark Structured Streaming or specialized Azure Event Hubs implementation are good choices here)
    * Multi-cloud support (Azure Stream Analytics is Azure-specific; Spark Structured Streaming, Storm, etc. will work here)

* Why use Time Series Insights?
  * Time Series Insights gives a business the ability to examine historical data over long periods of time, including:
  * Discovery of data
  * Trending of data over time
  * Anomaly detection over time with basic machine learning

## Other Helpful Resources

* [Azure IoT Blogs](https://azure.microsoft.com/blog/topics/internet-of-things/?wt.mc_id=eventspg_16482_webpage_reactor)
* [Azure IoT Central Data Integration Guide](https://docs.microsoft.com/azure/iot-central/core/overview-iot-central-solution-builder?wt.mc_id=eventspg_16482_webpage_reactor)
* [Azure IoT Reference Architecture](https://docs.microsoft.com/azure/architecture/reference-architectures/iot?wt.mc_id=eventspg_16482_webpage_reactor)
* [Export IoT Central Data to Azure Blob Storage](https://docs.microsoft.com/azure/iot-central/core/howto-export-to-blob-storage?wt.mc_id=eventspg_16482_webpage_reactor)
* [Export IoT Central Data to Azure Data Explorer](https://docs.microsoft.com/azure/iot-central/core/howto-export-to-azure-data-explorer?wt.mc_id=eventspg_16482_webpage_reactor)
* [Export IoT Central Data to Azure Event Hubs](https://docs.microsoft.com/azure/iot-central/core/howto-export-to-event-hubs?wt.mc_id=eventspg_16482_webpage_reactor)
* [Export IoT Central Data to Azure Service Bus](https://docs.microsoft.com/azure/iot-central/core/howto-export-to-service-bus?wt.mc_id=eventspg_16482_webpage_reactor)
* [Microsoft Tech Community - IoT](https://techcommunity.microsoft.com/t5/internet-of-things-iot/ct-p/IoT?wt.mc_id=eventspg_16482_webpage_reactor) - Blogs and conversation spaces
* [Transform Data Externally for IoT Central](https://docs.microsoft.com/azure/iot-central/core/howto-transform-data?wt.mc_id=eventspg_16482_webpage_reactor)
* [Transform Data Internally for IoT Central](https://docs.microsoft.com/azure/iot-central/core/howto-transform-data-internally?wt.mc_id=eventspg_16482_webpage_reactor)
* [YouTube - Microsoft IoT Developers](https://www.youtube.com/channel/UCL7wy-iy_V76xxPnrIzGOZQ?wt.mc_id=eventspg_16482_webpage_reactor)

Happy studies!
