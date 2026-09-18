<h1 align="center">From Dense Retrieval to Retrieval-Augmented Generation</h1>

<p align="center">
  MNLP 2026 coursework by Antonio Serra and Daniele Falanga.
</p>

## Overview

This repository contains two connected NLP projects: a dense text retrieval pipeline (HW1) and a retrieval-augmented generation and evaluation pipeline (HW2). The notebooks include experiments and saved results; the reports and final slides describe the methods and findings.

## Projects

- **HW1 - Dense retrieval:** compare DistilBERT and MiniLM bi-encoders, fine-tune with triplet loss and hard negatives, evaluate retrieval quality including MRR, and explore TinyBERT.
- **HW2 - RAG and evaluation:** use the fine-tuned HW1 MiniLM retriever with Qwen3-0.6B and SmolLM2-360M-Instruct. Compare Baseline, RAG and Oracle settings using EM, subEM and METEOR, LLM judges and human annotations. Extensions cover context compression, corrective prompting, alternative judges and Wikidata enrichment.

## Notebooks, Reports and Slides

| Material | Link |
| --- | --- |
| HW1 notebook | [MNLP_HW1.ipynb](notebooks/MNLP_HW1.ipynb) |
| HW2 notebook | [MNLP_HW2.ipynb](notebooks/MNLP_HW2.ipynb) |
| HW1 report | [Sentence Embeddings](docs/reports/MNLP_HW1_Report.pdf) |
| HW2 report | [Retrieval-Augmented Generation](docs/reports/MNLP_HW2_Report.pdf) |
| Final slides | [From Dense Retrieval to Retrieval-Augmented Generation](docs/slides/From_Dense_Retrieval_to_RAG.pdf) |

## Running the Notebooks

The notebooks use the Hugging Face dataset `sapienzanlp-course-materials/hw-mnlp-2026` and download pretrained models. Network access is required for these downloads; a GPU is recommended for training and generation.

1. Open the notebooks in Google Colab, or prepare a local Jupyter environment with `python -m pip install -r requirements.txt` and any additional dependencies used by the notebook setup cells.
2. Review the setup cells and adapt the Google Drive mounts, project directories and checkpoint paths to your environment. Local execution requires adapting Colab-specific code.
3. Run HW1 first to produce the fine-tuned retriever, or supply compatible existing checkpoints. Review `RUN_TRAINING` before execution; it is enabled in the supplied HW1 notebook.
4. Configure HW2 to use the fine-tuned MiniLM checkpoint and the required input files, then run the desired inference and evaluation sections. Human agreement analyses require the annotation files referenced by the notebook.

For a local Jupyter environment:

```bash
jupyter notebook notebooks/MNLP_HW1.ipynb
jupyter notebook notebooks/MNLP_HW2.ipynb
```

## Repository Contents

```text
.
|-- notebooks/
|   |-- MNLP_HW1.ipynb
|   `-- MNLP_HW2.ipynb
|-- docs/
|   |-- reports/
|   |   |-- MNLP_HW1_Report.pdf
|   |   `-- MNLP_HW2_Report.pdf
|   `-- slides/
|       `-- From_Dense_Retrieval_to_RAG.pdf
|-- requirements.txt
|-- .gitignore
`-- README.md
```

- `notebooks/`: project notebooks, including saved outputs.
- `docs/reports/`: the two homework reports.
- `docs/slides/`: final presentation.
- `requirements.txt`: Python dependency list.

Model checkpoints, standalone generation JSONL files and local caches are not included. Some stages require files produced by earlier stages or stored in the authors' Google Drive; the repository is not a self-contained bundle of all experiment artifacts.
