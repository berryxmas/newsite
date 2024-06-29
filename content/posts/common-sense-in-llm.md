---
title: "Enhancing Common Sense in Large Language Models: Insights from a Kaggle Competition"
date: 2022-02-15T23:15:00+07:00
slug: common-sense-in-llm
category: llm
tags:  ["First Post", "LLMs", "AI"]
summary:
description: 
cover:
  image: "covers/common-sense-img.jpeg"
  alt: "Common sense in AI?"
  caption: 
  relative: true
showtoc: true
draft: false
---

# Enhancing Common Sense in Large Language Models: Insights from a Kaggle Competition

Endowing AI with common sense, the intuitive understanding of everyday situations, remains a significant hurdle. This challenge is crucial as it underpins the natural language understanding capabilities of AI, making interactions more human-like and reliable. Recently, I participated in a Kaggle competition aimed at evaluating and improving the common sense reasoning of natural language understanding systems. Here’s an overview of the competition, its importance, and my experience.

## The Importance of Common Sense in AI

Introducing common sense to natural language understanding systems has garnered increasing attention within the research community. Unlike specific, domain-based knowledge, common sense involves a broad understanding of the world, enabling systems to handle ambiguous and context-dependent scenarios effectively. The ability to identify why a statement does not make sense is fundamental to building robust AI models capable of interacting with humans in a more intuitive and meaningful way.

## The Challenge: Common Sense Reasoning

The competition posed a unique and intriguing task: Given a statement that defies common sense, can a model identify the best explanation for why it does not make sense? Participants were required to choose the most appropriate reason from three given options. For example:

**Statement:** He put an elephant into the fridge.
- **A:** An elephant is much bigger than a fridge. (correct)
- **B:** Elephants are usually white while fridges are usually white.
- **C:** An elephant cannot eat a fridge.

In this instance, option A is correct because it directly addresses the implausibility of the statement based on the relative sizes of an elephant and a fridge.

## Evaluation and Submission

The evaluation was straightforward yet challenging. Submissions were assessed based on category accuracy, which measures the proportion of correctly identified explanations:

\[ \text{Category Accuracy} = \frac{1}{N} \sum_{i=1}^{N} (y_i = \hat{y}_i) \]

Where \( N \) is the number of sentences in the test set, \( y_i \) is the true label, and \( \hat{y}_i \) is the predicted label. Achieving a score around 0.33, akin to random guessing, was the baseline.

Participants were required to submit their predictions in a CSV format, containing the sentence IDs and the corresponding predicted labels. The dataset comprised 8000 sentences for training and 2000 sentences for testing.

## Dataset and Files

The provided dataset included:
- `train_data.csv`: The training set with sentences and options.
- `train_answers.csv`: Correct labels for the training set.
- `test_data.csv`: The test set.
- `sample.csv`: A sample submission file in the correct format.

Each data entry contained:
- `id`: An identifier for each sentence.
- `FalseSent`: The nonsensical sentence.
- `OptionA`, `OptionB`, `OptionC`: Potential explanations.
- `answer`: The correct answer among the options.

## My Experience and Approach

Participating in this competition was both a challenging and enlightening experience. I utilized several techniques to enhance the model's ability to discern common sense. Here’s a brief overview of my approach:

1. **Data Preprocessing:** Cleaning and preparing the dataset for efficient model training.
2. **Model Selection:** Leveraging transformer-based models such as BERT, known for their superior natural language understanding capabilities.
3. **Fine-tuning:** Adapting pre-trained models to the specific task of common sense reasoning using the provided dataset.
4. **Evaluation and Optimization:** Iteratively evaluating model performance on a validation set and optimizing hyperparameters to improve accuracy.

## Conclusion

The competition highlighted the ongoing challenges and advancements in integrating common sense into AI systems. By tackling seemingly simple yet fundamentally complex tasks, we push the boundaries of what AI can achieve, moving closer to creating systems that understand and interact with the world more naturally.

For more details about the competition, you can visit the [Kaggle competition page](https://www.kaggle.com/competitions/common-sense-challenge-2021).
