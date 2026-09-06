# Low Stock Alert Automation (n8n)

An automated inventory monitoring system that scans a live Google Sheets inventory tracker daily and instantly notifies the team via Slack when any product falls below its reorder threshold — eliminating manual stock checks and preventing missed reorders.

## How It Works

- Runs automatically every morning on a scheduled trigger
- Reads real-time inventory data (Product, Quantity, Reorder Level) from Google Sheets
- Filters for any items that have dropped below their reorder point
- Aggregates all low-stock items into a single, clean alert
- Posts a formatted notification directly to a dedicated Slack channel

## Tech Stack

- **n8n** — workflow automation
- **Google Sheets API** — live inventory data source
- **Slack API (OAuth)** — instant team notifications

## Use Case

Ideal for e-commerce businesses, small retailers, or warehouse operations that want proactive inventory alerts without manually checking spreadsheets — reduces stockouts and lost sales from unnoticed low inventory.

## Workflow

`Schedule Trigger` → `Google Sheets (Read Inventory)` → `IF (Quantity < Reorder Level)` → `Aggregate` → `Slack (Post Alert)`

---

**Built by [Subtech Automation](https://github.com/subhanumer5935-hub)** — custom n8n automation solutions for e-commerce and small business operations.
