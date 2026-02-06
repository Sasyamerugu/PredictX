# Causal RAG System for Conversational Analysis

## Overview
This project implements a **Causal Retrieval-Augmented Generation (RAG)** system to analyze customer service conversations and produce **explainable, evidence-backed answers** to analytical queries.

Instead of generating free-form text, the system focuses on:
- Identifying *why* outcomes occur
- Extracting causal factors
- Grounding explanations in real transcript evidence

---
## Project Structure
PredictX/
│
├── src/
│ └── main.py
│
├── data/
│ ├── Conversational_Transcript_Dataset.json
│ ├── queries.csv
│ └── submission_output.csv
│
├── Requirements.txt
├── README.md
└── technical_report.pdf

---

## How the System Works
1. Retrieve relevant conversations using sentence embeddings  
2. Retrieve relevant dialogue turns  
3. Tag turns with causal signals (rule-based, deterministic)  
4. Aggregate dominant causal factors  
5. Produce explainable output with evidence  
6. Support follow-up questions using session memory  

---

## Installation

pip install -r requirements.txt

## Running the System
python src/main.py

This will:

1.Read queries from data/queries.csv

2.Run the causal analysis pipeline

3.Write results to data/submission_output.csv

## Notes

No external LLM calls are required

All reasoning is transparent and auditable

Designed for analytical and compliance-focused use cases
