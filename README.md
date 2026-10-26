

## Overview

Project Nexus is an AI-powered workflow automation project built with **n8n, HubSpot, and Slack**. It automates lead qualification by analyzing incoming lead information, identifying purchase intent, and classifying leads as Hot, Warm, or Cold.

The workflow updates contact records in HubSpot and sends Slack notifications when a lead requires sales escalation. This helps sales teams prioritize promising leads, reduce manual work, and respond more efficiently.

## Key Features

- **Automated Lead Capture:** Receives lead information through a webhook.
- **AI-Powered Qualification:** Analyzes lead messages to evaluate purchase intent.
- **Lead Classification:** Categorizes leads into Hot, Warm, and Cold.
- **CRM Integration:** Creates or updates contact records in HubSpot.
- **Lead Score Updates:** Stores the qualification category in a custom HubSpot property.
- **Slack Notifications:** Alerts the sales team when escalation is required.
- **Conditional Routing:** Sends leads through different workflow paths based on qualification results.
- **Webhook Response:** Returns a response after processing the request.

## How It Works

1. A lead submits their details through a webhook.
2. HubSpot creates or updates the contact record.
3. An AI model analyzes the lead's message.
4. JavaScript processes the AI-generated qualification result.
5. A Switch node routes the lead to the Hot, Warm, or Cold path.
6. HubSpot is updated with the appropriate lead score.
7. The escalation condition is checked, and qualifying leads trigger a Slack notification.
8. The workflow returns a response to the webhook request.

## Technology Stack

| Technology | Purpose |
|---|---|
| n8n | Workflow automation |
| HubSpot | CRM and contact management |
| AI model | Lead qualification |
| Slack | Sales notifications |
| JavaScript | Processing AI output |
| Webhooks | Receiving lead data |
| GitHub | Source control and project backup |

## Lead Classification

- **Hot:** Strong purchase intent; prioritized for sales follow-up.
- **Warm:** Moderate interest; suitable for further engagement.
- **Cold:** Low immediate purchase intent; recorded for future reference.

## Example Input

```json
{
  "firstName": "Rahul",
  "lastName": "Kumar",
  "email": "rahul@example.com",
  "company": "ABC Technologies",
  "message": "I am interested in your product and would like to discuss pricing.",
  "source": "website"
}
```

## Setup Instructions

1. Import the workflow JSON file into n8n.
2. Configure your own HubSpot and Slack credentials.
3. Configure the AI provider credential used by the workflow.
4. Ensure the HubSpot custom contact property `Lead Score` supports `hot`, `warm`, and `cold`.
5. Configure and test the webhook with sample lead data.
6. Verify lead classification, CRM updates, Slack notifications, and webhook responses.
7. Publish the workflow when testing is complete.

## Testing

The workflow has been tested with Hot, Warm, and Cold lead scenarios, including escalation routing.

Before using it in a live business environment, verify the production webhook, credential configuration, error handling, and all integrations.

## Security

- Never commit API keys, passwords, access tokens, or other secrets to GitHub.
- Use your own credentials when importing the workflow.
- Handle lead information responsibly and follow applicable privacy requirements.

## Future Improvements

- Add error handling and retry mechanisms.
- Implement execution logging and monitoring.
- Improve lead scoring and qualification rules.
- Integrate additional lead sources and CRM platforms.
- Add analytics and lead conversion reporting.

## Project Status

**Prototype completed and published in n8n Cloud.**

Project Nexus demonstrates AI-assisted decision-making, business process automation, CRM integration, conditional routing, and sales notification workflows.
