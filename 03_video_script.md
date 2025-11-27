# Video Script: Reinforcement Learning (DPO)

**Host:** [Your Name]

## 1. Introduction
"In this video, we're diving into **Reinforcement Learning** using **DPO (Direct Preference Optimization)**. This technique helps align models with human preferences without needing a complex Reward Model."

## 2. Setup & Patching
"We import `PatchDPOTrainer` from Unsloth. This is crucial because it patches the standard TRL DPOTrainer to work efficiently with Unsloth's memory optimizations."
*(Show cell 2)*

## 3. Model Loading
"We're using `unsloth/zephyr-sft-bnb-4bit`. It's best to start DPO with a model that has already been Supervised Fine-Tuned (SFT)."
*(Show cell 2)*

## 4. Data Preparation
"We use the `mlabonne/orpo-dpo-mix-40k` dataset. The key here is that our data must have `chosen` and `rejected` columns, representing the preferred and non-preferred responses."
*(Show cell 5)*

## 5. Training
"We configure the `DPOTrainer`. Notice we set `ref_model = None`. Unsloth optimizes this so we don't need to load a second reference model into memory, saving a huge amount of VRAM."
*(Show cell 6 & 7)*

## 6. Conclusion
"And that's how you perform DPO with Unsloth! Thanks for watching."
