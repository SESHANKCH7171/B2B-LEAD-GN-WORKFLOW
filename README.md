# B2B Lead Generation Workflow — AI Agent (n8n)

> An intelligent, fully automated B2B lead generation system built with **n8n**, powered by AI agents and real-time data APIs — specifically designed for the **Aerospace & Defense** industry.

---

## Workflow Architecture

![B2B Lead Gen Workflow — n8n Agent Overview](LEAD%20GEN%20WORKFLOW.png)

---

## What This Workflow Does

This n8n Agent Workflow automates the entire B2B lead generation pipeline:

1. **Searches** for target companies in Aerospace & Defense using Apollo.io API
2. **Enriches** company and contact data with real-time research via Perplexity AI & Tavily
3. **Qualifies** leads automatically using AI scoring logic (Score >= 70)
4. **Exports** structured lead data to Google Sheets / CRM
5. **Sends** personalized outreach email drafts using LLM (Claude / Gemini)

---

## Node Breakdown

| Node | Role |
|---|---|
| When clicking 'Execute workflow' | Manual trigger to start the pipeline |
| ICP Definition (Agent Input) | Defines Ideal Customer Profile parameters |
| B2B Lead Gen Agent | Core AI agent that orchestrates all tools |
| Gemini 3.0 Flash (Agent Brain) | LLM powering the agent's reasoning |
| Window_Buffer_Memory | Maintains context across agent steps |
| Tavily_Company_Search | Searches for matching companies in real-time |
| Apollo_Contact_Finder | Finds verified contact emails & titles |
| Tavily_Deep_Research | Deep-dives into company background & news |
| Quality Gate (Score >= 70?) | Filters out low-quality leads automatically |
| Google Sheets — Save Lead1 | Saves high-quality leads (true path) |
| Google Sheets — Save Lead | Saves qualified leads (false path) |
| Low Quality — Log & Skip | Logs and skips leads below threshold |

---

## Tech Stack

| Tool | Purpose |
|---|---|
| n8n (self-hosted) | Workflow automation engine |
| Apollo.io API | Company & contact search |
| Perplexity AI API | Real-time company research |
| Tavily API | Web search & enrichment |
| Google Gemini 3.0 Flash | AI reasoning & agent brain |
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
- `Tavily API Key`
- `Google Gemini API Key`
- `Google Sheets OAuth`

### Step 3 — Configure Inputs
In the **ICP Definition** node, update:
- Target **industry** (e.g., Aerospace & Defense)
- Target **company size** (e.g., 50–500 employees)
- Target **geography** (e.g., India, USA)

### Step 4 — Run the Workflow
- Click **Execute Workflow**
- Leads scoring >= 70 are saved to Google Sheets automatically
- Low quality leads are logged and skipped

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
