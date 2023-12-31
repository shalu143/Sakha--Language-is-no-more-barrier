#  सखा- भाषा अब कोई बाधा नहीं है
# Sakha-Language is no more barrier
Databricks LLM CUP: Ready to launch your AI game to new heights? Build, iterate and polish your LLM ideas into shiny, production-ready solutions with this competition.

## Contents
* [Submission or Project Name](#Sakha-Language-is-no-more-barrier)
    * [Contents](#Contents)
    * [Short Description](#Short-description)
         * [What's the Problem?](#what's-the-problem)
         * [The Idea](#the-idea)
         * [Advantages](#Advantages)
    * [Demo Video](#Demo-video)
    * [The Architecture](#the-architecture)
    * [Getting Started](#Getting-started)
    * [Built-with](#Built-with)
    * [Acknowledgments](#Acknowledgments)
    * [Further Advancements](#Further-Advancements)
 
## Short Description
### What's the Problem
There are many geographical regions in the world, where more than one language is generally spoken. India is one such multilingual country, where a number of languages are spoken, and a mere 10% are English literate. Here, a single common language is adopted in the community for proper communication. But this can cause one language to be dominant over others, and can be a disadvantage to the speakers of other languages. This can also result in the disappearance of a language, its distinctive culture and a way of thinking. For national / international companies here, having their business / marketing content in multiple languages is an expensive option, hence majority of them stick to one language of commerce – English, which could also mean losing opportunity to better connect with local audiences and thus losing potential customers. While there is nothing wrong with using English, those who are not conversant in that language are left out of the mainstream commerce.


### The Idea
Our idea is to bridge this gap. People should be allowed to express themselves, ask their queries in their own language. We propose a solution that Let people ask queries in local language, use LLMs to understand and get information in English and translate this back into local language. We harness the power of Large Language Models for two uses – one to translate from local language to English and vice-versa, find most similar query in our database, if not then to answer his query via base LLM. This solution intends to let people query and get their queries answered in their own local language. This will only be applicable to those languages that are supported by the underlying LLM. This will not only help businesses especially banks reach out wider population but to get benefits of banking reach the common man and help him improve his financial prospects. 

### Advantages
* Increased Customer Reach:
   Supporting multiple languages, a chatbot can reach a wider audience and provide assistance to users who may not speak the same language
   Make information and services – especially essential services like Banking – more accessible to people
   This benefits both – the people as well as the company.

* Improved Personalization:
   Multi-lingual chatbots can provide personalized recommendations and tailored experiences to users based on their language and cultural preferences.

* Enhanced Customer Service:
   Chatbots can provide better customer service and help resolve issues more efficiently, thus leading to increased customer satisfaction.

## Demo Video
[Demo Video](https://youtu.be/7ksZJzD74Jw)

## Getting Started
* [gradio](htps://93dfd7ec6727684e8d.gradio.live) https://93dfd7ec6727684e8d.gradio.live link which is valid for 72 hours
* use the script and run it to get the link that can be used


## The Architecture
* The user opens the Gradio app and has options of typing the data in the local language
* Translation: Utilizing given prompt in given local language using LLM (Llama-70b-chat) through mlflow route.
* RAG: The translated prompt is converted to embeddings using Instructor-xl embeddings and searched in the created vector database(chroma) from the local language personalised data.
* The Prompt with the context (most similar embeddings from the semantic search) is passed to the LLM for the result
* Translation: Translation of result in the local language

## Built-with
We have used:
* Gradio is used to build the front-end of the app. [Gradio](https://www.gradio.app/)
* Databricks was used for Coding. All the framework is designed in Databricks [Databricks](https://www.databricks.com/)
* We have used LLAMA-2 70b chat as the chosen Large Language Model. MosaicML inferencing was used to get the chat completion output from the prompt. [MosaicML](https://www.mosaicml.com/)
* Embeddings were done using Instructor-xl model [HuggingFace Embedding](https://huggingface.co/hkunlp/instructor-xl)
* The Embeddings were stored in the ChromaDb vector database. [Chromadb](https://www.trychroma.com/)
* Langchain and MLflow were used for the framework and pipeline of  the app. [Langchain](https://www.langchain.com/) and [MLflow](https://mlflow.org/)

## Further Advancements
* Currently for demo purpose, we have built the solution for hindi language. The Same to be Scaled for different regional languages.
* Fine-Tuning Llama 70b chat model with the hindi custom data
* Fine-Tuning the model with other local native languages
* Scaling the solution for different organizations

