# Image Upload and Analysis Workflow

## Overview
This project provides a complete solution to upload an image through a web interface, analyze it using AI, and store the analysis results into Airtable. The workflow leverages **n8n**, **OpenAI's vision models**, and **Airtable integration** for seamless automation.

## Project Workflow

1. **Web Interface:**
    - A clean HTML page allows users to upload an image.
    - Upon clicking **Upload & Analyze**, the image is sent to the backend.

2. **Backend Workflow (n8n):**
    - **Webhook Node:** Listens for the incoming image file via POST request (`/image-analysis-upload`).
    - **Send to Compress Node:** Compresses the uploaded image using **TinyPNG API**.
    - **Received Compressed Node:** Retrieves the compressed image.
    - **OpenAI Analysis Node:**
      - Sends the compressed image to OpenAI's vision model (`gpt-4o-mini`).
      - Asks OpenAI to analyze and output a strict JSON with fields like:
        - `Image Name`
        - `Emotional Triggers`
        - `Colors`
        - `Facial Expressions`
        - `Text or Symbols`
        - `Composition Techniques`
        - `Trends/Style`
        - `Suggestions for Improvement`
    - **Code Node:**
      - Cleans and parses the JSON output from OpenAI.
    - **Airtable Node:**
      - Stores the parsed JSON into a designated Airtable base and table.
    - **Respond to Webhook Node:**
      - Returns the processed analysis back to the web interface.

3. **Result Display:**
    - The frontend dynamically displays the analysis results in a styled table once the response is received.

## Tech Stack
- **Frontend:** HTML, CSS (Bootstrap-Tailwind Hybrid)
- **Backend Workflow:** n8n (Low-code automation platform)
- **Image Compression:** TinyPNG API
- **AI Analysis:** OpenAI GPT-4o-mini Vision Model
- **Database:** Airtable

## Important Links
- Airtable Base: [View Airtable Base](https://airtable.com/app6LYn5SLnshv85m)

## Installation and Setup

### 1. n8n Setup
- Install and run **n8n** (locally or on cloud).
- Import the provided `finalWorkflow.json` into your n8n instance.
- Set up credentials:
  - Airtable API Key
  - TinyPNG API Key
  - OpenAI API Key

### 2. Frontend Setup
- Host the `test7.html` file on a local server (e.g., VSCode Live Server, XAMPP, or a cloud service).
- Ensure the form submission points to the correct n8n webhook URL.

### 3. Airtable Setup
- Create an Airtable Base with the correct fields as mentioned.
- Connect Airtable API with n8n.

## Example Output
An uploaded image returns a table showing:

| Field | Value |
| :--- | :--- |
| Emotional Triggers | Sadness, stress, contemplation |
| Colors | Muted tones, mainly gray and soft neutral colors |
| Facial Expression | Head in hands, body language suggesting distress |
| Text or Symbols | None |
| Composition Techniques | Subject off-center, focus on emotion and isolation |
| Trends/Styles | Contemporary, moody photography |
| Improvements | Add contrast or varied lighting for more depth |

## License
This project is licensed under the **MIT License**.

---

> Developed by **[Your Name]** ✨  
> Date: **April 28, 2025**
