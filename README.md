# SMM4H 2022 Task 8: Classification of self-reported chronic stress on Twitter (in English)

## Overview 

Chronic stress is defined as the physiological or psychological response to a prolonged internal or external stressful event (i.e., a stressor), which can lead to poor mental health, including depression and anxiety, and can also take a toll on the body, resulting in the dysfunctions of cardiovascular, metabolic, endocrine, and immuno-inflammatory systems. Traditional methods of assessing stress, including interviews, questionnaires/surveys, etc., have some limitations in accurately measuring population-level stress. Thus, there is a critical need to develop innovative chronic stress assessment methods. Social media are potentially valuable resources for studying chronic stress and its characteristics, and the first step is to accurately detect the tweets that are self-disclosures of chronic stress. In this task, about 37% of the tweets are positive (self-disclosure of chronic stress, P) and 63% are negative (non-self-disclosure of chronic stress, N). Systems designed for this task need to automatically identify tweets in the self-disclosure category. Classifier evaluation will be based on the F1 score over the positive class.

**This note was for #SMM4H 2022 Shared Task 8: Extraction of the clinical and social impacts of non-medical substance use from Reddit.**

**Codalab: https://codalab.lisn.upsaclay.fr/competitions/16648**

## Key Features

**Dataset Composition:** The Reddit-Impacts dataset consists of 1,380 posts, with 23% containing annotated entities related to clinical and social impacts of substance use. The dataset includes annotations for 30 entity types, focusing on the most critical but often underrepresented aspects of substance use.

**Annotation Process:** Posts were manually annotated, focusing on identifying clinical impacts (e.g., health consequences) and social impacts (e.g., effects on relationships and communities) reported by Reddit users discussing substance use.

**Machine Learning Models:** Baseline performance for NER tasks was established using several models, including BERT, RoBERTa, DANN (a few-shot learning model), and GPT-3.5 in a one-shot setting.

## Data Collection and Annotation

**Data Source:** The dataset was curated from 14 opioid-related subreddits, selected for their relevance and high levels of user engagement. Posts were collected using the Python Reddit API Wrapper (PRAW).

**Annotation:** A comprehensive manual annotation process was applied to identify and classify 30 different entity types, with a particular focus on the clinical and social impacts of substance use.

## Dataset Statistics

Training Data: 843 posts  
Validation Data: 259 posts  
Testing Data: 278 posts  
Entity Types: Clinical impacts and social impacts for subsetance use 

## Baseline Models and Performance

**BERT and RoBERTa:** Transformer-based models fine-tuned on the full training dataset, although they struggled to detect the sparse clinical and social impact entities.

**DANN:** A few-shot learning model that achieved the highest F1-scores among the tested models when trained on the full dataset.

**GPT-3.5:** Evaluated in a one-shot setting, demonstrating higher accuracy in few-shot learning scenarios compared to traditional pre-trained models.

**Llama3:** Ealuated its performance in recognizing clinical and social impacts within the Reddit-Impacts dataset, showcasing its potential in handling sparse and nuanced entities in social media data.

## Usage

To use this dataset:

**Download the Dataset:** Access the dataset through the google group for #SMM4H 2024 shared task 4.  
**Evaluation:** Compare the performance of different models using the evaluation metrics provided.
