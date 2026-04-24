# 🧠 CGS410: Investigating Dependency Grammar in LLMs

[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![Transformers](https://img.shields.io/badge/%F0%9F%A4%97-Transformers-orange)](https://huggingface.co/docs/transformers/index)

This project investigates whether large language models (LLMs) implicitly learn dependency grammar structures. We analyze the attention mechanisms of transformer-based models and compare the inferred dependency relations against gold-standard parses from the Universal Dependencies corpora.

## 🌟 Key Features

- **Attention Extraction:** Maps sub-word piece attention back to original word-level tokens.
- **Dependency Parsing:** Infers syntactic heads directly from self-attention weights.
- **Automated Evaluation:** Calculates Unlabeled Attachment Score (UAS) against gold-standard `.conllu` corpora.
- **Visualizations:** Generates heatmaps to identify which specific transformer layers and heads act as syntactic parsers.
- **Relation & Positional Analysis:** Evaluates model accuracy on specific dependencies (e.g., 'nsubj') and detects positional heuristics (e.g., heavily predicting the adjacent token).
- **Graph Visualization:** Draws directed dependency tree graphs for sentence syntax.

## Research Question

Do large language models (LLMs) implicitly learn dependency grammar structures similar to those found in human language, and how closely do the dependency relations inferred from model attention mechanisms match the gold-standard dependency parses in linguistic corpora?

## Hypothesis

Transformer-based LLMs develop latent representations of dependency grammar through the self-attention mechanism. The dependency structures inferred from attention patterns will significantly correlate with the gold-standard dependency structures available in annotated linguistic corpora.

## Collaborators

- Asheesh (240207)
- Saksham Gupta (240912)
- Nitin Kumar (240709)
- Sanjay Chaudhary (240933)
- Tanishq Singh Gurava (241089)

## Setup

1.  **Clone the repository:**
    ```bash
    git clone <your-repo-url>
    cd cgs410_dependency_parsing
    ```

2.  **Create a virtual environment and install dependencies:**
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    pip install -r requirements.txt matplotlib seaborn networkx
    ```

3.  **Download Data:**
    Download a corpus from [Universal Dependencies](https://universaldependencies.org/) (e.g., the English Web Treebank) and place the `.conllu` file inside the `data/` directory.
    
    *Note: There is a placeholder file `data/put_ud_corpus_here.txt` to help you locate the directory.*

## Usage

### 1. Run the Analysis
Run the main experiment script to analyze a corpus file and extract attention scores.

```bash
python main.py --model_name "bert-base-cased" --corpus_path "data/en_ewt-ud-train.conllu" --output_file "results/analysis.csv"
```

### 2. Visualize Results
After generating the `analysis.csv` file, run the analysis script to find the best-performing heads and generate a heatmap.

```bash
python analyze_results.py --input_file "results/analysis.csv" --heatmap_output "results/uas_heatmap.png"
```
