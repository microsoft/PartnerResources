---
layout: page
title: AI & ML Academy - Customizable AI Models
sorttitle: 01
description: Customizable AI Models
permalink: /skilling/ai-ml-academy/prebuilt-ai
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
- customizable ai models
---

# AI & ML Academy - Customizable AI Models

Welcome to the AI & ML Academy (AIA) - Customizable AI Models!

In this section, we will go through an overview of AI Customizable AI Models and what services reside within each. There is also a level of customization that can be achieved in each of these pillars through services like Custom Vision and Custom Speech that we will introduce. Finally, we provide some best practices for each of these services.

## AI Services

Azure AI Services are cloud-based artificial intelligence (AI) services that help you build cognitive intelligence into your applications. They are available as REST APIs, client library SDKs, and user interfaces. You can add cognitive features to your applications, without having AI or data science skills. These AI services enable you to build cognitive solutions that can see, hear, speak, understand, and even make decisions.

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
### Vision 

AI Services features (1) the ability to leverage off-the-shelf APIs pre-trained to tag and analyze your images and videos, and (2) customizable models that allow you to train models using your own data.

**Computer Vision**

Analyze content in images and video with a turn-key API service
-	[Vision Studio](https://portal.vision.cognitive.azure.com/gallery/featured) - Explore functionality by trying each API (requires Azure account)
- [Computer Vision Learning Path](https://docs.microsoft.com/en-us/learn/paths/explore-computer-vision-microsoft-azure/) - Get started analyzing images with the API

**Custom Vision**

Build Custom Image Classification & Object Detection models for your scenario
- [Learning Path for Object Detection](https://docs.microsoft.com/en-us/learn/modules/train-custom-vision-ai/) - Get started using AI to recognize objects in images using the Custom Vision service
- [Learning Path for Image Classification](https://docs.microsoft.com/en-us/learn/modules/classify-images-custom-vision/) - Get started classifying images using the Custom Vision service

**Face API**

Detect and identify people in images
- [Face API Learning Path](https://docs.microsoft.com/en-us/learn/modules/detect-analyze-faces/) - Get started detecting and analyzing faces 
- [Transparency Note](https://azure.microsoft.com/mediahandler/files/resourcefiles/transparency-note-azure-cognitive-services-face-api/Face%20API%20Transparency%20Note%20(March%202019).pdf) - Understand how Face API works, the choices you can make as System Owner that influence accuracy, and the importance of thinking about the whole system, including the technology, the people, and the environment

### Language

**[Cognitive Services for Language](https://docs.microsoft.com/en-us/azure/cognitive-services/language-service/overview)** similarly provides pre-trained, pre-configured models to use in a turn-key fashion, as well as customizable services that enable you to leverage your own data with the provided platform and tooling.

With an Azure subscription, navigate to the **[Language Studio](https://language.cognitive.azure.com/)** to explore all of the tools offered for Natural Language Processing within Azure AI Services.

Key functionality includes:
* [Named Entity Recognition (NER)](https://docs.microsoft.com/en-us/azure/cognitive-services/language-service/named-entity-recognition/concepts/named-entity-categories): Identify and categorize named entities from input documents, including names of people, locations, organizations, events, products, addresses, phone numbers, emails, URLs, IP addresses, dates & times, and quantities.
    * [Custom Named Entity Recognition](https://docs.microsoft.com/en-us/azure/cognitive-services/language-service/custom-named-entity-recognition/overview): Build custom models to extract domain-specific entities.
* [Personally identifying (PII) and health (PHI) information detection](https://docs.microsoft.com/en-us/azure/cognitive-services/language-service/personally-identifiable-information/concepts/entity-categories): Identify, categorize, and redact sensitive information from documents, including names of people, job roles, organizations, addresses, phone numbers, emails, URLs, IP addresses, dates & times, quantities, ABA routing numbers, SWIFT codes, credit card numbers, International Banking Account Numbers, and country/region-specific identification (e.g. U.S. Social Security Numbers).
* [Language detection](https://docs.microsoft.com/en-us/azure/cognitive-services/language-service/language-detection/overview): Determine which language a document is written in.
* [Sentiment analysis and opinion mining](https://docs.microsoft.com/en-us/azure/cognitive-services/language-service/sentiment-opinion-mining/how-to/call-api?source=recommendations): Leverage Sentiment Analysis to label text as *positive*, *neutral*, or *negative*.  Use Opinion Mining to gather more granular information about sentiment, including the subject the text is referring to as well as the associated opinion or sentiment.  
* [Summarization](https://docs.microsoft.com/en-us/azure/cognitive-services/language-service/summarization/overview?tabs=document-summarization): Summarize documents or conversations.
* [Key phrase extraction](https://docs.microsoft.com/en-us/azure/cognitive-services/language-service/key-phrase-extraction/overview): Identify and extract the main concepts in text.
* [Entity linking](https://docs.microsoft.com/en-us/azure/cognitive-services/language-service/entity-linking/overview): Identify entities in text and provide a Wikipedia link for more information.
* [Text Analytics for Health](https://docs.microsoft.com/en-us/azure/cognitive-services/language-service/text-analytics-for-health/overview?tabs=ner): Extract and label medical information from health documents, such as doctor's notes, discharge summaries, clinical documents, and electronic health records.  
* [Custom Text Classification](https://docs.microsoft.com/en-us/azure/cognitive-services/language-service/custom-text-classification/overview): Train your own text classification models using your data.
* [Conversational language understanding](https://docs.microsoft.com/en-us/azure/cognitive-services/language-service/conversational-language-understanding/overview): Predict what the user's intent is when they say a particular phrase or sentence so that you can reply accordingly.
* [Question answering](https://docs.microsoft.com/en-us/azure/cognitive-services/language-service/question-answering/overview): Find the most appropriate answer for a user's question for a conversational client application.

To start getting hands-on, refer to the following resources:
* [GitHub Python Samples for Text](https://github.com/Azure/azure-sdk-for-python/tree/main/sdk/textanalytics/azure-ai-textanalytics/samples): Common scenario operations with the Azure Text Analytics client library for Python
* [Learning Path for Common Pre-configured Language APIs](https://docs.microsoft.com/en-us/training/modules/extract-insights-text-with-text-analytics-service/): Get started extracting insights from text
* [Learning Path for Customizable Language solutions](https://docs.microsoft.com/en-us/training/paths/build-custom-text-analytics/): Build custom text classification and custom NER models using the Language service

### Speech

**[Cognitive Services for Speech](https://learn.microsoft.com/en-us/azure/cognitive-services/speech-service/)** also has both pre-trained models as well as customizable services to convert speech to text, text to speech, as well as speaker recognition, and speech translation.

**Speech to Text**
* [Speech to Text Overview](https://learn.microsoft.com/en-us/azure/cognitive-services/speech-service/speech-to-text): Explore the capabilities of the STT service.

**Text to Speech**
* [Text to Speech Overview](https://learn.microsoft.com/en-us/azure/cognitive-services/speech-service/text-to-speech): Explore the capabilities of the TTS service.

**Speaker Recognition**
* [Speaker Recognition Overview](https://learn.microsoft.com/en-us/azure/cognitive-services/speech-service/speaker-recognition-overview): Explore Speaker Recognition and some commonly asked questions.

**Speech Translation**
* [Speech Translation QuickStart](https://learn.microsoft.com/en-us/azure/cognitive-services/speech-service/get-started-speech-translation?tabs=terminal&pivots=programming-language-csharp): Get hands-on with translating speech from a microphone in the language of your choice.

**Custom Neural Voice**
* [Custom Neural Voice Overview](https://learn.microsoft.com/en-us/azure/cognitive-services/speech-service/custom-neural-voice): Explore the different project types for Custom Neural Voice. This page is followed by a great step-by-step guide on how to get started.
* [How to Create a Custom Neural Voice](https://techcommunity.microsoft.com/t5/ai-cognitive-services-blog/how-to-create-a-custom-neural-voice/ba-p/3028275): A great tutorial along with best practices.
* [Latest Updates on Azure Neural TTS](https://techcommunity.microsoft.com/t5/ai-cognitive-services-blog/latest-updates-on-azure-neural-tts-new-voices-for-casual/ba-p/2761278): Stay up to date with the latest changes and view some examples.
* [Transparency Note and Use Cases](https://learn.microsoft.com/en-us/legal/cognitive-services/speech-service/custom-neural-voice/transparency-note-custom-neural-voice?context=%2Fazure%2Fcognitive-services%2Fspeech-service%2Fcontext%2Fcontext): Understanding some key considerations when using Custom Neural Voice
* [Guidelines for responsible deployment of synthetic voice technology](https://learn.microsoft.com/en-us/legal/cognitive-services/speech-service/custom-neural-voice/concepts-guidelines-responsible-deployment-synthetic): Understand how to responsibly use synthetic voice technology.
* [Data, privacy, and security for Custom Neural Voice](https://learn.microsoft.com/en-us/legal/cognitive-services/speech-service/custom-neural-voice/data-privacy-security-custom-neural-voice?context=%2Fazure%2Fcognitive-services%2Fspeech-service%2Fcontext%2Fcontext): Understand how the data will be used and processed.

**Content Creation**
* [Speech Studio](https://speech.microsoft.com/audiocontentcreation?msclkid=68f18c52c10711ec8b45f75fc0c21c62): Test the features of Content Creation.
* [Audio Content Creation](https://www.youtube.com/watch?v=ygApYuOOG6w&t=173s): Tutorial on how to convert text to speech using Microsoft AI voices.