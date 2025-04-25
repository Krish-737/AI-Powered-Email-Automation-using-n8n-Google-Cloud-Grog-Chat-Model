
# AI-Powered Email Automation using n8n, Google Cloud & Groq Chat Model

This project is a low-code workflow built in **n8n** that uses **Groq's Chat Model**, **Google Sheets**, and **Gmail** to automate intelligent email communication based on chat input.

---

## 🚀 Features

- 🤖 AI-powered chat processing using Groq's Chat Model
- 📬 Auto-send personalized emails via Gmail
- 🧠 Memory buffer for maintaining conversation context
- 📊 Logs interactions in Google Sheets
- ⚡ Seamless automation with n8n nodes and LangChain integration

---

## 🛠 Tech Stack

- **n8n** – Workflow automation platform
- **Groq Chat Model** – LLM for AI-driven responses
- **LangChain** – AI agent orchestration
- **Google Sheets** – Data storage and tracking
- **Gmail API** – Email sending functionality

---

## 📌 Workflow Overview

1. **Trigger**: Chat message received via `chatTrigger` node
2. **AI Agent**: Uses LangChain and Groq model to process and respond
3. **Memory**: Maintains session context using `memoryBufferWindow`
4. **Google Sheets**: Logs data into a specific sheet
5. **Gmail**: Sends AI-generated email with subject and body

---

## 📁 Google Sheets Setup

Make sure to set up a Google Sheet and connect it to your n8n instance.

**Example columns:**
```
| Name | Email | Subject | Message | Timestamp |
```

---

## 🔑 Prerequisites

- A working [n8n](https://n8n.io/) instance
- Groq API credentials
- Gmail OAuth credentials
- Google Sheets OAuth credentials
- LangChain-compatible nodes installed in n8n

---

## 🔄 Connections in the Workflow

| Node Name               | Type                            | Description                                 |
|------------------------|----------------------------------|---------------------------------------------|
| When chat message received | `chatTrigger` (LangChain)        | Triggers on chat message input              |
| AI Agent               | `agent` (LangChain)              | Processes prompt using LLM + tools          |
| Groq Chat Model        | `lmChatGroq` (LangChain)         | Provides AI response                        |
| Simple Memory          | `memoryBufferWindow` (LangChain) | Adds conversational memory                  |
| Google Sheets          | `googleSheetsTool`               | Logs interaction data                       |
| Gmail                  | `gmailTool`                      | Sends the composed email                    |

---

## 🧪 How to Run

1. Import the `.json` workflow into your n8n instance.
2. Set up and connect all required credentials:
   - Groq API
   - Google Sheets OAuth2
   - Gmail OAuth2
3. Modify the Google Sheet ID and Sheet Name as needed.
4. Trigger the workflow via a chat input.

---

## 👤 Author

**Krish**

---

## 📎 Useful Links

- [n8n Documentation](https://docs.n8n.io/)
- [LangChain Documentation](https://js.langchain.com/docs/)
- [Groq Chat Model](https://groq.com/)
- [Google Sheets API](https://developers.google.com/sheets/api)
- [Gmail API](https://developers.google.com/gmail/api)


