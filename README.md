# 🧠 CGS410: Investigating Dependency Grammar in LLMs

[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![Transformers](https://img.shields.io/badge/%F0%9F%A4%97-Transformers-orange)](https://huggingface.co/docs/transformers/index)

This project investigates whether large language models (LLMs) implicitly learn dependency grammar structures. We analyze the attention mechanisms of transformer-based models and compare the inferred dependency relations against gold-standard parses from the Universal Dependencies corpora.

## Research Question

Do large language models (LLMs) implicitly learn dependency grammar structures similar to those found in human language, and how closely do the dependency relations inferred from model attention mechanisms match the gold-standard dependency parses in linguistic corpora?

## Hypothesis

Transformer-based LLMs develop latent representations of dependency grammar through the self-attention mechanism. The dependency structures inferred from attention patterns will significantly correlate with the gold-standard dependency structures available in annotated linguistic corpora.

##Methodolgy

1. Model Selection
Use a pre-trained transformer-based language model (e.g., GPT-style or BERT-style models)
and analyze its attention heads.
2. Sentence Dataset
Extract sentences from Universal Dependencies (UD) corpora, which provide gold-standard
dependency annotations.
3. Attention Analysis
○ Compute attention distributions between tokens across layers and heads.
○ Identify attention patterns that correspond to syntactic dependencies.
4. Dependency Extraction
Convert high-attention links between tokens into predicted dependency edges and represent
them as directed graphs

## Collaborators

- Saksham Gupta (240912)
- Nitin Kumar (240709)
- Sanjay Chaudhary (240933)
- Tanishq Singh Gurava (241089)
- Asheesh (240207)



