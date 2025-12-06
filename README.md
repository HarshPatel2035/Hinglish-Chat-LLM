# Hinglish WhatsApp Chatbot – Fine-Tuned Qwen 1.5B (LoRA)

A conversational Hinglish chatbot fine-tuned using:
- **Qwen 1.5B Instruct Model**
- **LoRA Parameter-Efficient Fine-Tuning**
- **1M+ Hinglish Everyday Conversation Dataset**
  (Abhishekcr448/Hinglish-Everyday-Conversations-1M)

---

## 🚀 Features
✔ Natural Hinglish responses  
✔ Flirty, casual WhatsApp-style chatting  
✔ Low-compute fine-tuning (LoRA)  
✔ Easily deployable anywhere  

---

## 📂 Project Structure

📁 Project/
├─ 📂 Hinglish-Everyday-Conversations-1M
├─ 📂 qwen_hinglish_whatsapp_lora
└─ 📄 README.md

---

## 🧠 Model Details
- Base Model: `Qwen/Qwen2.5-1.5B-Instruct
- Trainable Parameters: ~0.9% (LoRA)
- Training Platform: Google Colab T4 GPU
- Output Style: WhatsApp Hinglish tone 😎🔥

---

## ▶️ Quick Start
```python
from transformers import AutoTokenizer, AutoModelForCausalLM
import torch

model_path = "Harsh/Hinglish-Qwen-Chatbot"

tokenizer = AutoTokenizer.from_pretrained(model_path)
model = AutoModelForCausalLM.from_pretrained(model_path)

prompt = "Kya kar rahe ho?"
inputs = tokenizer(prompt, return_tensors="pt")
outputs = model.generate(**inputs, max_new_tokens=50)
print(tokenizer.decode(outputs[0]))
````

---

## 🛠 Future Work

* Add voice-based Hinglish chat
* Deploy as WhatsApp bot with Twilio
* Improve flirt / casual personality tuning
* Fine-tune safety & consistency more

---

## 📄 License

This project is released under the **Apache-2.0 License**.

---

💡 Suggestions, PRs & Stars ⭐ are welcome!


```
