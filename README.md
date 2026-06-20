<div align="center">

# Bilingual Banking Chatbot

Bilingual banking chatbot powered by GPT-4o, Azure AI Search, speech services, WhatsApp, and ACS.

![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?logo=python&logoColor=white)
![Status](https://img.shields.io/badge/Status-Reference%20Implementation-6366F1)

</div>

---

## Overview

Bilingual banking chatbot powered by GPT-4o, Azure AI Search, speech services, WhatsApp, and ACS.

## 📖 The Story

Language can become a barrier in digital banking, especially when the customer is more comfortable speaking than typing. This project tells the story of expanding a conventional assistant into one that can serve both English and Urdu conversations across text and voice.

The request enters through FastAPI, audio is transcribed, relevant banking information is retrieved through Azure AI Search, and GPT-4o prepares a grounded response. The answer can then return as text or synthesized speech and can be connected to WhatsApp or Azure Communication Services.

The repository demonstrates the architecture needed for inclusive conversational banking. Its next phase would add language-specific evaluation sets, human handoff, accessibility testing, and stricter controls around regulated financial content.

## Highlights

- Text conversation endpoint
- Speech-to-text and text-to-speech
- Conversational AI responses
- WhatsApp and ACS integration

## Tech Stack

Python Â· FastAPI Â· Azure OpenAI Â· LangChain Â· FAISS

## Getting Started

```bash
git clone https://github.com/haseebconventarian2-gif/bilingual-Chatbot.git
cd bilingual-Chatbot
python -m venv .venv
# Windows: .venv\Scripts\activate
# macOS/Linux: source .venv/bin/activate
pip install -r requirements.txt
```

## Configuration

Configure Azure OpenAI deployments and any messaging-channel credentials in `.env`.

> Store credentials in `.env` and never commit secrets.

## Run

```bash
uvicorn main:app --host 0.0.0.0 --port 8000
```

## Project Status

This is a learning and reference implementation. Review security, validation, monitoring, and deployment settings before production use.

## Detailed Code Reference

**Runtime flow:** `Text/audio -> STT -> retrieval -> LLM -> TTS/text -> channel reply`

### Repository map

- `.github/` - supporting package or resources
- `__pycache__/` - supporting package or resources
- `api/` - supporting package or resources
- `faiss_index/` - supporting package or resources
- `fastapi_app.py` - project file
- `IMPLEMENTATION_SUMMARY.md` - project file
- `main.py` - project file
- `QUICKSTART.md` - project file
- `rag_pipeline.py` - project file
- `README.md` - project file
- `requirements.txt` - project file
- `START_HERE.md` - project file
- `VERIFICATION_CHECKLIST.md` - project file

### Validation checklist

1. Install dependencies in a clean virtual environment.
2. Configure only the environment variables needed by enabled integrations.
3. Start the documented entry point and test its health or root route.
4. Exercise successful and invalid requests.
5. Confirm secrets, private datasets, indexes, and model artifacts are ignored.

### Production checklist

- Use managed secret storage.
- Add authentication, authorization, rate limiting, and request-size limits.
- Add automated tests, structured logs, monitoring, and health checks.
- Pin and audit dependencies.
- Define retention and privacy controls for audio and customer data.

> This README reflects the current codebase. External AI, telephony, and messaging features require their respective accounts, assets, and approvals.


