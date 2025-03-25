# Fiction and Non-Fiction Text Classification

This repository contains the implementation of a classification model that distinguishes between fiction and non-fiction texts using linguistic features derived from part-of-speech (POS) tagging. Inspired by the research paper ["A Simple Approach to Classify Fictional and Non-Fictional Genres"](./A%20Simple%20Approach%20to%20Classify%20Fictional%20and%20Non-Fictional%20Genres.pdf), we replicate the results with a slight modification by utilizing the NLTK POS tagger instead of the one mentioned in the paper. The results demonstrate the robustness of the study. We further explore additional POS-based features for genre classification.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Data Sources](#data-sources)
- [Dependencies](#dependencies)
- [Usage](#usage)
- [Results](#results)
- [Further Work](#further-work)
- [References](#references)

## Introduction

The primary goal of this project is to classify text as fiction or non-fiction based on POS-based features. Initially, the study focuses on two key features:
1. Adverb-to-Adjective Ratio
2. Adjective-to-Pronoun Ratio

The classification is done using a logistic regression model. Additional POS-based features are also explored to test their efficacy in genre classification. Read the [original paper](./A%20Simple%20Approach%20to%20Classify%20Fictional%20and%20Non-Fictional%20Genres.pdf) for more details.

## Features

- **Adverb-to-Adjective Ratio**: Measures the prevalence of descriptive adverbs relative to adjectives.
- **Adjective-to-Pronoun Ratio**: Measures the descriptive richness of text in relation to pronouns.
- **Custom POS-Based Features**: Additional features derived from linguistic analysis are being evaluated for performance improvement.

## Data Sources

1. **Brown Corpus**: A collection of texts categorized into fiction and non-fiction, provided by the NLTK library.
2. **Baby BNC (British National Corpus)**: Fictional and non-fictional texts, sourced from the `baby_bnc.csv` file in the repository.

## Dependencies

Ensure the following libraries are installed:
- Python 3.7+
- NLTK
- pandas
- scikit-learn

Install dependencies using:
```bash
pip install -r requirements.txt
```

## Usage

1. **Prepare the Data**:
   - Place the `baby_bnc.csv` file in the repository root.
   - The Brown Corpus is automatically loaded from NLTK.

2. **Run the Notebook**:
   - Open and execute the Jupyter Notebook [`similar_results.ipynb`](./similar_results.ipynb) to reproduce results or experiment with additional features.

3. **Generate Features**:
   - Modify the feature extraction logic in the `extract_two_features` function or extend it to include new features.

4. **Train and Test**:
   - Execute the classification pipeline in the notebook to test the logistic regression model with various feature combinations.

## Results

- Using the NLTK POS tagger, the model achieves results comparable to the original study, validating its robustness.
- Preliminary experiments with additional POS-based features show promising directions for improving classification accuracy.

## Further Work

- Exploring additional POS-based ratios to improve classification accuracy.
- Testing the model on a broader set of corpora.
- Applying other machine learning algorithms to evaluate performance enhancements.
- Implementing explainability techniques to better understand the linguistic significance of features.

## References

1. Mohammed Rameez Qureshi, Sidharth Ranjan, Rajakrishnan P. Rajkumar, and Kushal Shah. ["A Simple Approach to Classify Fictional and Non-Fictional Genres"](./A%20Simple%20Approach%20to%20Classify%20Fictional%20and%20Non-Fictional%20Genres.pdf). *Proceedings of the Second Storytelling Workshop, Florence, Italy, August 1, 2019.*
2. NLTK documentation: [https://www.nltk.org/](https://www.nltk.org/)
3. Scikit-learn documentation: [https://scikit-learn.org/](https://scikit-learn.org/)
