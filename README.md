<h1 align="center">RAG and Qualitative NLP Analysis</h1>

<p align="center">
  Notebook-based NLP projects focused on generation analysis and RAG evaluation.
</p>

## Overview

This repository contains university NLP projects developed as notebooks. The work focuses on practical evaluation of generation behavior, retrieval-augmented generation and qualitative analysis of model outputs.

The included analysis files document failure modes and validation checks such as noisy context effects, positional bias and ambiguous generations. Reports and slides provide the higher-level discussion, while the notebooks contain the executable workflow.

## Key Features

- Notebook-based NLP experimentation.
- RAG-style generation and evaluation workflow.
- Qualitative analysis of generation failures.
- Positional-bias and noisy-context validation reports.
- Original reports and final slides included in `docs/`.

## Repository Structure

- `MNLP_HW1.ipynb`: first project notebook.
- `MNLP_HW2.ipynb`: second project notebook focused on generation/RAG evaluation.
- `analysis/`: qualitative-analysis evidence files.
- `docs/`: reports, final slides, prompt notes and screenshot.

## Installation

```bash
python -m pip install -r requirements.txt
```

## Run

```bash
jupyter notebook MNLP_HW1.ipynb
jupyter notebook MNLP_HW2.ipynb
```

## Notes

Long-running outputs, checkpoints, JSONL generations and local caches were excluded from the public version.

