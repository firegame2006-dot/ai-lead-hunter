AI Lead Hunter

An automated n8n workflow that finds potential clients for a web design studio.

Every day the system searches for local businesses in Ukraine through the Google Places API, identifies companies without a proper website, checks for duplicates, sends the candidates to AI qualification, and delivers the selected leads to Telegram.

Main Stages

- Search Generation — builds combinations of cities, categories and search modifiers. Queries rotate from day to day so the whole list is covered gradually.
- Google Places — fetches the business name, address, phone, rating, reviews, website and other details.
- Filtering — drops closed businesses, duplicates and companies that already have a proper website.
- Memory — a Data Table stores every business found so far, so the same business never shows up in a report twice.
- AI Qualification — OpenAI assesses each lead's potential, decides whether it needs a website, and produces a "lead_score", a reason and a recommended website type.
- Fallback — if the AI is unavailable or returns an invalid response, a backup scoring algorithm is used.
- Telegram — a structured report with the new leads is built and sent to Telegram.

Technologies

- n8n
- JavaScript
- Google Places API
- OpenAI API
- n8n Data Tables
- Telegram Bot API

Project Goal

Automate finding and pre-qualifying potential clients instead of collecting leads by hand.
