# GENBA Voice

GENBA Voice is a bilingual Japanese–English AI assistant that turns small frontline workplace concerns into a constructive first step for improvement.

## Live demo

- [Try GENBA Voice](https://script.google.com/macros/s/AKfycbz7fSkPUYs1qeCBRXLQM5X2pkOllmKIQAPsdDwm_Dp5MzTINjTVzwEDJ3el9COF8sUx/exec)
- [Watch the 44-second demo](https://youtu.be/HWja3w6Igzc)

## What it does

Users select a workplace context and urgency level, then describe a small concern or friction. GENBA Voice returns structured guidance covering:

- what may be happening
- a possible system pattern
- a small step to try
- a calm message that can be shared
- points that still need confirmation

The purpose is not to replace managers, specialists, or human judgment. It helps users begin a constructive conversation without immediately blaming an individual.

## Key features

- Japanese and English interface
- Bilingual dropdown options and AI responses
- Structured, non-judgmental guidance
- Copyable calm message
- Mobile-friendly web interface
- No intentional storage of user input
- API key stored in Google Apps Script Properties, never in browser code

## Built with

- Google Apps Script
- HTML5
- CSS3
- JavaScript
- OpenAI API
- GPT-5.6

## How Codex and GPT-5.6 were used

### Codex

Codex supported the development and debugging workflow. It helped review the Google Apps Script and HTML structure, diagnose a language-switching bug, and produce a reliable replacement for the frontend.

A specific bug caused the main interface to switch to English while the two dropdown menus remained in Japanese. Codex helped trace this to the dropdown update function not being called correctly. The language-switching flow was simplified, the existing web app was redeployed as a new version while preserving its public URL, and both dropdowns were verified in Japanese and English.

Codex also assisted with test cases, deployment guidance, documentation, and preparation of the Build Week submission.

### GPT-5.6

GPT-5.6 powers the application’s structured analysis. The selected context, urgency, language, and concern are sent from the browser to a server-side Google Apps Script function. The server calls the OpenAI API and returns five clearly separated sections designed to support a calm and constructive workplace conversation.

The prompt and output structure emphasize system patterns, small testable steps, uncertainty, and non-blaming language.

## Privacy and safety

Do not enter names, company names, client information, or confidential information.

The application does not intentionally store user input. The OpenAI API key is stored in Google Apps Script Properties and is not included in this repository or exposed in the browser.

AI suggestions are a starting point, not a final decision. Safety, legal, medical, harassment, or emergency concerns should be escalated through appropriate human channels.

## Repository files

- `index.html` — bilingual user interface and client-side logic
- `Code.gs` — server-side Google Apps Script and OpenAI API call

## OpenAI Build Week

Built as an individual submission for OpenAI Build Week in the Work & Productivity category.
