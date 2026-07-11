# MATH-5389-AI-Mathematics-Final-Project
An Evaluation of Algorithmic Bias and Fragility in Rate My Professor Sentiment Analysis
Course: MATH 5389 - AI Math Final Project

# Overview
This project builds a sentiment classifier on real Rate My Professor (RMP) reviews, then deliberately stress tests it. Rather than stopping once the model looks accurate, the project pushes it toward failure through overfitting experiments, adversarial (tricky) examples, and a bias audit. RMP reviews are informal, sarcastic, emotionally driven, and sometimes touch in identity (accent, language, gender). That makes them a good stress test for a classic NLP pipeline built on TF-IDF features and a linear classifier.

# Goals

1. Train a baseline sentiment classifier on real data.
2. Show how model complexity (n-grams, regularization strength c) drives a model from underfitting to overfitting.
3. Break the model with adversarial inputs sarcasm, keyword stuffing, and negation.
4. Audit the model for bias by comparing performance on subgroups against the dataset.
5. Produce a 4-6 page report where the model succeeds, where it fails, and why those failures matter.

# Project Structure

Introduction: Background on RMP and why sentiment analysis on it is a good test case.
Goals: What the project sets out to demonstrate.
Setup & Data Loading: Imports and loading the real RMP dataset from GitHub.
Dataset Pre-Processing: Filtering placeholders, short comments, mapping raw labels "Awful", "Neutral", "Great", and a word cloud with a vocabulary check.
Training, Testing & Baseline Model: TF-IDF and Logistic Regression pipeline, parameter search, and a regularized baseline model with a confusion matrix.
Overfitting: A complexity sweep to deliberately overfit the model.
Failures: Hand written adversarial reviews (sarcasm, keyword stuffing, negation, backhanded compliments) used towards the baseline and overfit models.
Bias Analysis: Subgroup of reviews that mention accent, language, or gender versus the rest of the data.
References: Important references that were used in this project.

# Data
- Source: https://github.com/vxuv/ratemyprofessor-dataset Real RMP reviews, loaded directly from GitHub in the notebook.
- Preprocessing: The 10,000 most recent reviews are used after removing place holder comments and comments under 20 characters.
- Labels: Raw sentiment strings are mapped into three categories: "Awful", "Neutral", and "Great."
Source: https://github.com/vxuv/ratemyprofessor-dataset Real RMP reviews, loaded directly from GitHub in the notebook.
Preprocessing: The 10,000 most recent reviews are used after removing place holder comments and comments under 20 characters.
Labels: Raw sentiment strings are mapped into three categories: "Awful", "Neutral", and "Great."
