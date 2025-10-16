# n8n Lead Qualification Automation

## Overview
This n8n workflow automates the entire lead qualification process from incoming emails. It extracts lead details, uses AI to categorize intent, logs leads into a Google Sheet CRM, sends automated follow-up emails, and notifies the sales team via Discord.

## Workflow Description
- **Gmail Trigger**: Watches for new lead emails.
- **Edit Fields**: Extracts fields like name, email, company, and message.
- **Message a Model**: Sends lead message to an AI model to classify lead intent (High, Medium, Low) with a confidence score.
- **If Node**: Routes based on intent categorization.
- **Google Sheets Append Row**: Logs every lead and category for tracking.
- **Send Message (Gmail)**: Sends automatic demo scheduling email for medium/low intent.
- **Send Message (Discord)**: Posts a notification to the sales channel with lead summary.

## Setup Instructions
1. Import this workflow JSON into your n8n environment.
2. Set up the Gmail and Google Sheets credentials with proper access scopes.
3. Configure the Discord bot token and specify your server & channel for notifications.
4. Modify the “Message a model” node with your OpenAI API key.
5. Test by sending a sample email or using the Manual Trigger node.

## Notes
- Demo values can be inserted for testing by editing the “Edit Fields” node.
- The workflow includes basic error handling and modular design for easy customization.
- Webhook support allows manual triggering for integration and testing.

---
