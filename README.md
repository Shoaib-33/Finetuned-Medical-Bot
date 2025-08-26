# Finetuned-Medical-Bot
This repository contains a workflow to fine-tune a **Large Language Model (LLM)** on a **medical domain dataset** using:

-  **[Unsloth](https://github.com/unslothai/unsloth)** → fast dataset preparation & efficient training  
-  **[LoRA (Low-Rank Adaptation)](https://arxiv.org/abs/2106.09685)** → parameter-efficient fine-tuning  
-  **[TRL](https://github.com/huggingface/trl)** → `SFTTrainer` for supervised fine-tuning  

The training pipeline supports **Complex Chain-of-Thought (CoT) reasoning** and can be adapted to other instruction-tuning tasks.

---

##  Dataset Structure

The dataset is expected to include:

| Column        | Description                              |
|---------------|------------------------------------------|
| `Question`    | The medical question or input prompt     |
| `Complex_CoT` | (Optional) step-by-step reasoning text   |
| `Response`    | The target/ground-truth medical answer   |
| `texts`       | Preprocessed training text (if generated)|

---
