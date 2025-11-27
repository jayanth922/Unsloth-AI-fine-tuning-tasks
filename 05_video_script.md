# Video Script: Continued Pretraining (New Language)

**Host:** [Your Name]

## 1. Introduction
"In this video, we're doing something exciting: **Continued Pretraining**. We're going to teach an English-centric LLM to understand a new language, for example, Hindi."

## 2. Setup & Model
"We load `Llama-3.2-1B`. It's a great small model to experiment with."
*(Show cell 2)*

## 3. LoRA for Pretraining
"When teaching a new language, we need to be more aggressive. We set `r = 128` (a high rank) and crucially, we add `embed_tokens` and `lm_head` to the `target_modules`. This allows the model to learn new vocabulary embeddings."
*(Show cell 3)*

## 4. Data Preparation
"We use the **Oscar** dataset for Hindi. Unlike previous tasks where we had instructions, here we just feed raw text. This helps the model learn the syntax and grammar of the new language."
*(Show cell 4)*

## 5. Training with Packing
"We use `SFTTrainer` with `packing = True`. Packing combines multiple short text examples into one long sequence, making training much more efficient for pretraining tasks."
*(Show cell 5 & 6)*

## 6. Conclusion
"Continued pretraining is the first step to building a truly multilingual model. Thanks for watching!"
