---
layout: page
title: AI & ML Academy - Azure OpenAI
sorttitle: 02
description: Workshop focused on AI and ML - Azure OpenAI
permalink: /skilling/ai-ml-academy/openai
updated: 2024-03-25
showbreadcrumb: true
tags: 
- azure
- data, analytics, and ai
- artificial intelligence
- machine learning
- academy content
- ai & ml academy module
- ai & ml academy
- openai
---

# AI & ML Academy - Azure OpenAI

Welcome to the AI & ML Academy (AIA) - Azure OpenAI!

This section includes Azure OpenAI resources to help you get started including sample code, end-to-end scenarios, notebooks, and other QuickStart resources.

### Also explore our [Learning Path Resources for Azure OpenAI](https://microsoft.github.io/PartnerResources/skilling/ai-ml-academy/resources/openai)!📖

<!--
```html
<!DOCTYPE html>
<html>
  <style>
    body {
        block {
      display: inline-block;
      width: 200px;
      height: 200px;
      background-color: lightgray;
        }
      container  {
  text-align: center;
    }
      th {
        text-align: left;
      }
    }
  </style>
  <body>
    <pre>
      <div class="container">
          <div class="block"></div>
          <div class="block"></div>
          <div class="block"></div>
          <div class="block"></div>
      </div>
    </pre>
  </body>
</html>

```
-->

We’ll start by covering the Prompt Engineering Techniques, which is the first step to LLM behavior and interactions

## Prompt Engineering Techniques

1. **System Message: Setting the Stage**

The System Message acts as the opening act for our AI model. It sets the tone and context. Consider this example:

- System Message: “You’re an AI assistant that helps people find information and responds in rhyme.”
- When a user asks, “What’s the capital of France?” our AI responds with: 
  - “In Paris, the Seine does dance, where croissants and baguettes enhance.”

Remember, the System Message shapes the AI’s behavior. Experiment with different prompts to fine-tune your model’s personality.

2. **Basic Best Practices for Prompting**

When crafting prompts, follow these best practices:

	1. Put Instructions at the Beginning:
		- Clearly state what you want the model to do.
		
		Example: Summarize the following text, highlighting the main point.
		Text: """
		{input}
		"""
		
	2. Be Explicit:
		- Specify the desired format or output.
		- Example: “Summarize the article in 3 sentences, highlighting the key figures.”
		
	3. Avoid Negations:
		- Instead of saying what not to do, focus on positive instructions.
		- Example: “Provide a concise summary” (instead of “Don’t be verbose”).
		
	4. Use Examples:
		- Show the model what you expect.
		- Example: “Translate the following: ‘Bonjour’” (with the expected output: “Hello”).
		
	5. Iterate and Experiment:
		- Fine-tune prompts based on model responses.
		- Observe how different instructions impact results.

3. **Zero-Shot Prompting**

- Definition: 
  - Zero-shot prompting tests the model’s ability to produce relevant outputs without relying on prior examples.
  - You provide a prompt that is not part of the training data, and the model generates a result given your instructions.
  
- Example: 
  - Imagine asking the model: “Translate the following English text to Spanish: ‘Good morning!’”
  - The model responds with: “¡Buenos días!”

4. **Few-Shot Prompting (In-Context Learning)**

- Definition: 
  - Few-shot prompting gives the model a few sample outputs (shots) to help it learn what the user wants.
  - By providing context, the learning model better understands the desired output.
  
- Example: 
  - Extract keywords from the corresponding texts below.
  
  1. Azure OpenAI and Language Models
	  - Text: “Azure OpenAI offers powerful language models that excel at understanding and generating text. Our API provides seamless access to these models, enabling developers to tackle a wide range of language-related tasks.”
	  - Keywords: Azure OpenAI, language models, text generation, API
	  
  2. Integration with Web Applications
	  - Text: “Integrating Azure OpenAI into web applications is straightforward. Developers can leverage our APIs to enhance natural language understanding, sentiment analysis, and chatbot interactions.”
	  - Keywords: Azure OpenAI, web applications, APIs, natural language understanding, sentiment analysis, chatbots
	  
  3. Custom Text (User-Specified)
	  - Text: {text}
	  - Keywords: 
	  
	  The model learns from these examples and responds similarly.

5. **Chain-of-Thought (CoT) Prompting**

- Definition: 
  - CoT prompting encourages reasoning and multi-step thinking.
  - A few sample questions and answers, followed by the actual question (Few-Shot prompt), for the model can help it generate reasoning to respond to the prompt. 
  
