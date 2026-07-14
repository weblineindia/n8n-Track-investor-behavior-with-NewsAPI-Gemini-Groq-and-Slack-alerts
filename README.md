## Quick Overview

This workflow captures an investor’s buy/sell action via an n8n Form, pulls related market news from NewsAPI, uses Google Gemini to generate a one-line behavioral reflection, sends it via Gmail and Slack, stores it in an n8n Data Table, and posts a weekly Slack summary using Groq.

## How it works

1. Receives an investment action submission (buy/sell, reason, and market name) through an n8n Form.
2. Fetches recent related news from NewsAPI based on the selected market and aggregates article descriptions into a single summary.
3. Stores the form submission in an n8n Data Table and merges it with the aggregated news summary.
4. Uses Google Gemini (via an AI Agent) to generate a short, supportive behavioral insight and sends it through Gmail and to a Slack channel.
5. Parses the AI output and updates the corresponding Data Table row with the generated instant feedback.
6. Runs weekly on a schedule, pulls the last seven entries from the Data Table, and uses Groq to generate a concise behavioral pattern report that is posted to Slack.

## Requirements to Use This Workflow

- [**n8n account** (Self-hosted or Cloud)](https://n8n.partnerlinks.io/om1efg2qgvwi)
- **NewsAPI** account and API key for retrieving market news
- **Google Gemini API** credentials for generating behavioral insights
- **Groq API** credentials for creating weekly behavioral summaries
- **Gmail** account with OAuth2 credentials for email notifications
- **Slack** workspace with OAuth credentials for instant notifications
- An **n8n Data Table** configured to store investment actions and AI feedback

## Setup

1. Create or select an n8n Data Table for storing submissions and feedback, and ensure it includes an `instant_feedback` column (and `market_type` if you want it stored).
2. Add credentials for NewsAPI (HTTP Header auth), Google Gemini (PaLM API), Gmail OAuth2, Slack OAuth, and Groq.
3. Update the NewsAPI query (`q`) mapping if you want different keywords than the selected market name.
4. Set the target Slack channel and confirm the Gmail **Send To** address (currently `errorcommits@mailinator.com`) matches your needs.
5. Publish the form and share the form URL with users, and confirm the weekly schedule timing matches your desired reporting cadence.

## Need Help?

If you need assistance setting up this workflow, customizing it for your investment analysis process, or building advanced AI-powered automation, our team at **WeblineIndia** is here to help.

We can assist you with:

- Workflow setup and customization
- Google Gemini and Groq AI integrations
- NewsAPI, Gmail, and Slack integrations
- AI-powered behavioral analysis workflows
- n8n Data Table design and optimization
- Enterprise workflow automation
- Custom n8n workflow development

**Useful Resources:**

- **Contact Us:** https://www.weblineindia.com/contact-us.html
- **n8n Automation Services:** https://www.weblineindia.com/n8n-automation/
- **Process Automation Solutions:** https://www.weblineindia.com/process-automation-solutions.html
- **Hire n8n Developers:** https://www.weblineindia.com/hire-n8n-developers/

Our experts can help you build, customize, and scale intelligent automation workflows tailored to your business requirements.
