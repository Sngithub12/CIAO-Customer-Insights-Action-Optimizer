# CIAO-Customer-Insights-Action-Optimizer
# CIAO – Customer Insights & Action Optimizer

CIAO is a Lyzr-powered AI agent designed to transform unstructured customer feedback and journey data into structured, actionable UX insights. It identifies key pain points, sentiment, and drop-offs to help businesses improve user experience and reduce churn.

## 🧠 Agent Role
- Read feedback and journey data from Notion
- Extract sentiment, themes, pain points, and drop-off indicators
- Recommend UX improvements
- Output insights in structured JSON format

## 🛠 Tools Used
- **Notion** – Connected to Notion database (feedback, journey)
- *(Optional)* Slack/Google Sheets for future workflow extensions
- **LLM** – Uses `text-embedding-ada-002` for embedding + GPT-style reasoning

## 🖥 Prompt Logic
```text
Read customer feedback from Notion. For each row:
- Analyze feedback
- Extract sentiment, key themes, pain points, drop-off points
- Return structured JSON like:

{
  "THEMES": {
    "POSITIVE": ["..."],
    "NEGATIVE": ["..."]
  },
  "DROP_OFF_POINTS": ["..."],
  "RECOMMENDATIONS": ["..."]
}

