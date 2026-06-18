# Personal LinkedIn Agent

An AI-powered Gradio chatbot that represents you using your LinkedIn profile and personal summary. It uses Google Gemini (via OpenAI-compatible API) to answer questions in your voice and can record user interest or unanswered questions via tools.

---

## 🚀 What This Project Does

This project creates a personal AI agent that:

* Reads your LinkedIn PDF
* Uses your personal summary for context
* Chats as if it is you (professional persona)
* Records user emails or unknown questions
* Sends notifications using Pushover
* Runs as a simple Gradio web app

---

## 📁 Project Structure

```text id="proj1"
personal-linkedin-agent-clean/
│
├── app.py                  # Main AI agent + Gradio app
├── requirements.txt        # Python dependencies
├── README.md               # Project documentation
├── .env.example            # Environment variables template
│
└── me/
    ├── linkedin.pdf        # Your LinkedIn export (replace this)
    └── summary.txt         # Your personal summary (edit this)
```

---

## ⚙️ Setup Instructions

### 1. Clone the repository

```bash id="clone1"
git clone https://github.com/shrijayadavalli/personal-linkedin-agent.git
cd personal-linkedin-agent
```

---

### 2. Create a virtual environment

```bash id="venv1"
python -m venv .venv
source .venv/bin/activate   # Mac/Linux
```

---

### 3. Install dependencies

```bash id="install1"
pip install -r requirements.txt
```

---

## 🔐 Environment Variables Setup

Create a `.env` file in the root directory using `.env.example`.

```env id="env1"
GOOGLE_API_KEY=your_google_api_key_here
GEMINI_API_KEY=your_gemini_api_key_here

PUSHOVER_USER=your_pushover_user_key_here
PUSHOVER_TOKEN=your_pushover_token_here

HF_TOKEN=your_huggingface_token_here
```

---

## 🤖 API Setup (Important)

### Google Gemini API (FREE)

This project uses Google Gemini via Google AI Studio.

Steps:

1. Go to https://aistudio.google.com/
2. Sign in with your Google account
3. Click **Get API Key**
4. Create a new key
5. Copy and paste it into both:

   * `GOOGLE_API_KEY`
   * `GEMINI_API_KEY`

---

## 🔔 Pushover Setup (Notifications)

Pushover is used to send notifications when:

* A user shares their email
* The AI cannot answer a question

### Setup steps:

1. Go to https://pushover.net/
2. Create a free account
3. Verify your email
4. Copy your **User Key** from the dashboard
5. Create a new application
6. Copy the **API Token**
7. Add both to `.env`

---

## 📂 Required User Files

### LinkedIn PDF

Place your exported LinkedIn profile here:

```text id="file1"
me/linkedin.pdf
```

### Personal Summary

Edit this file:

```text id="file2"
me/summary.txt
```

Write a short description of yourself, skills, and background.

---

## ▶️ Run the Application

```bash id="run1"
python app.py
```

Then open the Gradio link shown in the terminal.

---

## 🧠 How It Works

* Loads your LinkedIn PDF and extracts text
* Loads your personal summary
* Uses Gemini AI to act as you
* Maintains conversation context
* Uses tools to:

  * Save user emails
  * Log unanswered questions
* Sends notifications via Pushover

---

## ⚠️ Important Notes

* Never commit your `.env` file
* Keep API keys private
* Always replace files in `me/` with your own data
* This project is for learning and personal AI agent building

---

## 💡 Tech Stack

* Python
* Gradio
* Google Gemini API
* OpenAI SDK (for Gemini compatibility)
* Pushover API
* PyPDF

---

## 📌 Goal of This Project

To build a personal AI assistant that represents you online using your own professional data, powered by modern LLM APIs.

---
