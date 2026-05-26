# n8n Voice AI Receptionist

A collection of n8n workflows that deploy AI voice receptionists for service businesses using VAPI and ElevenLabs. Handles inbound calls, transcribes and logs conversations, updates CRM records, and sends WhatsApp follow-ups.

## Workflows

### VAPI AI Receptionist - Accounting Firm
Receives inbound call webhooks from VAPI, processes the transcript, creates or updates contacts in GoHighLevel (GHL), uploads call recordings to Google Drive, and sends a WhatsApp follow-up summary to the prospect.

**Stack:** VAPI Webhook, GoHighLevel CRM, Google Drive, WhatsApp API

### VAPI AI Receptionist - HVAC
Same architecture as the accounting version, adapted for HVAC service businesses. Captures caller details, logs to GHL, stores the recording, and sends a WhatsApp confirmation.

**Stack:** VAPI Webhook, GoHighLevel CRM, Google Drive, WhatsApp API

### ElevenLabs Voice Agent - Real Estate
Processes ElevenLabs voice agent call completions. Logs conversation data to Google Sheets, uploads call audio to Google Drive, and sends a WhatsApp follow-up to the lead.

**Stack:** ElevenLabs Webhook, Google Sheets, Google Drive, WhatsApp API

### ElevenLabs + Twilio SMS
Same ElevenLabs voice agent flow with Twilio SMS added as a follow-up channel alongside WhatsApp.

**Stack:** ElevenLabs Webhook, Twilio SMS, Google Sheets, Google Drive, WhatsApp API

## Tech Stack

- [n8n](https://n8n.io) - workflow automation
- VAPI - AI voice calling platform
- ElevenLabs - voice AI
- GoHighLevel (GHL) - CRM
- Twilio - SMS
- WhatsApp Business API
- Google Drive + Sheets - storage and logging

## Usage

1. Import the `.json` file into your n8n instance via **Workflows > Import from file**
2. Configure credentials: VAPI/ElevenLabs webhook secrets, GHL API key, Twilio SID + Auth Token, WhatsApp API
3. Set your webhook URL in VAPI or ElevenLabs to point to n8n
4. Activate the workflow

## Note

Credential values have been replaced with placeholders (e.g. `YOUR_API_TOKEN`). Add your own credentials via n8n's credential manager before activating.

## About

Built by [Rajiv Unnikrishnan](https://www.rajivunnikrishnan.com) - n8n automation specialist.
