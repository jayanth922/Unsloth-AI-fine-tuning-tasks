# Video Script: RL with GRPO (Reasoning)

**Host:** [Your Name]

## 1. Introduction
"In this video, we're exploring **GRPO (Group Relative Policy Optimization)**. This is a cutting-edge Reinforcement Learning technique used for reasoning models, similar to how DeepSeek R1 was trained."

## 2. Setup & Patching
"We use `PatchFastRL` to enable GRPO support in Unsloth. This allows us to use the `GRPOTrainer` efficiently."
*(Show cell 2)*

## 3. Model Loading
"We're using `Llama-3.2-3B-Instruct`. Reasoning tasks often benefit from slightly larger or more capable base models than the 135M one we used earlier."
*(Show cell 2)*

## 4. Data & Reward Function
"We use the **GSM8K** dataset, which contains math problems. The core of GRPO is the **Reward Function**. Here, we define a simple function that checks if the model's generated answer matches the ground truth. In a real scenario, you'd parse the output more carefully."
*(Show cell 5)*

## 5. Training
"We initialize the `GRPOTrainer`. It will generate multiple outputs for each prompt, score them using our reward function, and optimize the model to prefer the high-scoring paths."
*(Show cell 6 & 7)*

## 6. Conclusion
"GRPO is powerful for teaching models *how* to think, not just what to say. Thanks for watching!"
