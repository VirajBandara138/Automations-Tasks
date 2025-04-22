# 🧠 Telegram Mental Health Chatbot (Powered by n8n & GPT)

This project is a Telegram-based mental health chatbot built using **n8n**, **OpenAI GPT**, and **Google Sheets**. It allows users to send messages through Telegram and receive empathetic, AI-generated responses. The chatbot detects emotional tone and provides supportive replies. If the system detects a crisis, it sends an immediate alert to a predefined admin Telegram chat. All user interactions are logged to a Google Sheet for analysis or monitoring.

---

## 🔗 Technologies Used

- **n8n** – Workflow automation platform
- **Telegram Bot API** – For user interaction
- **OpenAI GPT (gpt-3.5)** – For sentiment detection and response generation
- **Google Sheets** – For logging user messages, bot replies, and emotional states

---

## ⚙️ Features

### ✅ User Interaction via Telegram
Users can message the chatbot on Telegram and receive compassionate AI-driven replies.

### 🧠 Emotion Detection
Each message is analyzed by GPT to determine the user’s emotional state:  
`happy`, `sad`, `anxious`, `angry`, or `crisis`.

### 🚨 Crisis Alerts
If the emotion is classified as "crisis", the system sends a Telegram alert to a specified admin chat ID for possible intervention.

### 📊 Conversation Logging
Every interaction (timestamp, user ID, user message, GPT reply, emotion) is logged to a Google Sheet for tracking and future analysis.

---

## 📋 How It Works (Workflow Overview)

1. **Telegram Trigger**: Starts when a user sends a message.
2. **OpenAI GPT Node**: Message is analyzed and a supportive reply is generated.
3. **IF Node (Crisis Detection)**: Checks for “crisis” emotions.
4. **Telegram Alert Node**: Sends an alert to the admin if a crisis is detected.
5. **Google Sheets Node**: Logs the interaction data.
6. **Telegram Send Message**: Sends the GPT reply back to the user.

---

## 🔐 Admin Setup

- Admin receives **crisis alerts** via Telegram using the admin chat ID: `5739827783`
- Google Sheet used for logs:  
  [Open Sheet](https://docs.google.com/spreadsheets/d/1roCA94uwm7ekVoAg-Ud2sP3p4CX-WYzN9uAoBOeo5XM/edit?usp=sharing)

---

## 📎 Credits

Built with ❤️ using [n8n](https://n8n.io), [Telegram Bot API](https://core.telegram.org/bots), [OpenAI](https://openai.com), and [Google Sheets](https://workspace.google.com/products/sheets/).
