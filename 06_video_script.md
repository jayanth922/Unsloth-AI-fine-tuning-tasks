# Video Script: Mental Health Chatbot

**Host:** [Your Name]

## 1. Introduction
"In this video, we're building a **Mental Health Chatbot**. We'll fine-tune a Llama 3.2 model on a dataset of counseling conversations to make it empathetic and helpful."

## 2. Setup & Model
"We use `Llama-3.2-3B-Instruct`. The 'Instruct' version is already tuned for chat, which gives us a great head start."
*(Show cell 2)*

## 3. Data Preparation
"We use the `Amod/mental_health_counseling_conversations` dataset. The crucial part here is formatting. We use Unsloth's `get_chat_template` to automatically apply the Llama 3 chat format (User/Assistant roles) to our dataset."
*(Show cell 5)*

## 4. Training
"We run the `SFTTrainer`. By training on these specific conversations, the model learns the tone and style of a counselor."
*(Show cell 6 & 7)*

## 5. Inference
"Let's test it. I'll tell the bot I'm anxious about an interview. Let's see how it responds."
*(Show cell 8 output)*

## 6. Conclusion
"You can see how the model adopts a supportive and professional tone. Thanks for watching!"
