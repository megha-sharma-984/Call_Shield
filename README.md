# Call Shield 🛡️

**Real-time protection from "digital arrest" and impersonation scam calls.**

Built for **Build With भारत 5.0** (CodeVerse) | Team: [Your Team Name]

---

## Problem

Scammers pose as police, CBI, or customs officers on calls and video calls. They create fear and urgency, tell victims "don't tell anyone," and push them to transfer money to a "safe account."

Existing tools mostly flag the caller's number, not what is being said. Scammers use fresh numbers, so victims get no warning during the call. Elderly and first-time digital users are the most vulnerable.

According to MHA / I4C data, reported "digital arrest" cases in India rose from 39,925 in 2022 to 1,23,672 in 2024, with losses growing from ₹91 crore to ₹1,918 crore (via ThePrint).

## Solution

Call Shield listens to a call in real time and scores scam risk from the conversation itself.

- Detects scam tactics: authority impersonation, urgency, isolation, and payment redirection
- Shows a full-screen warning in simple Hindi/English when risk rises
- Alerts a trusted family member at the same moment (WhatsApp/SMS)
- Auto-drafts a complaint summary for cybercrime.gov.in and the 1930 helpline
- Privacy-first: audio is processed in memory and never stored

## How It Works

Live call audio → Speech-to-text (Hindi/English) → Rule layer (instant keyword triggers) + LLM classifier (tactic detection) → Risk score (0-100) → Warning + trusted-contact alert → Complaint draft

## Tech Stack

|     Layer      |                   Technology               |
|----------------|--------------------------------------------|
| Frontend       | React                                      |
| Backend        | FastAPI + WebSockets                       |
| Speech-to-text | Whisper / cloud speech API                 |
| AI             | LLM classifier with structured JSON output |
| Alerts         | Twilio / WhatsApp API                      |

## Key Features

- Analyses what is said, not just who is calling
- Graded risk meter instead of a yes/no flag, to reduce false alarms
- Family alert during the call, not after the money is gone
- Built for Indian languages and first-time digital users

## Status

Prototype planned for the hackathon. Current scope:
- [ ] Live transcript
- [ ] Scam-tactic classifier and risk meter
- [ ] Warning screen
- [ ] Trusted-contact alert
- [ ] Complaint draft (stretch)

## Roadmap

- On-device Android app for real call protection
- More Indian languages
- Integration with the national cybercrime reporting portal

## Limitations

Android and iOS restrict access to call audio, so the demo uses speakerphone/microphone input. This is a warning tool, not proof of fraud.

## Team

Megha Sharma · Aaditya Sharma · Anjali Shishodia · Anisha Chauhan
IMS Engineering College,Ghaziabad

## References

- MHA / I4C data via ThePrint: "After 465% spike in 2024, MHA data shows digital arrest scams are on a decline in India"
- NewsBytes: "'Digital arrest' scam: Over ₹4,000cr lost in last 3 years" (Jul 2026)
- National Cyber Crime Reporting Portal: cybercrime.gov.in | Helpline: 1930
