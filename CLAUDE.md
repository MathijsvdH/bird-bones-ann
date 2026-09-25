# Bird bones neural network – school assignment

## Assignment
Build, train and test an artificial neural network with Keras on the
"Birds' Bones and Living Habits" dataset (Kaggle:
zhangjuefei/birds-bones-and-living-habits). Test at least two
hyperparameters and investigate their effect on learning. Deliverable is
a Jupyter notebook that describes the dataset (with reference), approach,
results, a confusion matrix with discussion, and a reflection. All
sources and tutorials used must be referenced.

## Tools
- Package management: uv only (uv add / uv run), never pip
- Python 3.12
- Keras via TensorFlow, no PyTorch
- Load data with kagglehub, fall back to data/ if the download fails

## How to work with me
- I'm an advanced-semester student, not a beginner. Readers are my
  teacher (expert) and me, so skip basic explanations
- Markdown cell before each code step: one or two plain sentences
  saying what the step does, e.g. "Download the dataset from Kaggle
  and load it." Human-written, no filler or textbook tone
- Structure: `##` per main step, `###` short subheader per sub-step
  (e.g. `### Missing values`), then the code. A line of text under the
  subheader only when it adds something; the header alone is fine
- Never explain libraries, syntax or standard tools (pandas, try/except,
  kagglehub...). Only mention a choice when it isn't obvious to an expert
- Build the notebook step by step; only do the step I ask for
- Keep code simple and readable over clever
- Set random seed 1 for reproducibility
- Keep a References section at the end and add sources as we go
- Notebook file: ann.ipynb