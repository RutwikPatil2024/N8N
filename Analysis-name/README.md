# Automated Form Processing & Notification System

## Overview

This project is an automated workflow that processes user form submissions, enriches the data using external APIs, stores the results in a Google Sheet, and sends a notification via email.

It is designed to demonstrate seamless integration between APIs, data processing, and automation tools.

---

## Workflow Description

The system follows a structured pipeline:

1. **Form Submission Trigger**

   * The workflow starts when a user submits a form.
   * Captures user input.

2. **Age Prediction API**

   * Sends a request to an external API to estimate the user's age based on their name.

3. **Gender Prediction API**

   * Uses another API to determine the likely gender associated with the name.

4. **Nationality Prediction API**

   * Calls an API to predict nationality based on the name.

5. **Data Storage (Google Sheets)**

   * The processed data (name, age, gender, nationality) is appended to a Google Sheet for record-keeping.

6. **Email Notification**

   * Sends a confirmation or notification email with the processed information.

---

## Tech Stack

* **Automation Platform**: (n8n)
* **APIs Used**:

  * Age Prediction API
  * Gender Prediction API
  * Nationality Prediction API
* **Google Sheets API** for data storage
* **Gmail API** for email notifications

---

## Features

* Automated data processing pipeline
* Integration with multiple external APIs
* Real-time data storage in Google Sheets
* Automated email notifications
* Scalable and modular workflow design

---

## Use Cases

* Lead data enrichment
* Form-based automation systems
* Data collection and analytics pipelines
* CRM integrations

---

## Setup Instructions

1. Create a form that captures user input .
2. Connect the form to your automation platform.
3. Configure API calls:

   * Age prediction
   * Gender prediction
   * Nationality prediction
4. Connect Google Sheets:

   * Set up a sheet with appropriate columns.
   * Configure append row action.
5. Set up Gmail integration:

   * Configure email sending module.
6. Test the workflow with sample data.

---

## Workflow Structure

```
Form Submission → Age API → Gender API → Nationality API → Google Sheets → Email Notification
```

---

## Notes

* Ensure API endpoints are correctly configured.
* Handle API rate limits and errors appropriately.
* Validate input data before processing.

---

## Author

**Rutwik Patil**
