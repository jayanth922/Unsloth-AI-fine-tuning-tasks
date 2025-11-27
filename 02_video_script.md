# Video Script: LoRA Fine-tuning Smollm2-135M

**Host:** [Your Name]

## 1. Introduction
"Welcome back! In this video, we're doing **LoRA Fine-tuning** on the same `Smollm2-135M` model. LoRA (Low-Rank Adaptation) is much more memory efficient than full fine-tuning."

## 2. Setup & Loading
"We install Unsloth and load the model. This time, we set `load_in_4bit = True` to take advantage of quantization."
*(Show cell 1 & 2)*

## 3. LoRA Configuration
"Here is the magic step. We use `FastLanguageModel.get_peft_model` to attach LoRA adapters. We're setting `r = 16`, which is the rank of the adapters. We target all linear layers (`q_proj`, `k_proj`, etc.) for maximum effectiveness."
*(Show cell 3)*

## 4. Data Preparation
"We use the same Alpaca dataset as before."
*(Show cell 4)*

## 5. Training
"We run the `SFTTrainer`. Because we are using LoRA, we are only training a fraction of the parameters, which makes this process much faster and lighter on VRAM."
*(Show cell 5 & 6)*

## 6. Inference
"Let's ask the model to list benefits of exercise."
*(Show cell 7 output)*

## 7. Conclusion
"LoRA is a powerful technique for adapting LLMs efficiently. Thanks for watching!"
