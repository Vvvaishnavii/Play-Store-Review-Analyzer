# 📊 Play Store Review Analyzer – AI Automation Workflow

## Overview

This project presents the design and implementation of an **AI-powered automation workflow** that analyzes Google Play Store reviews and generates actionable product insights.

The workflow is built using a **node-based automation approach (n8n-style design)** and leverages **LLM-based analysis (Gemini)** to convert unstructured user reviews into structured insights for product teams.

> ⚠️ **Note:** This repository focuses on **system design and workflow logic**, as required by the assignment. The workflow is designed to be production-ready but does not require live execution.

---

## Key Capabilities

- Automated daily fetching of Play Store reviews  
- Cleaning and normalization of noisy user-generated text  
- AI-driven sentiment analysis  
- Extraction of bugs, complaints, and feature requests  
- Aggregation of insights into a concise daily summary  
- Automated delivery of insights via email  

---

## Workflow Architecture

The system follows a **linear, modular pipeline**, where each node performs a single responsibility and passes structured output to the next node.

### High-Level Flow

1. Schedule trigger (daily execution)  
2. Fetch Play Store reviews via HTTP  
3. Filter and clean reviews  
4. Sentiment analysis using Gemini  
5. Parse and normalize AI output  
6. Aggregate all reviews  
7. Extract insights (bugs, complaints, features)  
8. Generate daily summary  
9. Send email to stakeholders  

---

## Workflow Diagram

**Figure 1:** End-to-end automation pipeline for Play Store review analysis.

The diagram below represents the actual workflow implemented in the automation tool.

*(Refer to the attached workflow screenshots in the repository.)*

---

## Node-wise Description

### 1. Schedule Trigger
- Triggers the workflow on a daily schedule  
- Ensures automated, hands-free execution  

### 2. Fetch Play Store Reviews (HTTP Request)
- Retrieves the latest app reviews from the Play Store  
- Acts as the data ingestion layer  

### 3. Filter & Clean Reviews (Code Node)
- Removes empty, duplicate, or irrelevant reviews  
- Normalizes text for AI processing  

### 4. Sentiment Analysis (Gemini AI)
- Classifies each review as positive, neutral, or negative  
- Returns structured JSON output  

### 5. Parse Sentiment Output
- Converts AI responses into consistent structured fields  
- Ensures downstream reliability  

### 6. Bundle All Reviews
- Aggregates all processed reviews into a single dataset  
- Prepares data for insight extraction  

### 7. Extract Insights (Gemini AI)
- Identifies common complaints, bugs, and feature requests  

### 8. Generate Daily Summary
- Produces a short, product-team-friendly summary  
- Highlights key issues and wins  

### 9. Send Daily Report (Email)
- Sends the generated summary to stakeholders  

---

## Example Output

> *“Most negative reviews today mention frequent app crashes after the latest update.  
> Users appreciate the new interface but report slow load times.  
> Priority recommendation: address stability issues before feature expansion.”*

---

## Design Strengths

- Handles noisy and unstructured user-generated text  
- Combines deterministic logic with AI for reliability  
- Modular design enables easy future extensions  
- Scalable for large review volumes  
- Clear separation of responsibilities across nodes  

---

## AI Usage Disclosure

AI (Gemini) was used for:
- Sentiment analysis  
- Insight extraction  
- Summary generation  

All AI outputs are structured and validated before further processing.

---

## Repository Structure

├── README.md
│
├── docs/
│   ├── system-design.md
│   ├── data-flow-diagram.png
│   


---

## Conclusion
This project demonstrates a **clean, professional automation design** that converts raw user feedback into meaningful product insights using AI and workflow orchestration.
It reflects real-world product analytics practices and aligns with the assignment’s emphasis on **design thinking, scalability, and clarity**.


