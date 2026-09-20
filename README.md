# 📰 AI News Curator Agent

An autonomous, lightweight, and 100% free AI agent for smart content curation. It fetches articles from your favorite RSS feeds, filters out clickbait and noise based on your personal interest profile using **Gemini 2.5 Flash**, and sends a beautifully formatted HTML briefing directly to your inbox every Monday morning.

Runs completely serverless in the cloud—no need to keep your PC on or pay for hosting!

---

## Tech Stack

- **Language:** Python 3.10
- **AI / LLM:** Google Gemini API (`google-genai`)
- **Automation / CI/CD:** GitHub Actions (Cron Jobs)
- **Email Delivery:** Resend API
- **Data Ingestion:** `feedparser`

---

## How It Works

1. **Scheduled Trigger (Cron):** Every Monday at 07:00 AM (BRT), GitHub Actions triggers the script execution.
2. **RSS Collection:** The agent scrapes configured RSS feeds for recent posts.
3. **Smart Curation:** Gemini evaluates article titles and summaries against your interest profile to discard irrelevant corporate noise and clickbaits.
4. **Email Dispatch:** A styled HTML report is generated and sent directly to your email inbox via Resend.

---

## Getting Started

1. Clone the repository:
   ```bash
   git clone [https://github.com/danielmcneto/ai-news-scout.git](https://github.com/danielmcneto/ai-news-scout.git)
   cd ai-news-scout

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
3. Create a .env file in the root directory:
   ```bash
   GEMINI_API_KEY=your_gemini_api_key
   RESEND_API_KEY=your_resend_api_key
   MY_EMAIL=your_email@example.com
4. Set up Repository Secrets in GitHub (Settings > Secrets and variables > Actions):
   - GEMINI_API_KEY
   - RESEND_API_KEY
   - MY_EMAIL
