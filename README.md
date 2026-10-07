# Lead Qualification Automation | n8n

## Overview

An automated lead qualification workflow built with n8n that receives incoming
lead information, evaluates the lead based on budget, generates a personalized
response, and returns the qualification result automatically.

## Business Problem

Sales teams often spend time manually reviewing incoming leads, determining
whether they meet qualification criteria, and preparing follow-up responses.

## Solution

This workflow automates the initial lead qualification process by:

1. Receiving lead data through a webhook
2. Extracting and formatting lead information
3. Checking the lead's budget against a qualification threshold
4. Generating a personalized message
5. Returning the qualification result through a webhook response

## Workflow

Webhook
↓
Format Lead Data
↓
Lead Qualified?
├── Qualified → Qualified Message
└── Not Qualified → Follow-up Message
↓
Merge
↓
Respond to Webhook

## Tools & Technologies

- n8n
- Webhooks
- JSON
- REST API concepts
- Conditional logic
- Dynamic expressions
- PowerShell for API testing

## Qualification Logic

Leads with a budget of 50,000 or more are classified as qualified.

Example:

Budget >= 50,000 → Qualified
Budget < 50,000 → Follow-up

## Example

Input:

{
  "name": "Rahim Ahmed",
  "email": "rahim@techcorp.com",
  "company": "TechCorp",
  "budget": 75000,
  "product": "Laptop"
}

Output:

{
  "status": "success",
  "lead_status": "Qualified",
  "message": "Hello Rahim Ahmed, thank you for your interest in our Laptop. Your lead has been qualified and our sales team will contact you shortly."
}

## Key Skills Demonstrated

- Workflow automation
- Webhook integration
- Data transformation
- Conditional branching
- Dynamic data mapping
- Personalized message generation
- API testing
<img width="1904" height="214" alt="Execution_result" src="https://github.com/user-attachments/assets/ff7d97c8-d6f7-439e-9aea-a2c22d1d3ead" />
<img width="1674" height="767" alt="Workflow_overview" src="https://github.com/user-attachments/assets/73667e74-54f1-4f35-b0c4-0f53776cc426" />

