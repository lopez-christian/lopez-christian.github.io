---
layout: post
published: true
title: Sentiment Analysis with Deep Learning Using BERT
date: '2020-09-12'
---
## Using BERT to Analyze a Dataset for Sentiment Analysis

<p align="center">
<img width="964" alt="Screen Shot 2020-10-01 at 9 33 58 AM" src="https://user-images.githubusercontent.com/53641091/94837890-a8309c80-03c9-11eb-89ad-c57bd91ce826.png">
</p>

<p align="center">
<img width="599" alt="Screen Shot 2020-10-01 at 9 33 39 AM" src="https://user-images.githubusercontent.com/53641091/94837940-b7174f00-03c9-11eb-9a22-790493d848b8.png">
</p>

#### <ins> KEY CONCEPTS: </ins>

What BERT is and what it can do?

Clean and preprocess text dataset

Split dataset into training and validation sets using stratified approach

Tokenize (encode) dataset using BERT toknizer

Design BERT finetuning architecture

Evaluate performance using F1 scores and accuracy

Finetune BERT using training loop

For this guided project from Coursera Project Network the purpose was to analyze a dataset for sentiment analysis. We learned how to read in a PyTorch BERT model, and adjust the architecture for multi-class classification. We learned how to adjust an optimizer and scheduler for ideal training and performance. While fine-tuning this model, we also learned how to design a train and evaluate loop to monitor model performance as it trains, including saving and loading models. The end result was a Sentiment Analysis model that leverages BERT's large-scale language knowledge. 

#### <ins> PROJECT OUTLINE: </ins>

Task 1: Introduction (this section)

Task 2: Exploratory Data Analysis and Preprocessing

Task 3: Training/Validation Split

Task 4: Loading Tokenizer and Encoding our Data

Task 5: Setting up BERT Pretrained Model

Task 6: Creating Data Loaders

Task 7: Setting Up Optimizer and Scheduler

Task 8: Defining our Performance Metrics

Task 9: Creating our Training Loop

#### <ins> Project SCREENSHOTS: </ins>

<p align="center">
<img width="1157" alt="Screen Shot 2020-10-01 at 10 03 33 AM" src="https://user-images.githubusercontent.com/53641091/94840710-b4b6f400-03cd-11eb-9716-8671a969f852.png">
</p>

<p align="center">
<img width="1135" alt="Screen Shot 2020-10-01 at 10 09 53 AM" src="https://user-images.githubusercontent.com/53641091/94841038-44f53900-03ce-11eb-80f5-5796ebfd168f.png">
</p>

<p align="center">
<img width="401" alt="Screen Shot 2020-10-01 at 9 33 19 AM" src="https://user-images.githubusercontent.com/53641091/94841088-5b02f980-03ce-11eb-826f-ed7fd039c43c.png">
</p>

*1. .*

[COVID-19 PyTorch Image Classifier](https://github.com/lopez-christian/COVID-19-PyTorch-Image-Classifier)
