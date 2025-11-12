# Session 3 — Applied Natural Language Processing

This repository contains the materials for **Session 3: Sentence-Level Analysis** of the *Applied NLP* course.  
- Slides: see [`slides/`](./slides/) folder  
- Notebooks: see [`notebooks/`](./notebooks/) folder 
---

## Session Outline

This session covers five key approaches to analyzing text at the sentence level, demonstrating various computational methods for measuring linguistic complexity, readability, and semantic relationships. All notebooks use Lewis Carroll's two Alice books as example texts for comparative literary analysis.

### Notebooks Overview

**1. Sentence Length & Distribution** (`1_AppliedNLP_Session3_Sentence_Length.ipynb`)
- Split text into sentences using regex-based sentence boundary detection
- Calculate average sentence length in tokens and characters
- Visualize sentence length distributions using histograms
- Compare sentence length patterns across two books
- Statistical analysis: mean, median, min, max values

**2. Readability Scores** (`2_AppliedNLP_Session3_Readability.ipynb`)
- Implement syllable counting for English words
- Calculate Flesch Reading Ease scores
- Calculate Flesch-Kincaid Grade Level scores
- Interpret readability metrics (grade level equivalents)
- Compare readability between texts using bar charts
- Understanding: higher Flesch scores = easier reading, lower grade levels = easier reading

**3.1 Sentence Embeddings - Basic** (`3_1_AppliedNLP_Session3_Sentence_Embeddings.ipynb`)
- Introduction to sentence embeddings and transformer-based encoders
- Using Sentence-BERT (all-MiniLM-L6-v2 model) to encode sentences
- Converting sentences to 384-dimensional semantic vectors
- Visualizing embeddings in 2D space using PCA (Principal Component Analysis)
- Computing cosine similarity between sentence pairs
- Creating similarity heatmaps and identifying semantically similar sentences
- Applications: semantic search, duplicate detection, content recommendation

**3.2 Sentence Embeddings - Advanced (BONUS)** (`3_2_AppliedNLP_Session3_Sentence_Embeddings_Advanced.ipynb`)
- Advanced extension of notebook 3.1 (complete basic notebook first)
- Extractive summarization: selecting key sentences from full books
- Multi-dimensional visualization (2D, 3D PCA projections)
- K-Means clustering to discover thematic groups automatically
- Cross-book semantic similarity analysis
- Quantitative comparative literature: measuring narrative parallels
- Six-panel comprehensive visualization dashboard
- Cluster coherence analysis and thematic interpretation

**4. Clause Density / Subordination** (`4_AppliedNLP_Session3_Clause_Density.ipynb`)
- Understanding clauses: independent vs subordinate clauses
- Measuring syntactic complexity through subordinating conjunctions
- Detecting clause markers using regex patterns (that, which, who, when, because, etc.)
- Computing clause density (clauses per 10 tokens)
- Why it matters: cognitive load, writing maturity, genre differences
- Visualizing complexity distributions with histograms and box plots
- Identifying the most syntactically complex sentences
- Comparative analysis of clause usage between books

**5. Sentence Types & Dialogue Ratio** (`5_AppliedNLP_Session3_Sentence_Types_and_Dialogue.ipynb`)
- Classifying sentences by type: dialogue, questions, exclamations, narrative
- Detecting dialogue using quotation mark patterns (both straight and curly quotes)
- Understanding limitations of simple heuristics vs full dialogue parsers
- Analyzing narrative pacing through dialogue ratio
- Reconstructing sentences with punctuation after regex splitting
- Why sentence types matter: genre markers, author style, narrative pacing
- Dual visualization: bar charts and side-by-side pie charts
- Comparative analysis of narrative style between books


## Environment Setup

Before starting, please **fork this repository** and create a fresh Python virtual environment.  
All required libraries are listed in `requirements.txt`.

Note: If you encounter errors during `pip install`, try removing the version pinning for the failing package(s) in `requirements.txt`.  
On Apple M1/M2 systems you may also need to install additional system packages.

---

### macOS / Linux (bash/zsh)

```bash
# Select Python version (if using pyenv)
pyenv local 3.11.3

# Create and activate virtual environment
python -m venv .venv
source .venv/bin/activate

# Upgrade pip and install dependencies
pip install --upgrade pip
pip install -r requirements.txt
```

### Windows (PowerShell)
```bash
# Select Python version (if using pyenv)
pyenv local 3.11.3

# Create and activate virtual environment
python -m venv .venv
.venv\Scripts\Activate.ps1

# Upgrade pip and install dependencies
python -m pip install --upgrade pip
pip install -r requirements.txt
```

### Windows (Git Bash)
```bash
# Select Python version (if using pyenv)
pyenv local 3.11.3

# Create and activate virtual environment
python -m venv .venv
source .venv/Scripts/activate

# Upgrade pip and install dependencies
python -m pip install --upgrade pip
pip install -r requirements.txt
```

You're now ready to run the session notebooks!

Deactivate the environment when you're done:
```bash
deactivate
```

---

## License

Text data of two Alice books is from Project Gutenberg (public domain).

