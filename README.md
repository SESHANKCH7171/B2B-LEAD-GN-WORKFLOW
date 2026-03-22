# B2B Lead Generation Workflow — AI Agent (n8n)

> An intelligent, fully automated B2B lead generation system built with **n8n**, powered by AI agents and real-time data APIs — specifically designed for the **Aerospace & Defense** industry.

---

## What This Workflow Does

This n8n Agent Workflow automates the entire B2B lead generation pipeline:

1. **Searches** for target companies in Aerospace & Defense using Apollo.io API
2. **Enriches** company and contact data with real-time research via Perplexity AI & Tavily
3. **Qualifies** leads automatically using AI scoring logic
4. **Exports** structured lead data to Google Sheets / CRM
5. **Sends** personalized outreach email drafts using LLM (Claude / Gemini)

---

## Tech Stack

| Tool | Purpose |
|---|---|
| n8n (self-hosted) | Workflow automation engine |
| Apollo.io API | Company & contact search |
| Perplexity AI API | Real-time company research |
| Tavily API | Web search & enrichment |
| Google Gemini / Claude | AI reasoning & email drafting |
| Google Sheets | Lead output & tracking |

---

## How to Use

### Step 1 — Import the Workflow
- Download the `.json` file from this repo
- Open your **n8n** instance
- Go to **Workflows** → **Import from File**
- Select the downloaded `.json` file

### Step 2 — Set Up Credentials
Add the following API credentials in n8n:
- `Apollo.io API Key`
- `Perplexity API Key`
- `Tavily API Key`
- `Google Gemini or Claude API Key`
- `Google Sheets OAuth`

### Step 3 — Configure Inputs
In the workflow, update the input node with:
- Target **industry** (e.g., Aerospace & Defense)
- Target **company size** (e.g., 50–500 employees)
- Target **geography** (e.g., India, USA)

### Step 4 — Run the Workflow
- Click **Execute Workflow**
- Leads will be automatically populated in your connected Google Sheet

---

## Workflow Architecture

```
Trigger --> Apollo Search --> Company Enrichment (Perplexity/Tavily)
 --> AI Lead Scoring --> Google Sheets Export
 --> Email Draft Generation
```

---

## Use Case

Built for **freelancers, agencies, and sales teams** targeting niche B2B markets like:
- Aerospace & Defense manufacturers
- MRO (Maintenance, Repair & Overhaul) companies
- Defense technology suppliers
- Aviation services companies

---

## Author

**Seshank CH** — B2B Lead Generation Specialist | AI Automation Builder
Aerospace & Defense Industry | IIT Madras PG Alumni

GitHub: [@SESHANKCH7171](https://github.com/SESHANKCH7171)

---

## License

MIT License — Free to use, modify, and distribute.
