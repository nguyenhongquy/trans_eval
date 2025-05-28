# Explainable Translation Evaluation with Generative AI

This repository contains a reimplementation of a translation quality assurance (QA) system designed for explainable, scalable evaluation using open-source Large Language Models (LLMs). Originally developed during an industrial internship at Mercedes-Benz, the system has been adapted for public release with open-source models. The original implementation remains proprietary and cannot be shared due to NDA restrictions.

## Project Overview

**Goal:**  
To develop a semi-automated, explainable QA pipeline that supports human translation review by detecting, explaining, and correcting translation errors—without requiring a reference translation.

**Key Features:**
- **Reference-less evaluation:** Inputs include source, target, and context only.
- **Three-part output:** Error label (`OK`/`Error`), explanation, and suggested correction.
- **Prompt-based orchestration:** Uses structured prompting to enable explainable evaluations.
- **Terminology-aware and domain-adaptable:** Includes integration of enterprise glossaries and domain-specific rules.

## Methodology

We explore and benchmark several prompting strategies:

- **CLA (Checklist-based Language Assessment):** Single-step evaluation with structured checklists.
- **NEXUS (Nodal Evaluation and Synthesis):** Multi-step Least-to-Most prompting to improve reasoning and correction quality.
- **RAG Extensions:** Integrate retrieved terminology and domain-specific constraints into the prompts.

## Evaluation

- **Metrics:** Precision, Recall, F1 for detection; BLEU, ROUGE, METEOR for refinement; FINE metrics for nuanced revision assessment.
- **Datasets:** Evaluated on two enterprise domains—Infotainment and OneWeb—with different linguistic profiles and error types.

## Results

- **CLA** excels in error detection, especially for subtle issues.
- **NEXUS** performs better in generating accurate corrections.
- **RAG and RAG+** significantly boost terminology-related performance.

## Coming Soon

- ✅ Open-source implementation using models like LLaMA or Qwen
- ✅ Example data and configs
- ✅ Modular prompting components
- ✅ Evaluation scripts and sample outputs

## Acknowledgments

This project was originally developed as part of a master's thesis titled *Enhancing In-Context Learning for Explainable Translation Evaluation with Generative AI – from Research to Business Integration*.

Supervised by Dr. Agnieszka Faleńska and conducted with the support of the Translation R&D and Language Technology teams at Mercedes-Benz AG.
