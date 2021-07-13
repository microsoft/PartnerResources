# AZ-220 Process and Manage Data (15-20%)

* [AZ-220: Microsoft Azure IoT Developer Exam](https://docs.microsoft.com/en-us/learn/certifications/exams/az-220)
* [Microsoft Certified: Azure IoT Developer Specialty](https://docs.microsoft.com/en-us/learn/certifications/azure-iot-developer-specialty)
* [Microsoft Tech Community "Learn IoT" Conversation Space](https://aka.ms/iottechcommunity/learniot) - Where you can discuss IoT learning resources and homework questions 

## Skills Measured:
### Configure routing in Azure IoT Hub
* Implement message enrichment in IoT Hub
* Configure routing of IoT Device messages to endpoints
* Define and test routing queries
* Integrate with Event Grid

### Configure stream processing
* Create Azure Stream Analytics (ASA) for data and stream processing of IoT data
* Process and filter IoT data by using Azure Functions
* Configure Stream Analytics outputs

### Configure an IoT solution for Time Series Insights (TSI)
* Implement solutions to handle telemetry and time-stamped data
* Create an Azure Time Series Insights (TSI) environment
* Connect the IoT Hub and the Time Series Insights (TSI)

## Homework:
### [AZ-220 IoT Labs](https://microsoftlearning.github.io/AZ-220-Microsoft-Azure-IoT-Developer) 
* Module 4: Message Processing and Analytics
  * [Lab 07: Device Message Routing](https://microsoftlearning.github.io/AZ-220-Microsoft-Azure-IoT-Developer/Instructions/Labs/LAB_AK_07-analyze-message-data-in-real-time.html)
  <br />Exercise 1: Verify Lab Prerequisites
  <br />Exercise 2: Write Code for Vibration Telemetry
  <br />Exercise 3: Create a Message Route to Azure Blob Storage
  <br />Exercise 4: Logging Route Azure Stream Analytics Job

* Module 5: Insights and Business Integration
  * [Lab 08: Visualize a Data Stream in Power BI](https://microsoftlearning.github.io/AZ-220-Microsoft-Azure-IoT-Developer/Instructions/Labs/LAB_AK_08-visualize-data-stream-in-power-bi.html)
  <br />Make a Call to a Built-in Machine Learning Model
  <br />Visualize data using Power BI
  <br />Exercise 1: Sign Up For Power BI
  <br />Exercise 2: Verify Lab Prerequisites
  <br />Exercise 3: Create an Azure Event Hubs service
  <br />Exercise 4: Create Real-Time Message Route
  <br />Exercise 5: Add Telemetry Route
  <br />Exercise 6: Create a Power BI Dashboard

  * [Lab 09: Integrate IoT Hub with Event Grid](https://microsoftlearning.github.io/AZ-220-Microsoft-Azure-IoT-Developer/Instructions/Labs/LAB_AK_09-iot-hub-integration-with-azure-event-grid.html)
  <br />Exercise 1: Verify Lab Prerequisites
  <br />Exercise 2: Create HTTP Web Hook Logic App that sends an email
  <br />Exercise 3: Configure Azure IoT Hub Event Subscription
  <br />Exercise 4: Test Your Logic App with New Devices

  * [Lab 10: Explore and analyze time stamped data with Time Series Insights](https://microsoftlearning.github.io/AZ-220-Microsoft-Azure-IoT-Developer/Instructions/Labs/LAB_AK_10-analyze-time-stamped-data-with-time-series-insights.html)
  <br />Exercise 1: Verify Lab Prerequisites
  <br />Exercise 2: Setup Time Series Insights
  <br />Exercise 3: Run Simulated IoT Devices
  <br />Exercise 4: View Time Series Insights Explorer

### Sign up for [Online Workshop Series: Build End-to-End IoT Solutions](https://aka.ms/IoT-online-workshop)
* Messaging processing, analytics, and business integration – May 7 (on-demand)

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

## Resources
* [IoT Technical Community](https://techcommunity.microsoft.com/t5/internet-of-things-iot/ct-p/IoT)
* [Microsoft Learn IoT Learning Paths](http://aka.ms/mslearniot)
* [Azure IoT Reference Architecture Guide](https://docs.Microsoft.com/azure/architecture/reference-architectures/iot)
* [Message Enrichments for D2C IoT Hub messages](https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview)
* [Tutorial: Message Enrichments](https://docs.microsoft.com/en-us/azure/iot-hub/tutorial-message-enrichments)
* [IoT Hub Metrics](https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-metrics)
* [Azure Stream Analytics (ASA) Documentation](https://docs.microsoft.com/en-us/azure/stream-analytics/)
* [Stream Analytics Query Patterns](https://docs.microsoft.com/en-us/azure/stream-analytics/stream-analytics-stream-analytics-query-patterns)
* [Stream Analytics Window Functions](https://docs.microsoft.com/en-us/azure/stream-analytics/stream-analytics-window-functions)
* [Stream Analytics Query Language Reference](https://docs.microsoft.com/en-us/stream-analytics-query/stream-analytics-query-language-reference?toc=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fazure%2Fstream-analytics%2Ftoc.json&bc=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fazure%2Fbread%2Ftoc.json)
* [Stream Analytics Outputs](https://docs.microsoft.com/en-us/azure/stream-analytics/stream-analytics-define-outputs)
* [Stream Analytics Solution Patterns](https://docs.microsoft.com/en-us/azure/stream-analytics/stream-analytics-solution-patterns)
* [Azure Functions](https://docs.microsoft.com/en-us/azure/azure-functions/functions-overview)
* [Run Azure Functions from Azure Stream Analytics jobs](https://docs.microsoft.com/en-us/azure/stream-analytics/stream-analytics-with-azure-functions)
* [Time Series Insights (TSI) Product Page](https://azure.microsoft.com/en-us/services/time-series-insights)
* [Time Series Insights Documentation](https://docs.microsoft.com/en-us/azure/time-series-insights/time-series-insights-update-overview)
* [Tutorial: Time Series Insights](https://docs.microsoft.com/en-us/azure/time-series-insights/tutorial-create-populate-tsi-environment)
* [Create IoT Hub and Device to Cloud Consumer Group](https://github.com/Azure/azure-quickstart-templates/tree/master/101-iothub-with-consumergroup-create)

NOTE: In most cases, exams do NOT cover preview features, and some features will only be
added to an exam when they are GA (General Availability).
