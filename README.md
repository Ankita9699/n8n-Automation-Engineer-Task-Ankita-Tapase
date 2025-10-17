# 🚀 n8n Automation Engineer – Analytos Task

## 📘 Overview
This project automates a **Lead Qualification Workflow** using **n8n**, demonstrating integration of multiple APIs, workflow branching, modular design (subflows), and real-world automation logic.

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
