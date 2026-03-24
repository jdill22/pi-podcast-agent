# PI — Podcast Inbox Manager

An AI-powered agent that monitors your podcast inbox, filters guest inquiries, and sends you a WhatsApp summary so you can accept or decline with one reply.

## The Problem
Managing podcast guest inquiries is time-consuming. Pitches come from multiple sources, most aren't a good fit, and responding to every email manually kills momentum.

## What PI Does
1. Monitors your Gmail inbox for guest inquiry emails
2. Filters out noise — newsletters, billing, automated senders
3. Uses Claude to generate a concise summary of each inquiry
4. Sends you a WhatsApp notification with the summary and sender details
5. (Coming soon) Accepts your YES/NO reply and responds to the guest automatically

## Tech Stack
- Python
- Gmail API — inbox monitoring
- Anthropic API (Claude Haiku) — inquiry summarization
- Twilio — WhatsApp notifications
- dotenv — environment variable management

## Setup
1. Clone the repo
2. Create a virtual environment: `python -m venv venv`
3. Activate it: `source venv/bin/activate`
4. Install dependencies: `pip install google-auth google-auth-oauthlib google-auth-httplib2 google-api-python-client anthropic twilio python-dotenv`
5. Add your credentials to a `.env` file:
```
ANTHROPIC_API_KEY=your_key
TWILIO_ACCOUNT_SID=your_sid
TWILIO_AUTH_TOKEN=your_token
TWILIO_WHATSAPP_FROM=whatsapp:+14155238886
MY_WHATSAPP_NUMBER=whatsapp:+1YOURNUMBER
```
6. Add your Google OAuth credentials as `PI-podcast-agent.json`
7. Run: `python podcast_agent_sketch.py`

## Roadmap
- HITL response loop — reply YES/NO via WhatsApp to accept or decline
- Podmatch integration when API becomes available
- Multi-agent architecture — separate agents for monitoring, summarizing, and responding
- Memory — track past guests and decisions over time

## Built By
Josh Dillingham · 2026
