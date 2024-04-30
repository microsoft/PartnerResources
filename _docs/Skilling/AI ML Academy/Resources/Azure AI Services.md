---
layout: page
title: Azure AI Services
description: Resources for Azure AI Services formerly known as Cognitive Services 
updated: 2024-01-29
permalink: /skilling/ai-ml-academy/resources/azure-ai-services
tags: 
- azure
- learning plan
- academy content
- aiml resources
---

# Azure AI Services Resources

## Fundamentals
Go through an overview of all the AI service pillars, sample use cases, as well as how to start working with some of these services through a unified studio experience.

### Overview & Use Cases
* [**Overview:** Azure AI Services Guide](https://learn.microsoft.com/en-us/azure/ai-services/)
* [**Use Cases:** Captioning with Speech-to-Text](https://learn.microsoft.com/en-us/azure/cognitive-services/speech-service/captioning-concepts?pivots=programming-language-csharp)
* [**Use Cases:** Call Center Overview](https://learn.microsoft.com/en-us/azure/cognitive-services/speech-service/call-center-overview)

### How to get started in the Azure Studio
* [Vision Studio](https://portal.vision.cognitive.azure.com/gallery/featured)
* [Speech Studio](https://speech.microsoft.com/)
* [Language Studio](https://language.cognitive.azure.com/)


## Associate

### Vision
Azure Cognitive Services for Vision is a cloud-based service that offers innovative computer vision capabilities. You can analyze images, read text, and detect faces with prebuilt image tagging, conduct text extraction with optical character recognition (OCR), and perform responsible facial recognition. These vision features can be integrated into your projects with no machine learning experience required.

* [Overview](https://learn.microsoft.com/en-us/azure/cognitive-services/computer-vision/)
* [Product Announcements](https://learn.microsoft.com/en-us/azure/ai-services/computer-vision/whats-new)
* [Pricing](https://azure.microsoft.com/en-us/pricing/details/cognitive-services/computer-vision/)
  
### Speech 
Azure Cognitive Services for Speech provides speech-to-text and text-to-speech capabilities. You can transcribe speech-to-text with high accuracy, produce natural-sounding text-to-speech voices, translate spoken audio, and use speaker recognition during conversations. In addition, you can create custom voices, add specific words to your base vocabulary, or build your own models. The service can be run in the cloud or at the edge in containers. 

* [Overview](https://learn.microsoft.com/en-us/azure/cognitive-services/speech-service/)
* [Product Announcements](https://learn.microsoft.com/en-us/azure/ai-services/speech-service/releasenotes?tabs=speech-sdk)
* [Pricing](https://azure.microsoft.com/en-us/pricing/details/cognitive-services/speech-services/)
  
### Language 
Azure Language is a cloud-based service that provides Natural Language Processing (NLP) features for understanding and analyzing text. With Azure Cognitive Services, you use pre-made models to identify entities, summarize text, find key phrases, understand sentiment, and more. There are more custom routes that allow you to create models that are able to extract key information and classify text for more specific use cases, create Q&A chatbots, and orchestrate  workflows to connect language models to other services.

* [Overview](https://learn.microsoft.com/en-us/azure/cognitive-services/language-service/overview)
* [Transparency Note](https://learn.microsoft.com/en-us/legal/cognitive-services/language-service/transparency-note?context=%2Fazure%2Fcognitive-services%2Flanguage-service%2Fcontext%2Fcontext)
* [Product Announcements](https://learn.microsoft.com/en-us/azure/ai-services/language-service/whats-new?tabs=csharp)
* [Pricing](https://azure.microsoft.com/en-us/pricing/details/cognitive-services/language-service/)
* [Migration Guidance for API & Standard Voice](https://learn.microsoft.com/en-us/azure/ai-services/speech-service/migration-overview-neural-voice)
  
### Decision
Azure Cognitive Services for Decision provides Natural Language Processing (NLP) features to provide recommendations for informed decision-making. You can use anomaly detection, content moderation, and personalizer.

* The Azure Content Moderator API checks text, image, and video content for material that is potentially offensive, risky, or otherwise undesirable. Content Moderator is being deprecated in February 2024, and will be retired by February 2027. It is being replaced by **[Azure AI Content Safety](https://learn.microsoft.com/en-us/azure/ai-services/content-safety/)**, which offers advanced AI features and enhanced performance.
* Starting on the **20th of September, 2023** you will not be able to create new Personalizer resources. The Personalizer service is being retired on the **1st of October, 2026.**
* Starting on the **20th of September, 2023** you won’t be able to create new Anomaly Detector resources. The Anomaly Detector service is being retired on the **1st of October, 2026.**


## Expert

### Vision

#### Computer Vision
* [Overview](https://learn.microsoft.com/en-us/azure/cognitive-services/computer-vision/overview)
* [QuickStart](https://learn.microsoft.com/en-us/training/paths/explore-computer-vision-microsoft-azure/)
* [OCR Overview](https://learn.microsoft.com/en-us/azure/cognitive-services/computer-vision/overview-ocr)
* [OCR + Computer Vision](https://www.youtube.com/watch?v=PrjlfdFRUrc&list=PLlrxD0HtieHi0mwteKBOfEeOYf0LJU4O1&index=18)
* [OCR + Document Intelligence](https://learn.microsoft.com/en-us/azure/ai-services/document-intelligence/concept-read?view=doc-intel-4.0.0)
* [Image Analysis Overview](https://learn.microsoft.com/en-us/azure/ai-services/computer-vision/overview-image-analysis?tabs=4-0)
* [Face Overview](https://learn.microsoft.com/en-us/azure/ai-services/computer-vision/overview-identity)
* [Face QuickStart](https://learn.microsoft.com/en-us/training/modules/detect-analyze-faces/)
* [Face Transparency Note](https://azure.microsoft.com/mediahandler/files/resourcefiles/transparency-note-azure-cognitive-services-face-api/Face%20API%20Transparency%20Note%20(March%202019).pdf)
* [Spatial Analysis Overview](https://learn.microsoft.com/en-us/azure/ai-services/computer-vision/intro-to-spatial-analysis-public-preview)
* [Spatial Analysis Florence Model](https://azure.microsoft.com/en-us/blog/announcing-a-renaissance-in-computer-vision-ai-with-microsofts-florence-foundation-model/)
* [Spatial Analysis with IoT Edge](https://learn.microsoft.com/en-us/azure/architecture/guide/iot-edge-vision/)
* [Visual Search Toolkit](https://www.youtube.com/watch?v=ZEwaqkMkLUY&list=PLlrxD0HtieHi0mwteKBOfEeOYf0LJU4O1&index=9)

#### Custom Vision
* [Overview](https://learn.microsoft.com/en-us/azure/ai-services/custom-vision-service/overview)
* [QuickStart](https://learn.microsoft.com/en-us/training/modules/classify-images-custom-vision/)
* [Custom Vision with AutoML](https://www.youtube.com/watch?v=VvTjHzcYuaQ&list=PLlrxD0HtieHi0mwteKBOfEeOYf0LJU4O1&index=39)

### Speech 
* [Speech-to-Text](https://learn.microsoft.com/en-us/azure/cognitive-services/speech-service/speech-to-text)
* [Text-to-Speech ](https://learn.microsoft.com/en-us/azure/cognitive-services/speech-service/text-to-speech)
* [Speech Translation](https://learn.microsoft.com/en-us/azure/cognitive-services/speech-service/get-started-speech-translation?tabs=terminal&pivots=programming-language-csharp)
* [Speaker Recognition](https://learn.microsoft.com/en-us/azure/cognitive-services/speech-service/speaker-recognition-overview)
* [Custom Neural Voice Overview](https://learn.microsoft.com/en-us/azure/cognitive-services/speech-service/custom-neural-voice)
* [Custom Neural Voice QuickStart](https://www.youtube.com/watch?v=di3vKMhyLaY)
* [Whisper Model](https://learn.microsoft.com/en-us/azure/ai-services/speech-service/whisper-overview)
* [Custom Vision: Get Started](https://github.com/azure-samples/rock-paper-scissors-customvision/tree/master/)
* [Hyperparameter for AutoML CV Tasks](https://learn.microsoft.com/en-us/azure/machine-learning/reference-automl-images-hyperparameters)
* [Containers](https://learn.microsoft.com/en-us/azure/cognitive-services/containers/container-faq)
* [Computer Vision with IoT Edge](https://learn.microsoft.com/en-us/azure/architecture/guide/iot-edge-vision/)

### Language

#### Entity Recognition
* [Custom NER Overview](https://learn.microsoft.com/en-us/azure/ai-services/language-service/custom-named-entity-recognition/overview)
* [NER in Azure AI Language](https://learn.microsoft.com/en-us/azure/ai-services/language-service/named-entity-recognition/overview)
* [PII Detection](https://learn.microsoft.com/en-us/azure/ai-services/language-service/personally-identifiable-information/overview)
* [Entity Linking](https://learn.microsoft.com/en-us/azure/ai-services/language-service/entity-linking/overview)
* [TA for Health Overview](https://learn.microsoft.com/en-us/azure/ai-services/language-service/text-analytics-for-health/overview?tabs=ner)
* [Key Phrase Extraction](https://learn.microsoft.com/en-us/azure/ai-services/language-service/key-phrase-extraction/overview)
* [Custom Text Classification](https://learn.microsoft.com/en-us/azure/ai-services/language-service/custom-text-classification/overview)
* [Document & Conversation Summarization](https://learn.microsoft.com/en-us/azure/ai-services/language-service/summarization/overview?tabs=document-summarization)
* [Sentiment Analysis Overview](https://learn.microsoft.com/en-us/azure/ai-services/language-service/sentiment-opinion-mining/overview?tabs=prebuilt)
* [Question Answering Overview](https://learn.microsoft.com/en-us/azure/ai-services/language-service/question-answering/overview)
* [Conversational Language Understanding Overview](https://learn.microsoft.com/en-us/azure/ai-services/language-service/conversational-language-understanding/overview)
* [Migration](https://learn.microsoft.com/en-us/azure/ai-services/language-service/concepts/migrate)
* [Translator Overview](https://learn.microsoft.com/en-us/azure/ai-services/translator/translator-overview)
* [Lang Detection](https://learn.microsoft.com/en-us/azure/ai-services/language-service/language-detection/overview)
* [Language Workflow Orchestration Workflow](https://learn.microsoft.com/en-us/azure/ai-services/language-service/orchestration-workflow/overview)