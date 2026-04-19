English–Vietnamese Neural Machine Translation

Overview
This project implements a neural machine translation (NMT) system for English–Vietnamese translation using a transformer-based architecture. The model is based on a pre-trained sequence-to-sequence transformer and fine-tuned for improved translation performance.

Model
Pretrained model: Helsinki-NLP/opus-mt-en-vi (MarianMT)
Architecture: Transformer-based Seq2Seq model
Fine-tuned on a subset of English–Vietnamese parallel corpus

Dataset
Source: HuggingFace Datasets – OPUS-100 English–Vietnamese subset
Dataset name: Helsinki-NLP/opus-100 (en-vi)
Corpus origin: OPUS (Open Parallel Corpus)
Type: Parallel text dataset (English ↔ Vietnamese sentence pairs)

Data Processing
Training subset: 1,000 sentence pairs (for fast experimentation)
Evaluation subset: 200 validation samples
Full dataset contains much larger parallel corpora from OPUS
Data Access Instructions

The dataset is automatically loaded using the HuggingFace datasets library:

from datasets import load_dataset
raw_datasets = load_dataset("Helsinki-NLP/opus-100", "en-vi")

No manual download is required. Internet access is needed when running the code for the first time.

Implementation
Framework: HuggingFace Transformers
Backend: PyTorch
Environment: Google Colab (GPU recommended)
Tokenizer: AutoTokenizer from MarianMT model
Evaluation metric: SacreBLEU

Results
BLEU score: 23.90
Validation loss improved from 1.758 → 1.732
Model shows reasonable performance on literal sentences, but struggles with idioms and figurative language.
Error Analysis (Qualitative)

The model performs well on standard sentences but has limitations with:

Idioms (e.g., “raining cats and dogs”)
Slang expressions (e.g., “kick the bucket”)
Metaphorical language

How to Run
Open the project in Google Colab

Install dependencies:

pip install transformers datasets sacrebleu torch
Run all cells sequentially
Model will automatically train and evaluate

Notes
This project uses a subset of the dataset for demonstration purposes
Full dataset training is recommended for production-level performance
Implementation includes both quantitative evaluation (BLEU) and qualitative error analysis
