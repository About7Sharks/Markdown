---
title: Training LLMs
date: 2023-10-7
author: Zachary Carlin
location: Tampa FL
image: https://upload.wikimedia.org/wikipedia/commons/thumb/e/e4/Artificial_neural_network.svg/440px-Artificial_neural_network.svg.png
summary: LLM's are a type of AI that are trained on large amounts of text. They are able to generate outputs that are similar to the training data. This allows them to be used for a variety of tasks such as question answering, summarization, and translation.
tags: ["AI", "LLM", "Tech", "Featured"]
---

# LLM's 

## How do LLM's learn?
With today's current state of the art (Subject to change!) the training is usually spit into 2 parts:
1. Pre-training
2. Fine-tuning

### Pre-training
Pre-training is the process of training a model on a large corpus of text. This is usually done on a large dataset of text from the internet. The model is trained to predict the next word in a sentence. This is called a language model.

Here are a few examples of what the training data often looks like ([Source](https://huggingface.co/datasets/databricks/databricks-dolly-15k/viewer/default/train?row=0)). 

| Instruction | Context | Response | Category |
| ----------- | ------- | -------- | -------- |
| When did Virgin Australia start operating? | Virgin Australia, the trading name of Virgin Australia Airlines Pty Ltd, is an Australian-based airline. It is the largest airline by fleet size to use the Virgin brand. It commenced services on 31 August 2000 as Virgin Blue, with two aircraft on a single route. It suddenly found itself as a major airline in Australia's domestic market after the collapse of Ansett Australia in September 2001. The airline has since grown to directly serve 32 cities in Australia, from hubs in Brisbane, Melbourne and Sydney. | Virgin Australia commenced services on 31 August 2000 as Virgin Blue, with two aircraft on a single route. | closed_qa |
| Which is a species of fish? Tope or Rope | | Tope | classification |

### Fine-tuning
Fine-tuning is the process of taking a pre-trained model and training it on a smaller dataset. This is usually done on a dataset that is specific to the task you want the model to perform. For example, if you want to train a model to answer questions, you would fine-tune the model on a dataset of questions and answers.

This is where users and companies can train their own models to perform specific tasks. For example, a company could train a model to answer questions about their products. Or a user could train a model to answer questions about their favorite TV shows or music preferences.

## How to fine-tune a model?

If you are trying to train a model 1 time for a specific task, I would recommend using [oobabooga](https://github.com/oobabooga/text-generation-webui) the have a great web interface that makes it easy to train, test, and deploy a model. Here is a [guide](https://github.com/oobabooga/text-generation-webui/blob/main/docs/Training-LoRAs.md) on how to fine-tune a model using oobabooga. They use the term LoRA to refer to a fine-tuned model.