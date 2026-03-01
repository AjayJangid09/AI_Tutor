# AI Tutor RAG System

A production-style open-source RAG AI Tutor that reads PDFs/text, retrieves relevant context using hybrid search, and generates grounded answers using Qwen2.5 with strong safety guardrails.

## Features

* PDF & text ingestion
* Hybrid retrieval (Dense + BM25 + Reranker)
* Qwen2.5 based answer generation
* Guardrails (PII masking, toxicity, injection, hallucination check)
* Multi-turn conversation memory
* Evaluation metrics support

## Installation

```bash
git clone <your-repo-url>
cd ai-tutor-rag
pip install -r requirements.txt
python -m spacy download en_core_web_sm
```

## How to Run

```python
loader = DocumentLoader()
docs = loader.load_multiple(["sample.pdf"])

kb = KnowledgeBase(config)
kb.ingest(docs)

tutor = TutorSystem(config)
result = tutor.run("Your question here")
print(result.final_answer)
```

## Author

Ajay Jangid
