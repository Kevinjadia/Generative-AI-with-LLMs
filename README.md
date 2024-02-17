# Project Title: Enhanced Dialogue Summarization and Content Detoxification with FLAN-T5

## Overview
This project focuses on dialogue summarization using generative AI techniques with a specific emphasis on enhancing model performance through prompt engineering. Additionally, it explores various fine-tuning approaches including full finetuning, Parameter Efficient Fine-Tuning (PEFT), and reinforcement learning techniques such as Proximal Policy Optimization (PPO) for generating less-toxic summaries. The main goal is to create efficient and effective models for summarizing dialogues while mitigating the presence of toxic content.

## Project Parts

### 1. Generative AI Use Case: Summarize Dialogue without and with Prompt Engineering
This part involves experimenting with generative AI models for dialogue summarization both with and without prompt engineering. The objective is to understand how prompt engineering can enhance the performance of the models in generating accurate summaries.

### 2. Full Finetuning and Parameter Efficient Fine-Tuning (PEFT)
Here, we conduct fine-tuning of the FLAN-T5 model for dialogue summarization. We explore both full finetuning and PEFT optimization methods, utilizing LoRA for efficient parameter tuning. The goal is to optimize model performance while minimizing computational resources.

### 3. Fine-Tuning with Reinforcement Learning (PPO) and PEFT to Generate Less-Toxic Summaries
In this part, we delve into fine-tuning the model using reinforcement learning techniques, particularly Proximal Policy Optimization (PPO). We leverage PEFT along with Meta AI's RoBERTa-based hate speech model to generate summaries with reduced toxic content. The objective is to develop models that not only summarize dialogues effectively but also promote content detoxification by reducing the presence of harmful language.

## Files and Libraries

### Files:
- **Model weights**: 
  - Full finetuning weights: [flan-dialogue-summary-checkpoint](./flan-dialogue-summary-checkpoint)
  - PEFT finetuning weights: [peft-dialogue-summary-checkpoint](./peft-dialogue-summary-checkpoint)

### Libraries to Install:
- Trl: for accessing PPO
- torch==1.13.1 
- torchdata==0.5.1 
- transformers==4.27.2 
- datasets==2.11.0 
- evaluate==0.4.0 
- rouge_score==0.1.2 
- loralib==0.1.1 
- peft==0.3.0 

## Dataset

### DialogSum Dataset
- **Description**: DialogSum is a large-scale dialogue summarization dataset comprising 13,460 dialogues along with manually labeled summaries and topics. Additionally, it includes 100 holdout data for topic generation.
- **Data Fields**:
  - **dialogue**: Text of dialogue.
  - **summary**: Human-written summary of the dialogue.
  - **topic**: Human-written topic/one-liner of the dialogue.
  - **id**: Unique file ID of an example.

## Models

### FLAN T5 Base Model
- **Model**: google/flant5-base

### Meta AI's RoBERTa-based Hate Speech Model
- **Model**: facebook/roberta-hate-speech-dynabench-r4-target

## How to Run the Notebook?
1. Upload both fine-tuning weights folders (`flan-dialogue-summary-checkpoint` and `peft-dialogue-summary-checkpoint`) in your environment.
2. Change the path accordingly in the notebook.
3. You are ready to execute the notebook and explore the dialogue summarization and content detoxification techniques.
