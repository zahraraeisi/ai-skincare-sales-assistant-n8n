````markdown
# AI Skincare Sales Assistant with n8n

This project is a demo AI-powered sales and customer support assistant for skincare and beauty stores.

It is built with **n8n**, **Bale Messenger**, and **OpenAI** to demonstrate how an online store can automate part of the customer consultation and pre-sales process.

> This repository is a Demo / Proof of Concept and is not based on a real client project.

## What This Workflow Does

The assistant can:

- Guide users through a multi-step skincare consultation
- Recommend products based on skin type and concerns
- Answer questions about specific products
- Handle common customer support questions
- Collect customer information
- Create test orders
- Track test orders
- Maintain user session state
- Generate AI-assisted product responses

## Example Use Cases

A customer can ask questions such as:

- Which sunscreen is suitable for oily skin?
- What should I use for acne-prone skin?
- Which moisturizer is suitable for dry skin?
- How should I use this product?
- Is this product suitable for sensitive skin?

The workflow first uses structured product data and then uses AI to generate a natural response while following predefined rules.

## Workflow Architecture

Main components:

1. Bale Messenger Trigger
2. Input normalization
3. Session retrieval
4. Business logic and product matching
5. AI decision routing
6. OpenAI response generation
7. Session persistence
8. Bale Messenger response

## Main Features

### Product Recommendation

The workflow contains sample skincare products with:

- Product name
- Category
- Price
- Stock status
- Suitable skin types
- Skin concerns
- Benefits
- Usage instructions
- Limitations
- Product URL

### Smart Product Search

User messages are normalized and matched against product information using simple keyword scoring and synonym expansion.

### AI-Assisted Responses

AI is only used when necessary.

The AI receives structured product information and is instructed not to invent:

- Products
- Prices
- Stock information
- Product URLs
- Medical claims

### Guided Consultation

Users can receive recommendations based on:

- Skin type
- Acne
- Dryness
- Oiliness
- Spots and pigmentation
- Sensitive skin
- Fine lines

### Order Demo

The workflow includes a simple test-order flow:

Product → Name → Phone → Address → Confirmation

This functionality is included only to demonstrate how a sales workflow could be structured.

## Tech Stack

- n8n
- Bale Messenger
- OpenAI
- JavaScript
- n8n Data Tables
- HTTP APIs

## Setup

After importing the workflow into n8n:

1. Configure your Bale Messenger credentials.
2. Configure your OpenAI credentials.
3. Create an n8n Data Table for session storage.
4. Replace `YOUR_DATA_TABLE_ID` with your Data Table ID.
5. Add the `BALE_BOT_TOKEN` environment variable.
6. Replace `YOUR_CONTACT_INFO` with your preferred contact information.
7. Activate the workflow.

## Required Environment Variable

```env
BALE_BOT_TOKEN=YOUR_BALE_BOT_TOKEN
````

## Security

The public version of this workflow does not contain real API keys, bot tokens, credential IDs, private Data Table IDs, or personal contact information.

Never commit real credentials to a public repository.

## Platform Adaptation

This demo was originally built for **Bale Messenger** for the Persian market.

The same workflow architecture can be adapted for other messaging channels such as:

* Telegram
* Website chat
* WhatsApp integrations
* Other messaging APIs

The business logic, product recommendation system, and AI layer can remain largely the same while the messaging integration is replaced.

## Disclaimer

This project is intended as a demonstration of AI-assisted ecommerce automation.

It does not provide medical diagnosis or professional skincare advice.

For serious or persistent skin conditions, users should consult a qualified medical professional.

## Author

Zahra Raeisi

AI Automation Specialist

n8n • WordPress • WooCommerce • AI Agents • API Integrations

```
