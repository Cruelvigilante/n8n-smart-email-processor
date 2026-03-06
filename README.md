# n8n Smart Email Processor

An AI-powered email automation workflow built with n8n and Google Gemini that automatically classifies, processes, and organizes incoming Gmail messages.

This workflow turns your inbox into an intelligent system that can:
- Automatically categorize emails
- Generate summaries
- Draft replies
- Detect security alerts
- Extract receipts
- Send push notifications
- Log important information to Google Sheets

---

# Features

# Email Classification
Incoming emails are automatically categorized into:
- Promotions
- Social
- Personal
- Job Listings
- Security / Password Requests
- Receipts
- Miscellaneous

---

# Automatic Email Drafting
Personal emails can automatically generate reply drafts using gemini-Flash-2.5.

---

# Receipt Extraction
Receipts are parsed and logged to Google Sheets with:
- The Purchase Date
- The Company / Merchant
- And The Charge Amount

---

# Security Monitoring
Security related emails are analyzed and classified into:
- Security Alerts
- OTP (One Time Passwords)
- Account Updates

Important events trigger a Pushover notification to my phone.

---

# Job Alerts
Job listing emails trigger instant push notifications so that I know to apply to them when i get a second.

---

# Email Analytics
Social or misc emails can be summarized and stored in Google Sheets for tracking.

---

# Workflow Architecture
Gmail Trigger --> Email Parsing + Cleaning --> AI Text Classifier (Gemini) --> Routing by category --> Category-specific processing --> Merge → Processed-AI label

---

# Technologies Used

- **n8n** – workflow automation
- **Google Gemini** – AI classification and analysis
- **Gmail API** – email access
- **Google Sheets API** – data logging
- **Pushover API** – push notifications to my phone

---

# Setup

# 1. Requirements

You will need:
- n8n instance
- Gmail account
- Google Sheets account
- Google Gemini API access
- Pushover account (optional for notifications)

---

# 2. Import the Workflow

1. Open **n8n**
2. Import the workflow JSON
3. Connect your credentials:
   - Gmail
   - Google Sheets
   - Gemini API
   - Pushover API

---

# 3. Configure Gmail Trigger

Recommended filter:
is:unread -label:processed-ai


This prevents the workflow from processing the same email multiple times.

---

# 4. Activate Workflow

Once configured, activate the workflow in n8n.
The system will now automatically process incoming emails every minute.

---

# Example Use Cases

- Automatically track expenses from email receipts
- Detect suspicious login alerts
- Receive push notifications for job listings
- Draft email replies automatically
- Organize inbox without manual filtering

---

# Future Improvements

Possible enhancements:

- Calendar event detection
- AI task extraction from emails
- Smart newsletter summarization
- Expense categorization

---

# License

MIT License

---

# Author

Created by **Cayden Marty**
