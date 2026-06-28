# feature-request-pipeline
# AI Feature Request Prioritizer

An enterprise-grade n8n workflow that centralizes customer feedback from multiple channels, classifies feature requests using Google Gemini, prioritizes them by urgency, and logs structured insights into Google Sheets with automated error handling.

## 🚀 Architectural Overview

This solution consists of three coordinated workflows:

1. **Feedback Ingestion**: Collects customer feedback from Gmail, Typeform, and Webhooks into a centralized database.
2. **AI Classification**: Uses **Google Gemini 2.5 Flash Lite** via LangChain to detect feature requests, normalize feature names, and assign urgency levels.
3. **Processing & Logging**: Stores prioritized requests in Google Sheets, updates processing status, retries failed items, and sends email notifications for successful batches and workflow failures.

## ✨ Features

* Multi-source feedback ingestion
* AI-powered feature request detection
* Feature name normalization
* Urgency classification
* Automated Google Sheets logging
* Scheduled batch processing
* Processing status tracking
* Built-in error notification workflow

## 🛠 Prerequisites

* **n8n** (Cloud or Self-hosted)
* **Google Gemini API Key**
* **Google Sheets OAuth Credentials**
* **Gmail OAuth Credentials**
* **Typeform API Credentials** (optional)
* **Webhook Endpoint** (optional)

## 📥 Installation

1. Import all workflow JSON files into n8n.
2. Configure your Google Gemini, Google Sheets, Gmail, and Typeform credentials.
3. Create the required Google Sheets with the expected columns.
4. Update email recipients and webhook endpoints where applicable.
5. Activate the three workflows.

## 📂 Repository Structure

```text
Feature Requests Prioritizer.json      # Feedback ingestion workflow
Features Logging.json                  # AI processing and prioritization
Feature Requests Error Workflow.json   # Global error notifications
```

## ⚖️ License

Distributed under the MIT License.
