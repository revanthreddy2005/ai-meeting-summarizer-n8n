# 🚀 AI Meeting Summarizer (n8n + Groq + Notion + Slack)

## 🔥 Overview

An AI-powered automation workflow that:

* 📄 Summarizes meeting transcripts using LLM (Groq)
* ✅ Extracts action items (task, owner, deadline)
* 🗂️ Stores structured data in Notion
* 💬 Sends real-time updates to Slack

---

## 🎥 Demo

👉 https://drive.google.com/drive/folders/1_Kv53yl3WFMBOSrd5sw3KA7PsOcd4cYN?usp=sharing

---

## ⚙️ Tech Stack

* **n8n** – Workflow automation
* **Groq API (LLM)** – AI processing
* **JavaScript (Code Node)** – Data transformation
* **Notion API** – Database storage
* **Slack API** – Notifications

---

## 🧠 Key Highlight

👉 Implemented a **JavaScript transformation layer** to convert unstructured AI outputs into structured JSON for seamless integration with Notion and Slack.

---

## 🏗️ Architecture

```
Webhook → Data Prep → Groq API → JS Processing → Notion → Slack
```

---

## 🔄 Workflow Explanation

1️⃣ Webhook (Input)

Receives meeting transcript via HTTP request and triggers the workflow.

2️⃣ Data Preparation

Cleans and extracts transcript for AI processing.

3️⃣ AI Processing (Groq)

Uses LLM to generate:

* Summary
* Action items

4️⃣ Data Transformation (JavaScript)

* Parses AI output
* Removes noise
* Converts into structured JSON

5️⃣ Notion Integration

Stores:

* Summary
* Action items

6️⃣ Slack Integration

Sends formatted message to team channel.

---

## 🧪 Example Input

```json
{
  "transcript": "John: Good morning everyone. So we need to launch the new landing page by next Friday. Sarah, can you handle the design? Sarah: Yes I will have mockups ready by Wednesday. John: Great. Mike, can you set up Google Analytics tracking by Thursday? Mike: Sure, I will handle that. John: Perfect. Next meeting is Monday at 10am.",
  "meeting_name": "Weekly sync - March 29"
}
```

---

## 🎯 Example Output

```json
{
  "summary": "The new landing page is due to launch next Friday, with Sarah handling the design and Mike setting up Google Analytics tracking.",
  "action_items": [
    {
      "task": "Design of the new landing page",
      "owner": "Sarah",
      "deadline": "Wednesday"
    },
    {
      "task": "Set up Google Analytics tracking",
      "owner": "Mike",
      "deadline": "Thursday"
    }
  ]
}
```

---

## 🚀 Features

* 🔥 Fully automated pipeline
* ⚡ Real-time processing
* 🧠 AI-powered insights
* 🔗 Multi-tool integration
* 🧹 Clean data transformation

---

## 📁 Project Files

* `workflow.json` – Exported n8n workflow

---

## 🏆 Learning Outcomes

* API integration with LLMs
* Prompt engineering
* Workflow automation
* Data transformation (JS)
* Building real-world AI systems

---
## ⚙️ Setup Instructions
1. Import `workflow.json` into n8n
2. Add credentials:
   - Groq API key → HTTP Request node
   - Notion Integration Token → Notion node
   - Slack Bot Token → Slack node
3. Update Notion Database ID in the Notion node
4. Activate workflow
5. POST to webhook URL to test
  

---

## 🔮 Future Improvements

* UI dashboard (React / Streamlit)
* Voice-to-text integration
* Multi-language support
* Task assignment automation

---

## 📬 Author

Bommala Revanth Reddy
Artificial Intelligence and Data Science student 
