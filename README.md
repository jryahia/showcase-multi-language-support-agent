# Multi-Language Support Agent

**WhatsApp support agent that detects the customer's language and answers fluently in it, grounded only in the business's own knowledge base.**

> **This is a proprietary project. Source code is private. This page showcases the system's architecture and results.**

**Case study page:** [https://jryahia.github.io/showcase-multi-language-support-agent/](https://jryahia.github.io/showcase-multi-language-support-agent/)

![Multi-Language Support Agent](assets/00-dashboard.png)

## Problem it solves

Support teams cannot staff every language customers write in. This agent detects the language, answers from the business's FAQ, hours and policies, escalates what it should not handle, and shows which languages customers actually use.

## Architecture

![Architecture](assets/architecture.svg)

1. A signed WhatsApp message arrives via Twilio.
2. The language is detected with a confidence score; low confidence falls back to the primary language.
3. A reply is generated only from the knowledge base, in the detected language.
4. Sensitive cases escalate to a human via Telegram; language usage is recorded.

## Key features

- Language detection across 75+ languages
- Answers restricted to the configured knowledge base
- Confidence-based fallback
- Real Telegram escalation, logged
- Language coverage dashboard

## Tech stack

![Python](https://img.shields.io/badge/Python-161b22?style=for-the-badge&labelColor=161b22&color=161b22) ![FastAPI](https://img.shields.io/badge/FastAPI-161b22?style=for-the-badge&labelColor=161b22&color=161b22) ![lingua](https://img.shields.io/badge/lingua-161b22?style=for-the-badge&labelColor=161b22&color=161b22) ![Twilio](https://img.shields.io/badge/Twilio-161b22?style=for-the-badge&labelColor=161b22&color=161b22) ![OpenAI-compatible LLM](https://img.shields.io/badge/OpenAI--compatible%20LLM-161b22?style=for-the-badge&labelColor=161b22&color=161b22) ![Telegram Bot API](https://img.shields.io/badge/Telegram%20Bot%20API-161b22?style=for-the-badge&labelColor=161b22&color=161b22)

## What it does in practice

- Shows the business which languages its inbound volume actually arrives in.

## Screenshots

**Language coverage and live test box**

![Language coverage and live test box](assets/00-dashboard.png)

**API surface: agent, knowledge base, stats**

![API surface: agent, knowledge base, stats](assets/10-api.png)

---

Built by [Yahya Jarray](https://github.com/jryahia). Interested in a similar system? [Get in touch](mailto:yahiajarray43@gmail.com).
