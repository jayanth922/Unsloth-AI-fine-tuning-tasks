# Unsloth AI Fine-tuning Tasks Collection

![Unsloth AI](https://img.shields.io/badge/Unsloth-Fast%20Fine--Tuning-blue)
![Python](https://img.shields.io/badge/Python-3.10+-yellow)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange)

This repository contains a comprehensive collection of **7 Advanced Fine-tuning Tasks** implemented using [Unsloth AI](https://github.com/unslothai/unsloth). Unsloth allows for 2x faster training and 70% less memory usage, making it possible to fine-tune LLMs on consumer hardware (like free Colab T4 instances).

Each task includes a complete **Jupyter Notebook** and a **Video Script** explaining the process.

## 📚 Table of Contents

1.  [Full Fine-tuning (Smollm2 135M)](#1-full-fine-tuning-smollm2-135m)
2.  [LoRA Fine-tuning (Smollm2 135M)](#2-lora-fine-tuning-smollm2-135m)
3.  [Reinforcement Learning (DPO/ORPO)](#3-reinforcement-learning-dpoorpo)
4.  [RL with GRPO (Reasoning)](#4-rl-with-grpo-reasoning)
5.  [Continued Pretraining (New Language)](#5-continued-pretraining-new-language)
6.  [Mental Health Chatbot](#6-mental-health-chatbot)
7.  [Export to Ollama (GGUF)](#7-export-to-ollama-gguf)

---

## 🛠️ Prerequisites

To run these notebooks, you can use Google Colab (free tier is sufficient for most tasks) or a local machine with an NVIDIA GPU.

**Installation:**
```bash
pip install unsloth
pip install --no-deps "unsloth[colab-new] @ git+https://github.com/unslothai/unsloth.git"
```

---

## 1. Full Fine-tuning (Smollm2 135M)
**Notebook:** [`01_full_finetuning_smollm2.ipynb`](./01_full_finetuning_smollm2.ipynb)

Youtube Demo : https://youtu.be/uomRuBPA8Qs

Demonstrates how to perform a full parameter fine-tune on the ultra-lightweight `HuggingFaceTB/SmolLM2-135M` model. This is ideal for understanding the basics of SFT (Supervised Fine-Tuning) without the complexity of adapters.

## 2. LoRA Fine-tuning (Smollm2 135M)
**Notebook:** [`02_lora_finetuning_smollm2.ipynb`](./02_lora_finetuning_smollm2.ipynb)

Youtube Demo : https://youtu.be/6fbyxz-1QZQ

Implements **LoRA (Low-Rank Adaptation)** on the same Smollm2 model. This shows the efficiency of LoRA compared to full fine-tuning, using significantly less memory while achieving comparable results.

## 3. Reinforcement Learning (DPO/ORPO)
**Notebook:** [`03_rl_dpo.ipynb`](./03_rl_dpo.ipynb)

Youtube Demo : https://youtu.be/9Vb0NfZXB0Y

Uses **Direct Preference Optimization (DPO)** to align a model (`unsloth/zephyr-sft-bnb-4bit`) with human preferences. We use the `mlabonne/orpo-dpo-mix-40k` dataset containing "chosen" vs "rejected" responses.

## 4. RL with GRPO (Reasoning)
**Notebook:** [`04_rl_grpo.ipynb`](./04_rl_grpo.ipynb)

Youtube Demo : https://youtu.be/Z7X_KFSefLc

Explores **GRPO (Group Relative Policy Optimization)**, a cutting-edge technique for reasoning tasks. We train `Llama-3.2-3B-Instruct` on the **GSM8K** math dataset, rewarding the model for generating correct answers.

## 5. Continued Pretraining (New Language)
**Notebook:** [`05_continued_pretraining.ipynb`](./05_continued_pretraining.ipynb)

Teaches an LLM (`Llama-3.2-1B`) a completely new language (Hindi) using **Continued Pretraining** on the Oscar dataset. This involves training embedding layers and using raw text data.

## 6. Mental Health Chatbot
**Notebook:** [`06_mental_health_finetune.ipynb`](./06_mental_health_finetune.ipynb)

Fine-tunes `Llama-3.2-3B-Instruct` to act as an empathetic Mental Health Counselor. We use the `Amod/mental_health_counseling_conversations` dataset and apply a specific chat template for optimal interaction.

## 7. Export to Ollama (GGUF)
**Notebook:** [`07_ollama_export.ipynb`](./07_ollama_export.ipynb)

The final step in the pipeline: exporting your fine-tuned model to **GGUF format**. This allows you to run your custom model locally using **Ollama**.

---

## 🤝 Credits

-   **Unsloth AI**: For the incredible library that makes this possible.
-   **Hugging Face**: For the models and datasets.

## 📄 License

This project is licensed under the Apache 2.0 License.
