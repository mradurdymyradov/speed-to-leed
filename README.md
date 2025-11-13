# Speed to Lead n8n Workflow

This repository contains an n8n workflow that automates the speed-to-lead process: capturing new leads from your website or ad forms, immediately contacting them via WhatsApp/SMS/email, and scheduling follow-ups to maximize conversions.

## Features

- **Immediate Response:** Triggers when a lead form is submitted and sends a personalised message via WhatsApp or SMS within seconds, ensuring the lead feels valued.
- **Multi-Channel Messaging:** Supports integration with Twilio, WhatsApp Business API or email (via nodemailer) so you can reach leads on their preferred channel.
- **Follow‑Up Scheduling:** Creates follow‑up reminders in your CRM or calendar to ensure no lead is forgotten. Includes configurable delay intervals and retry logic.
- **CRM Integration:** Updates or creates lead records in your CRM (e.g. HubSpot, Pipedrive) with conversation status, tags and next action.
- **Customizable Workflow:** Modular nodes let you adjust message templates, response times and follow‑up cadence without modifying code.

## Getting Started

1. **Prerequisites**
   - Running n8n instance (self‑hosted or n8n cloud).
   - API credentials for your messaging provider (e.g., Twilio SID/Auth Token or WhatsApp Business API).
   - API token for your CRM (if synchronising leads).

2. **Import the Workflow**
   - Download or copy `speed to leed.json`.
   - In n8n, click *Import* and select the JSON file.
   - Review the nodes and set up your credentials for messaging, CRM and any webhooks.

3. **Configure Webhook & Credentials**
   - Set the webhook URL in your lead form to the URL shown in the **Webhook** node.
   - Configure the **Send Message** node with your messaging credentials and customise the message template.
   - Configure the **CRM** nodes with your CRM API credentials.

4. **Customise & Activate**
   - Adjust the delays between initial contact and follow-ups using the **Wait** or **Set** nodes.
   - Customise conditions for leads with high/low priority.
   - Activate the workflow and test submission.

## Customising

- **Messaging Channel:** Replace Twilio/WhatsApp nodes with your preferred provider (e.g., Sendgrid for email).
- **Lead Scoring:** Add logic to score leads based on form fields and route them to different sequences.
- **Analytics:** Integrate with analytics tools to measure response time, conversion rate and adjust triggers.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
