English–Vietnamese Neural Machine Translation

Overview

This project implements a neural machine translation (NMT) system for English–Vietnamese translation using a transformer-based model.

Model

* Pretrained model: Helsinki-NLP/opus-mt-en-vi (MarianMT)
* Fine-tuned on a subset of the OPUS dataset

Dataset

* Source: OPUS corpus (English–Vietnamese)
* Size: 1,000 sentence pairs
* Split: 80% train, 10% validation, 10% test

Implementation

* Framework: HuggingFace Transformers
* Backend: PyTorch
* Environment: Google Colab (GPU)

Results

* BLEU score: 23.90
* Validation loss decreased from 1.758 → 1.732

How to Run

1. Open the project in Google Colab
2. Install required libraries:
   pip install transformers datasets sacrebleu
3. Run all cells to train and evaluate the model

Notes

* Full implementation code is provided in Appendix A of the report.
* This project focuses on both quantitative evaluation and linguistic error analysis.
