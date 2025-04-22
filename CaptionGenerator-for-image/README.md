# 📸 Social Media Image Caption Generator – n8n Workflow

This **n8n workflow** automates the process of generating engaging captions for images uploaded to social media platforms. Whether you're a content creator, marketer, or just looking to enhance your online presence, this automation streamlines your captioning process using AI.

---

## 🚀 Features

- 🔁 Automated trigger when a new image is uploaded (e.g., via webhook, Google Drive, Telegram, etc.)
- 🧠 AI-powered caption generation using OpenAI (or other LLM services)
- 📝 Custom caption styles (e.g., professional, funny, inspirational, product-focused)
- 🌍 Supports hashtags and emoji enhancements
- 📤 Ready to integrate with social media schedulers like Buffer, Hootsuite, or direct posting via API

---

## 🔧 Workflow Steps

1. **Trigger Node** – Detects new image upload (e.g., via webhook, Telegram bot, or Google Drive)
2. **Image Metadata Extraction** *(optional)* – Extracts details like filename, tags, or location
3. **AI Request Node** – Sends image context or description to AI model to generate a caption
4. **Format Response** – Cleans and formats the caption with hashtags/emojis
5. **Store / Send** –  
   - Save to Google Sheets/Notion  
   - Send via Telegram/Email for review  
   - Or automatically post to social media (if integrated)

---

## 🧠 Example Prompt for AI

```text
Generate an engaging social media caption for a photo of a sunset beach with people surfing. Add 3 relevant hashtags and 2 emojis.
