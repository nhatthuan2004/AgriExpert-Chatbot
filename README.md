# AgriExpert Chatbot

Vietnamese crop disease advisory chatbot using VLM + RAG + LLM.

## Overview
AgriExpert is a multimodal chatbot that receives a leaf image and a user question, extracts visual symptoms using a Vision-Language Model, retrieves agricultural knowledge using RAG, and generates a controlled Vietnamese advisory answer.

## Key Features
- Leaf image + Vietnamese question input
- VLM-based symptom extraction
- RAG knowledge retrieval from structured crop disease knowledge
- Controlled answer generation
- Safety constraints: avoid unsupported pesticide/dosage recommendations
- Gradio demo

## Dataset
- 125,120 QA samples
- 10,260 unique images
- 4 crops: tomato, pumpkin, cucumber, bitter melon
- 239 RAG knowledge/rule entries
- 22-field structured schema
- Includes symptoms, lesion location, severity, confidence, priority level, and linked knowledge IDs

## Method
Image + question → VLM structured output → RAG retrieval → LLM answer generation → safety-controlled response

## Results
| Metric | Method 1 | Method 2 |
|---|---:|---:|
| RAG Hit@5 | 0.822 | 1.000 |
| RAG Recall@5 | 0.264 | 0.521 |
| MRR | 0.633 | 0.970 |
| ROUGE-L | 0.308 | 0.412 |
| Token-F1 | 0.226 | 0.530 |

## Demo
Demo is provided in notebooks/05_gradio-vlm-rag-chatbot.ipynb.
A standalone app.py version will be added later.
<img width="1918" height="958" alt="image" src="https://github.com/user-attachments/assets/69654258-9431-4fbf-beeb-4850ed627e93" />


## How to Run
pip install -r requirements.txt
python app.py

## Limitations
- Image classification accuracy still needs improvement.
- Some visually similar diseases remain difficult.
- Full expert evaluation is needed before real agricultural deployment.
