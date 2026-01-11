Vibe AI Hiring Assignment – Empathetic Chatbot Fine-Tuning

This repository contains my submission for the Vibe AI first-round hiring assignment.
It implements a multi-task fine-tuning pipeline for an open-weight language model
using parameter-efficient fine-tuning.

Model and Setup

Base model: Qwen Qwen2.5-7B-Instruct
Fine-tuning: QLoRA with 4-bit quantization and LoRA adapters
Frameworks: HuggingFace Transformers, Datasets, PEFT
Environment: Google Colab with GPU support

Only LoRA adapters are trained and saved. The base model remains frozen.

Datasets

EmpatheticDialogues for user prompts
GoEmotions for emotion classification supervision
ESConv for emotional support strategy classification

Missing labels are handled using masked loss computation.

Training

A custom Trainer computes a multi-task loss using emotion and strategy
classification objectives. Language modeling loss is not included.

Artifacts

Saved LoRA adapters, tokenizer files, and training metrics are stored
in the results directory.

How to Run

Open training.ipynb in Google Colab, enable GPU, and run all cells.

Limitations

EQ-Bench evaluation, preference alignment, and safety regularization
are not included and are identified as next steps.

Author

Sivasri
GitHub: replace with your profile URL

cc: ahan-2000
