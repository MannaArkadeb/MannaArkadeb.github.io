---
title: "Voretx Financial Agent"
date: 2025-11-30
author: "Arkadeb Manna"
words_per_minute : 100
read_time: true
tags :
    - Machine Learning
---

## Project Overview : End-to-end, AI-driven financial platform that automates portfolio management, financial research, and user onboarding. It combines reinforcement learning, retrieval-augmented generation (RAG), and real-time data streaming to provide risk-adaptive, explainable, and fully compliant investment strategies.

## Introduction 

Vortex is an integrated financial platform that combines reinforcement learning-based portfolio optimization, retrieval-augmented generation for financial research, and comprehensive KYC verification into a unified system. Built on Pathway's real-time data processing capabilities and leveraging modern LLM architectures, Vortex addresses critical challenges in automated portfolio management including risk-adaptive allocation, explainable AI decisions, and regulatory compliance through robust KYC workflows. The platform features a Next.js dashboard for user interaction, a Flask orchestration layer, and microservices for each specialized domain.

## Key Features

### 1. **Portfolio Management (SmartFolio)**
- **Challenge:** Traditional portfolio systems lack adaptability to individual risk profiles and market dynamics.
- **Solution:** PPO-based reinforcement learning with Heterogeneous Graph Attention Networks (HGAT) enables dynamic portfolio allocation that adapts to market conditions and user risk tolerance for 
- **Monthly Fine-tuning:** Policy Transfer Regularization (PTR) enables continuous model improvement without catastrophic forgetting.
- **Explainability:** LangGraph-based agents generate human-readable explanations for portfolio decisions.

### 2. **Financial RAG (FinRAG)**
- **Challenge:** Generic retrieval systems fail to capture domain-specific nuances in financial documents.
- **Solution:** Pathway-powered vector store with real-time document ingestion and specialized retrieval tools for financial analysis.
- **Multi-Source Retrieval:** Aggregates data from news articles, SEC filings, and fundamental data sources.
- **Ensemble Scoring:** Combines sentiment analysis, technical indicators, and fundamental metrics for stock scoring.
- **MCP Server:** Model Context Protocol server enables agentic integrations with external tools.

### 3. **KYC Verification**
- **Challenge:** Manual document verification is slow, error-prone, and lacks consistency.
- **Solution:** Automated document parsing using PaddleOCR with cross-document validation and ML-based risk scoring.
- **Document Support:** PAN Card, Aadhaar Card, and ITR documents with automatic field extraction.
- **Video Verification:** Selfie video analysis with face matching (Aadhaar-to-PAN, PAN-to-Video) and liveness detection.
- **Risk Scoring:** ML model evaluates investor risk based on questionnaire responses and financial data.

### 4. **Real-time Streaming Pipeline**
- **Challenge:** Batch processing introduces latency in portfolio updates and market data ingestion.
- **Solution:** Kafka-based streaming architecture enables real-time stock data ingestion and processing.
- **Stock Data Producer:** Streams OHLCV data from multiple sources to Kafka topics.
- **Consumer Pipeline:** Calculates display features (daily change, trend, volatility) and triggers monthly fine-tuning.
- **User Stream:** Processes user onboarding data for KYC workflows.

## Results

**VortEx Agent vs Expert Trajectories vs Benchmarks Performance (2025)**

| Metric | VortEx (Risk Score 0.7) | VortEx (Risk Score 0.3) | Expert Trajectories (Baseline) | Benchmark | NIFTY 50 |
| :--- | :---: | :---: | :---: | :---: | :---: |
| Annual Return (%) | 31.92 | 29.86 | 19.20 | 14.02 | 9.05 |
| Annual Volatility (%) | 15.40 | 15.25 | 25.98 | 14.46 | 14.09 |
| Sharpe Ratio | 1.80 | 1.71 | 0.68 | 0.91 | 0.68 |
| Max Drawdown (%) | -10.39 | -10.21 | -13.35 | N/A | -11.00 |