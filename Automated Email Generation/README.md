# 📧 Automated Email Generation Workflow (n8n)

## Overview

This project implements an automated workflow using **n8n** to collect user data, enrich it using external APIs, process it, and generate a **professional HTML email** using AI. The final output is automatically sent via email.

The workflow is designed to be modular, scalable, and suitable for real-world automation use cases such as onboarding, lead processing, and profile-based communication.

---

## 🚀 Workflow Summary

The automation follows this sequence:

1. **Form Submission Trigger**
2. **Fetch Age Based on Name**
3. **Determine Gender**
4. **Fetch Nationality**
5. **Store Data in Google Sheets**
6. **Generate Email using AI (OpenAI)**
7. **Parse AI Output (JSON Extraction)**
8. **Send Email via Gmail**

---

## 🧩 Nodes Breakdown

### 1. On Form Submission

* Trigger node that starts the workflow when user data is submitted.
* Captures fields like:

  * Name
  * Email
  * Other relevant inputs

---

### 2. HTTP Request 3 – Age API

* Fetches estimated age based on the user's name.
* Example API: `https://api.agify.io`

---

### 3. HTTP Request 4 – Gender API

* Predicts gender using name.
* Example API: `https://api.genderize.io`

---

### 4. HTTP Request 5 – Nationality API

* Predicts nationality based on name.
* Example API: `https://api.nationalize.io`

---

### 5. Append Row in Sheet

* Stores enriched user data into Google Sheets.
* Useful for:

  * Record keeping
  * Analytics
  * CRM-like tracking

---

### 6. Message a Model (OpenAI)

* Generates a **professional email** using AI.

* Input includes:

  * Name
  * Age
  * Gender
  * Nationality

* Output:

  * JSON containing:

    * `subject`
    * `body` (HTML email)

---

### 7. Code in JavaScript

* Parses AI response (since it returns JSON as string).
* Extracts usable fields:

```javascript
const raw = $json.output[0].content[0].text;
const parsed = JSON.parse(raw);

return [
  {
    json: parsed
  }
];
```

---

### 8. Send a Message (Gmail)

* Sends the generated email.
* Uses:

  * Subject → `{{$json.subject}}`
  * Body → `{{$json.body}}` (HTML)

---

## 🛠️ Technologies Used

* **n8n** – Workflow automation
* **OpenAI API** – AI email generation
* **Google Sheets API** – Data storage
* **REST APIs**:

  * Agify (Age)
  * Genderize (Gender)
  * Nationalize (Nationality)
* **Gmail API** – Email delivery

---

## ✨ Key Features

* Fully automated pipeline from input to email delivery
* AI-generated professional HTML emails
* Real-time data enrichment via APIs
* Structured JSON handling and parsing
* Scalable and modular workflow design

---

## 📌 Use Cases

* Lead generation and follow-up emails
* User onboarding automation
* CRM enrichment workflows
* Personalized communication systems

---

## ⚙️ Setup Instructions

1. Import the workflow into n8n
2. Configure credentials:

   * OpenAI API
   * Gmail
   * Google Sheets
3. Update API endpoints if needed
4. Test using sample form input
5. Activate workflow

---

## 🔍 Notes

* Ensure proper error handling for API failures
* Validate JSON parsing in the Code node
* Customize email template as needed
* Monitor execution logs for debugging

---

## 👤 Author

**Rutwik Patil**
