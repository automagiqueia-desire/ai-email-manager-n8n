# 🤖 AI Email Agent — Smart Customer Support Automation for E-Commerce

[![n8n](https://img.shields.io/badge/n8n-Automation-FF6D5A?style=for-the-badge&logo=n8n)](https://n8n.io)
[![LLM](https://img.shields.io/badge/LLM-Llama_3.3_%7C_Mistral-blue?style=for-the-badge)](https://openrouter.ai)

> **AI-powered Gmail automation agent built on n8n for e-commerce businesses. Classifies incoming emails, generates personalized draft replies, and alerts your team — 24/7, without manual input.**

---

## 📺 Workflow Overview

![Workflow Diagram](workflow-image.png)
*Full architecture: from Gmail trigger to Telegram alert — every step automated.*

---

## 🎯 The Problem It Solves

E-commerce support teams spend hours every day doing the same three things: reading emails, deciding what they are, and writing a first reply. This system eliminates all three.

| Before | After |
|--------|-------|
| Manual triage of every inbox email | Automatic semantic classification |
| Writing responses from scratch | AI-generated drafts ready for human validation |
| Missing urgent messages | Instant Telegram alert for high-priority emails |
| 2+ hours/day on email | Staff focuses on decisions, not sorting |

---

## ⚙️ How It Works

1. **Trigger** — Gmail listener detects new incoming email
2. **Classification** — Llama 3.3 70B categorizes the email: Order, Complaint, Prospecting, Advertising, or Website
3. **Auto-labeling** — Gmail label applied automatically based on category
4. **Draft generation** — Mistral 7B writes a personalized reply draft, ready for human review
5. **Priority alert** — High-priority emails (complaints, urgent orders) trigger an instant Telegram notification
6. **Zero manual input** — runs continuously, 24/7

---

## 🛠️ Tech Stack

| Layer | Tool |
|-------|------|
| Orchestration | [n8n](https://n8n.io) |
| Email | Gmail API |
| Classification LLM | Llama 3.3 70B (via OpenRouter) |
| Reply Generation LLM | Mistral 7B (via OpenRouter) |
| Alerts | Telegram Bot API |
| AI Framework | LangChain |

**Why two LLMs?** Llama 3.3 gives higher precision on classification tasks. Mistral generates more natural, conversational reply drafts. Using the right model for the right task improves both accuracy and output quality.

---

## 🚀 Setup

1. Download `WORKFLOW.json` from this repo
2. Import it into your n8n instance (File → Import workflow)
3. Configure your credentials:
   - Gmail OAuth2
   - OpenRouter API key
   - Telegram Bot token + Chat ID
4. Activate the workflow

> Requires an active n8n instance (cloud or self-hosted). Free tier works for most small/medium volumes.

---

## 📁 Repository Structure

```
├── WORKFLOW.json        # Full n8n workflow — import directly
├── workflow-image.png  # Architecture diagram
└── README.md
```

---

## 🔧 Customization

- **Add categories** — edit the classification prompt in the Llama node to match your business (returns, wholesale, partnerships, etc.)
- **Change notification channel** — swap Telegram for Slack or email in under 5 minutes
- **Connect to CRM** — add a HubSpot or Airtable node after classification to log every email automatically
- **Multi-language support** — the LLM nodes handle multilingual input natively

---

## 👤 About

Built by **Désiré** — AI Automation Engineer specializing in n8n workflows, AI agents, and API integrations for e-commerce operations.

- 🔗 LinkedIn: [linkedin.com/in/désiré-nkurunziza-9375ba356](https://www.linkedin.com/in/désiré-nkurunziza-9375ba356)
- 💼 Upwork: [upwork.com/freelancers/desire-nkurunziza](https://www.upwork.com)
- 📧 automagiqueia@gmail.com