- Example: 
  - “Let’s think step-by-step: Roger started with 5 balls. 2 cans of 3 tennis balls each is 6 tennis balls. 5 + 6 = ?”
  - Generated Response: “Roger started with 5 balls. Adding the 6 tennis balls from the cans, he now has 11 balls.”

6. **Parameters**

	1. Model- Based on what model is used, you may expect different results and latency. For example, GPT 3.5 turbo will return faster than a GPT-4 model, but GPT-4 has better reasoning, so the resulting text could be better in more complex scenarios. The **[Azure AI studio](https://ai.azure.com/)** and **[Hugging Face](https://huggingface.co/collections/open-llm-leaderboard/the-big-benchmarks-collection-64faca6335a7fc7d4ffe974a)** have benchmarking to show the difference between performances for certain tasks.
	
	2. Temperature & Top_p- These metrics can determine how varied the response will be. The metrics can be a number between 0 to 1, with the closer the temperature is set 1 the more creative/random, and with it set to 0 more grounded and great for use cases where factual data is needed. Both Temperature and Top_p are similar in the fact that they control randomness, but they do it in a different way. The general recommendation is to alter only one out of the pair.

7. **Grounding**

	1. The best way to get reliable answers is by providing your model context. For example, if you were to ask a question like, "Who is responsible to project A on my team?", the model would have no idea on how to answer that. Provided context "Sally is in charge of project A, Sam for project B, and Steve for project C", the model is able to respond back with an answer grounded by this context.


## Getting Started
Start here for an introduction to programmatically utilizing GPT models.

<table>
    <tbody>
        <tr>
            <th>Name</th>
            <th>Description</th>
        </tr>
        <tr>
            <td><a href="https://github.com/Azure/azure-openai-samples/tree/main/quick_start">QuickStart</a></td>
            <td>A collection of notebooks where you can quickly start with using GPT (such as creating resources, code generation, prompt engineering, LLM chain demo)</td>
        </tr>
    </tbody>
</table>


## Demo-ready Resources
Below is a table of official Azure OpenAI Accelerators and workshops from the [OpenAI
Accelerators and Demo Assets repository](https://github.com/Azure/ai-solution-accelerators-list/blob/main/OpenAIDemos/README.md).

<table>
    <tbody>
        <tr>
            <th>Name</th>
            <th>Description</th>
        </tr>
        <tr>
            <td>
                <a href="https://github.com/Azure/azure-openai-samples">Azure OpenAI Samples</a>
            </td>
            <td>Resources to help you understand how to use GPT (Generative Pre-trained Transformer) offered by Azure OpenAI at the fundamental level, explore sample end-to-end solutions, and learn about various use cases.</td>
        </tr>
        <tr>
            <td>
                <a href="https://github.com/microsoft/OpenAIWorkshop">Azure OpenAI Workshop</a>
            </td>
            <td>In this workshop, you will learn how to use the Azure OpenAI service to create AI powered solutions. You will get hands-on experience with the latest AI technologies and will learn how to use Azure OpenAI API.</td>
        </tr>
        <tr>
            <td>
                <a href="https://github.com/microsoft/semantic-kernel">Semantic Kernel</a>
            </td>
            <td>
                Semantic Kernel (SK) is a lightweight SDK enabling integration of AI Large Language Models (LLMs) with conventional programming languages.
            </td>
        </tr>
        <tr>
            <td>
                <a href="https://github.com/microsoft/visual-chatgpt">Visual ChatGPT</a>
            </td>
            <td>
                Visual ChatGPT connects ChatGPT and a series of Visual Foundation Models to enable sending and receiving images during chatting.
            </td>
        </tr>
    </tbody>
</table>


## Notebooks
Examples of applications applied to various industries in complete Jupyter Notebook format in conjunction with additional Azure services.

<table>
    <tbody>
        <tr>
            <th>Name</th>
            <th>Application</th>
            <th>Description</th>
            <th>Components</th>
        </tr>
        <tr>
            <td><a href="https://github.com/jakeatmsft/AzureOpenAIExamples/blob/main/Examples/FormRecognizer/Balance_sheet_analysis.ipynb">Income Statement Analysis </a></td>
            <td>Text/Code generation</td>
            <td>• Read a table into a Pandas DataFrame and generate code to analyze insights<br>
                • Generate 2-3 tag lines based on the podcast content.<br>
            </td>
            <td>• Davinci-002<br>• Form Recognizer</td>
        </tr>
        <tr>
            <td><a href="https://github.com/jakeatmsft/AzureOpenAIExamples/blob/main/Examples/FormRecognizer/FormRecognizerExamples.ipynb">Form Recognizer Examples</a></td>
            <td>Text generation</td>
            <td>• Validate format of text extracted from Form Recognizer<br> 
                • Correct formats of text
            </td>
            <td>• Form Recognizer</td>
        </tr>
        <tr>
            <td><a href="https://github.com/jakeatmsft/AzureOpenAIExamples/blob/main/Examples/Language/CustomerServiceCall.ipynb">Customer Service Call</a></td>
            <td>Summarization, Text generation</td>
            <td>• Summarize call<br>
                • Generate list of follow up tasks<br>
            </td>
            <td>• Cognitive Services Language</td>
        </tr>
        <tr>
            <td><a href="https://github.com/jakeatmsft/AzureOpenAIExamples/blob/main/Examples/Language/Loan_call.ipynb">Loan Call</a></td>
            <td>Summarization, Text generation</td>
            <td>• Identify and extract PII<br>
                • OpenAI validates whether extracted text is PII or normal conversation<br>
                • Summarize call<br>
                • Generate list of follow up tasks<br>
            </td>
            <td>• Cognitive Services Language</td>
        </tr>
        <tr>
            <td><a href="https://github.com/jakeatmsft/AzureOpenAIExamples/blob/main/Examples/Language/Pharmacy_call.ipynb">Pharmacy Call</a></td>
            <td>Summarization, Text generation</td>
            <td>• Summarize call<br>
                • Provide list of medications, dose, and form discussed in the call<br>
            </td>
            <td>• Cognitive Services Language</td>
        </tr>
        <tr>
            <td><a href="https://github.com/jakeatmsft/AzureOpenAIExamples/blob/main/Examples/Speech/Conversation_SSML%20OpenAI.ipynb">Conversation SSML</a></td>
            <td>Summarization, Text generation</td>
            <td>• Summarize call from audio file<br>
                • List call participants<br>
                • Generate list of follow up tasks<br>
                • Extract components of conversation from transcript based on keys ("reason," "cause," caller")<br>
            </td>
            <td>• Cognitive Services Language</td>
        </tr>
    </tbody>
</table>


## End-to-end Solutions
A collection of solution accelerators (repositories) that show you how to create a robust, end-to-end Azure solution that leverages OpenAI.

<table>
    <tbody>
        <tr>
            <th>Name</th>
            <th>Application</th>
            <th>Description</th>
            <th>Components</th>
        </tr>
        <tr>
            <td>
                <a href="https://github.com/Azure/business-process-automation">Business Process Automation</a>
            </td>
            <td>Summarization, Search</td>
            <td>Creates pipelines to analyze text and audio datasets, across multiple cognitive services, and the Hugging Face library. The accelerator deploys all of the resources, and transforms the input data at each step, allowing multiple Cognitive Services to be called and deployed within a single, end-to-end pipeline. Includes capabilities like Azure OpenAI (summarization or custom prompts) and integration with CosmosDB, Cognitive Search, and RediSearch for Vector Search</td>
            <td>
                • Cognitive Services (Speech, Language, Form Recognizer, Read API)<br>
                • Cognitive Search<br>
                • Azure Machine Learning<br>
                • CosmosDB<br>
            </td>
        </tr>
        <tr>
            <td>
                <a href="https://github.com/Azure-Samples/azure-search-openai-demo/">ChatGPT + Enterprise data with Azure OpenAI and Cognitive Search</a>
            </td>
            <td>Search</td>
            <td>This sample demonstrates a few approaches for creating ChatGPT-like experiences over your own data using the Retrieval Augmented Generation pattern. It uses Azure OpenAI Service to access the ChatGPT model (gpt-35-turbo), and Azure Cognitive Search for data indexing and retrieval. <b>NOTE: sample created by Product Group</b></td>
            <td>
                • GPT/ChatGPT<br>
                • App UX<br>
                • App Server<br>
                • Azure SQL<br>
                • Azure Cosmos DB<br>
            </td>
        </tr>
        <tr>
            <td>
                <a href="https://github.com/pablomarin/GPT-Azure-Search-Engine">Accelerator powered by Azure Cognitive Search + Azure OpenAI</a>
            </td>
            <td>Search</td>
            <td>The goal of the MVP workshop is to show/prove the value of a Smart Search Engine built with the Azure Services, with your own data in your own environment. This repository comes with a PPT deck for a client 2-day workshop.
</td>
            <td>
                • Cognitive Search<br>
                • Cognitive Services (Text Analytics, Translator, Computer Vision)<br>
                • OpenAI Embedding and Completion models<br>
                • Cosmos DB<br>
                • LangChain<br>
                • Web App
            </td>
        </tr>
        <tr>
            <td>
                <a href="https://github.com/Azure-Samples/summarization-python-openai">Summarization Python OpenAI</a>
            </td>
            <td>Search, Summarization</td>
            <td>E2E ready to deploy solution architecture combining Cognitive (Enterprise) Search with OpenAI in a Python Notebook to search for relevant information and then to summarize the content to present to the user in a concise and succinct manner.
            </td>
            <td>
                • Blob Storage<br>
                • Cognitive Search<br>
                • OpenAI Embedding and Completion models (GPT-3)
            </td>
        </tr><tr>
            <td>
                <a href="https://github.com/MSUSAzureAccelerators/Knowledge-Mining-with-OpenAI">Knowledge Mining with Azure OpenAI</a>
            </td>
            <td>Search</td>
            <td>The purpose of this repo is to accelerate the deployment of a Python-based Knowledge Mining solution with OpenAI that will ingest a Knowledge Base, generate embeddings using the contents extracted, store them in a vector search engine (Redis), and use that engine to answer queries / questions specific to that Knowledge Base.
</td>
            <td>
                • Includes a Cognitive Search component and Power Virtual agent bot using ChatGPT<br>
                • Form Recognizer<br>
                • Event Grid<br>
                • Cognitive Search<br>
                • Azure Function<br>
                • Cosmos DB<br>
                • Service Bus<br>
                • Cognitive Services<br>
                • Translator<br>
                • Redis
            </td>
        </tr><tr>
            <td>
                <a href="https://github.com/openai/chatgpt-retrieval-plugin">ChatGPT Retrieval Plugin</a>
            </td>
            <td>Search</td>
            <td>The ChatGPT Retrieval Plugin repository provides a flexible solution for semantic search and retrieval of personal or organizational documents using natural language queries. Includes examples and documentation for usage.
            </td>
            <td>
                • ChatGPT<br>
            </td>
        </tr><tr>
            <td>
                <a href="https://github.com/microsoft/OpenAIWorkshop/tree/main/scenarios/powerapp_and_python">Build your first AOAI application with PowerApps</a>
            </td>
            <td>Summarization, Text Generation, Search</td>
            <td>Submit prompts to OpenAI from Power App using the OpenAI Python SDK. </td>
            <td>
                • Power App<br>
                • LangChain<br>
                • Azure OpenAI Embeddings API
            </td>
        </tr>
        <tr>
            <td>
                <a href="https://github.com/microsoft/OpenAIWorkshop/tree/main/scenarios/natural_language_query">A natural language query application on SQL data</a> (Advanced)
            </td>
            <td>Code/Text Generation</td>
            <td>This scenario allows users to use Open AI as an intelligent agent to get business questions prompts from end users and generating SQL queries from the prompts. This implementation scenario focuses on building a Natural Language to query from business questions and generate the queries for database retrieval</td>
            <td>
                • Power App<br>
                • Azure Function<br>
                • Azure SQL
            </td>
        </tr><tr>
            <td>
                <a href="https://github.com/microsoft/OpenAIWorkshop/tree/main/scenarios/openai_batch_pipeline">Build an Open AI Pipeline to Ingest Batch Data, Perform Intelligent Operations, and Analyze in Synapse</a> (Advanced)
            </td>
            <td>Summarization, Search</td>
            <td>This scenario allows OpenAI to summarize and analyze customer service call logs for the fictitious company, Contoso. The data is ingested into a blob storage account, and then processed by an Azure Function. The Azure Function will return the customer sentiment, product offering the conversation was about, the topic of the call, as well as a summary of the call. These results are written into a separate designated location in the Blob Storage. From there, Synapse Analytics is utilized to pull in the newly cleansed data to create a table that can be queried in order to derive further insights.</td>
            <td>
                • Synapse Analytics<br>
                • Blob Storage<br>
                • Azure Function
            </td>
        </tr>
        <tr>
            <td>
                <a href="https://github.com/microsoft/OpenAIWorkshop/tree/main/scenarios/openai_on_custom_dataset">Using Azure OpenAI on custom dataset</a> (Advanced)
            </td>
            <td>Q&A, Search, Text Generation</td>
            <td>This scenario allows use cases to use Open AI as an intelligent agent to answer questions from end users or assist them using knowledge of a proprietary corpus and domain for a variety of applications</td>
            <td>
                • Power App<br>
                • Form Recognizer<br>
                • Azure Cognitive Search<br>
                • Azure Function
            </td>
        </tr>
    </tbody>
</table>