# 🚀 n8n Automation Engineer – Analytos Task

## 📘 Overview
This project automates a **Lead Qualification Workflow** using **n8n**, demonstrating integration of multiple APIs, workflow branching, modular design (subflows), and real-world automation logic.

---

## ⚙️ Workflow Summary

### 🔹 Trigger
- **Gmail Trigger** — When a new email arrives (filtered by label or sender)

### 🔹 Step 1: Extract Lead Details
- Parses email content to extract:
  - Name  
  - Email  
  - Company  
  - Message

### 🔹 Step 2: Lead Categorization (OpenAI / LLM)
- Sends the extracted message to **OpenAI API** (or any LLM)
- Receives:
  - Category → High / Medium / Low Intent  
  - Confidence Score (0–100)
- Built as a **Reusable Subflow**

### 🔹 Step 3: Branching Logic
- **High Intent → CRM Entry** (Google Sheet or HubSpot)
- **Medium/Low Intent → Automated Email Reply**

### 🔹 Step 4: Log All Leads
- Appends all lead data into Google Sheets / Airtable for tracking:
  ```
  Timestamp | Name | Email | Company | Message | Category | Confidence | Status
  ```

### 🔹 Step 5: Notify Sales Team
- Sends a **Slack / Discord** notification with:
  ```
  🚀 New Lead Alert
  Name: {{Name}}
  Intent: {{Category}}
  Confidence: {{Confidence}}%
  ```

### 🔹 Step 6: Error Handling & Retry
- Error Trigger node to log or notify errors in Slack
- Retry logic enabled for failed API calls

---

## 🧩 Subflow: Lead Categorization
This subflow accepts the **lead message text** as input and returns:
```json
{
  "category": "High Intent",
  "confidence": 93
}
```
It can be reused in other automation workflows for consistency and modularity.

---

## 🧠 Tech Stack
| Tool | Purpose |
|------|----------|
| **n8n** | Workflow automation |
| **Gmail API** | Email trigger & auto-reply |
| **OpenAI API** | Lead intent analysis |
| **Google Sheets / HubSpot** | CRM data storage |
| **Slack / Discord Webhook** | Lead notifications |
| **Webhook Trigger** | Manual testing and flexibility |

---

## 🧪 Testing the Workflow
1. Import the provided `.json` workflow(s) into n8n.
2. Add credentials for:
   - Gmail  
   - OpenAI (or custom LLM endpoint)  
   - Google Sheets / HubSpot  
   - Slack / Discord Webhook
3. Send a sample lead email to your Gmail.
4. Observe:
   - Auto lead categorization  
   - CRM entry creation  
   - Slack/Discord notification  
   - Automated reply (if Medium/Low intent)

---

## 📦 Deliverables
- `main_workflow.json`  
- `lead_categorization_subflow.json`  
- `README.md` (this file)  
- Demo Video (2–5 min, showing workflow setup and execution)

---

## 🎥 Demo Video
📹 [Watch the Demo](#) *(Add your Google Drive or YouTube link here)*

---

## 📧 Submission
**Email To:** santosh.thota@analytos.ai  
**CC:** ravi.soni@analytos.ai  
**Subject:** `n8n Automation Engineer Task – Ankuri`

Include:
- GitHub/Drive link to workflows & README  
- Demo video link  
- Updated resume

---

## 👩‍💻 Author
**Ankuri**  
Automation Engineer | QA Tester | API & AI Workflow Builder  
🌐 [GitHub](https://github.com/) | 💼 [LinkedIn](#) | ✉️ ankuri@example.com

---

## ⭐ Notes
- The workflow design follows n8n best practices:
  - Reusable subflows  
  - Structured branching  
  - Error handling  
  - API modularization  
- Built for scalability and real-world automation use cases.
