---
title: "Fake News Detection by GNN"
date: 2025-06-29
author: "Arkadeb Manna"
words_per_minute : 100
read_time: true
tags :
    - Machine Learning
    - Project
    - Graph Neural Network
---

## Project Overview :
* This project focuses on classifying news articles into **Fake** and **Real** categories.
* It utilizes Graph Neural Networks (GNNs) on social and contextual interaction graphs.
* The system combines both structural graph data and textual semantic data.
* It achieves a reported highlight of **85% test accuracy**.

## Introduction
* Misinformation spreads rapidly on social networks, creating complex interaction graphs.
* The core objective is to leverage these interaction-style graphs for automated classification.
* The project uses the **UPFD dataset** (specifically the `politifact` variant).
* It implements a machine learning pipeline using **PyTorch** and **PyTorch Geometric**.

## Key Features
* **Graph Representation Learning:** Implements GraphSAGE encoders with both Global Attention and MLP classifier heads.
* **Textual Embeddings:** Integrates **BERT** to capture semantic features and user preferences.
* **Caching Mechanism:** Features a `BertTextEmbedder` with an SHA256-based embedding cache for efficient text processing.
* **Graph Analytics:** Utilizes **NetworkX** to build and analyze weighted interaction graphs.
* **Comprehensive Evaluation:** Tracks multiple metrics including Accuracy, Precision, Recall, and F1-score.
* **Robust Optimization:** Employs Binary Cross Entropy loss (`BCEWithLogitsLoss`) and Adam/AdamW optimizers.

## Real Life Application
* **Social Media Moderation:** Automatically flagging suspicious articles and misinformation propagation on platforms like X or Facebook.
* **Fact-Checking Assistance:** Providing investigative journalists with prioritized lists of highly suspicious news clusters.
* **Source Credibility Scoring:** Evaluating the trustworthiness of news sources based on user interaction and sharing graphs.
* **Trend Analysis:** Understanding how fake news diffuses through networks to design better intervention strategies.

## Conclusion
* The integration of GraphSAGE and BERT embeddings successfully captures both the propagation structure and text semantics of news.
* The baseline model demonstrates strong predictive performance, ranging from ~83.2% to 85% accuracy.
* **Future Improvements:** Addressing the class imbalance that occasionally affects validation F1 scores.
* **Next Steps:** Consolidating multiple notebook experiments into a single, reproducible Python script and updating deprecated PyG APIs.