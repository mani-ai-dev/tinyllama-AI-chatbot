# 🤖 AI Chatbot using TinyLlama + Streamlit

A conversational AI chatbot built with **TinyLlama-1.1B-Chat**, 
**Hugging Face Transformers**, and **Streamlit**. 
Designed and tested on **Google Colab** with GPU support.

---

## 🚀 Demo

> Ask the bot anything — general knowledge, coding questions, 
> math, or just have a conversation!

---

## 🧠 Model Used

| Property | Details |
|----------|---------|
| Model | TinyLlama/TinyLlama-1.1B-Chat-v1.0 |
| Parameters | 1.1 Billion |
| Type | Causal Language Model (Chat) |
| Source | Hugging Face 🤗 |

---

## 📁 Project Structure

tinyllama-chatbot/

│

├── app.py # Main Streamlit chatbot app

├── requirements.txt     # Python dependencies

├── .gitignore        # Files to ignore in git

└── README.md         # Project documentation

__ Output Images

---

## ⚙️ How It Works

1. User types a question in the Streamlit text input
2. The input is formatted using TinyLlama's chat template
3. The model generates a response using sampling-based decoding
4. The response is decoded and displayed in the UI

---

## 🛠️ Setup & Run (Google Colab)

### Step 1 — Install dependencies
```bash
!pip install streamlit transformers torch accelerate sentencepiece pyngrok
```

### Step 2 — Run the app
```bash
!streamlit run app.py &
from pyngrok import ngrok
public_url = ngrok.connect(8501)
print("App running at:", public_url)
```

---

## 📦 Requirements
streamlit
transformers
torch
accelerate
sentencepiece
---

## 💬 Example Prompts to Test

- `What is mercury?`
- `Write a Python function to reverse a string`
- `What is 15% of 200?`
- `List 3 benefits of drinking water`
- `Explain machine learning in 2 sentences`

---

## 🔧 Key Technical Decisions

| Setting | Value | Reason |
|--------|-------|--------|
| `do_sample` | True | Enables diverse responses |
| `temperature` | 0.7 | Balanced creativity vs accuracy |
| `top_k` | 50 | Limits to top 50 probable tokens |
| `max_new_tokens` | 200 | Enough for full answers |
| `torch_dtype` | float16 | Faster inference on GPU |

---

## ⚠️ Known Limitations

- Requires a **GPU runtime** in Colab for fast responses
- TinyLlama is a small model — answers may sometimes be basic
- No conversation memory (each question is independent)

---

## 👤 Author

**Manikanta**  
Built as part of a Prompt Engineering project  
Platform: Google Colab + Streamlit + ngrok

---
