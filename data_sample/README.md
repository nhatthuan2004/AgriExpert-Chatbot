# Sample Data

This folder contains small public samples from the AgriExpert dataset for demonstrating the data schema and RAG knowledge format.

The full dataset is not included in this repository due to storage size and data usage constraints.

## Full dataset statistics

- 125,120 QA samples after augmentation and semantic similarity filtering
- 10,260 unique images
- 4 crops: tomato, pumpkin, cucumber, bitter melon
- 239 agricultural knowledge/rule entries for RAG
- 22-field structured QA schema

## Files

- `sample_qa.csv`: 100 QA samples selected across the four crops and multiple question types. Local image paths are masked for public release.
- `sample_rag_knowledge.csv`: 40 sample knowledge/rule rows used for RAG retrieval and controlled answer generation.

## Notes

These files are intended for schema inspection and lightweight testing only. They are not enough to reproduce the full training or evaluation results reported in the project.
