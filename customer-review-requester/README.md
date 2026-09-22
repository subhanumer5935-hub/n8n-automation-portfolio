# Customer Review & Feedback Requester

**Subtech Automation | n8n E-commerce Automation Portfolio**

An automated workflow that identifies delivered orders and sends personalized review-request emails to customers — with built-in duplicate prevention so no customer is ever emailed twice.

## Use Case

E-commerce stores lose valuable reviews simply because follow-up is manual and easy to forget. This workflow closes that gap automatically, running on a daily schedule with zero manual effort after setup.

## How It Works

1. **Schedule Trigger** — runs daily
2. **Google Sheets (Get Rows)** — pulls current order data
3. **Filter** — isolates orders that are `delivered` AND not yet sent a review request
4. **Gmail (Send Message)** — sends a personalized HTML review-request email per matching order
5. **Google Sheets (Update Row)** — flags the order as `Review Requested: Yes` to prevent duplicate sends

## Tech Stack

- **n8n** (self-hosted via Docker)
- **Google Sheets API** — order data + state tracking
- **Gmail API** — automated email delivery
- No external API costs — built entirely on the free-tier Google Workspace stack

## Key Engineering Detail

Idempotency is handled via a `Review Requested` status column, updated only after successful email delivery — ensuring the workflow is safe to run on a recurring schedule without ever double-emailing a customer.

---
Built and maintained by **Subtech Automation**.
