# Video Script: Export to Ollama (GGUF)

**Host:** [Your Name]

## 1. Introduction
"In this final video, we're going to take our fine-tuned model and **export it to GGUF format**. This allows us to run the model locally on our laptop using **Ollama**."

## 2. Setup & Training
"We setup and train the model just like before. I'm skipping ahead to the export part."
*(Show cells 1-8 briefly)*

## 3. Exporting to GGUF
"Here is the magic command: `model.save_pretrained_gguf`. We specify the quantization method, for example `q8_0` for 8-bit quantization. Unsloth handles all the complex conversion logic for us."
*(Show cell 9)*

## 4. Running in Ollama
"Once the file is saved (it will be named something like `model-unsloth.Q8_0.gguf`), we can import it into Ollama."

"In your terminal, you would run:"
```bash
ollama create my-finetuned-model -f Modelfile
ollama run my-finetuned-model
```

## 5. Conclusion
"And that's it! We've covered everything from full fine-tuning to RL and finally exporting for local deployment. Unsloth makes all of this incredibly easy. Thanks for watching!"
