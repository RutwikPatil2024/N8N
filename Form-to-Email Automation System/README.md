# ⚡ Form Automation using n8n

## 📌 Overview

This project demonstrates **form automation** using n8n.
When a user submits a form, the data is processed automatically:

1. The data is stored in a Google Sheet
2. An email is sent to the entered email address

---

## 🚀 Workflow

* 📝 Form Submission
* 📊 Append data to Google Sheets
* 📧 Send email notification

---

## 🧠 How It Works

### 🔹 Step 1: Form Trigger

* User fills out a form
* Workflow starts automatically on submission

### 🔹 Step 2: Store Data

* Data is added as a new row in **Google Sheets**

### 🔹 Step 3: Send Email

* Email is sent using **Gmail integration**
* Message is delivered to the email entered in the form

---

## 🛠️ Tools Used

* n8n (Workflow Automation)
* Google Sheets (Data Storage)
* Gmail API (Email Sending)

---

## 📂 Workflow Structure

```id="3w8rhv"
Form Trigger → Google Sheets → Gmail
```

---

## ▶️ How to Use

1. Set up n8n locally or on a server
2. Create a form trigger (Webhook/Form node)
3. Connect Google Sheets node
4. Connect Gmail node
5. Activate the workflow

---

## 📊 Output

* Data is saved in Google Sheets
* Email is sent automatically to the user

---

## 🎯 Purpose

* Automate repetitive tasks
* Learn workflow automation
* Integrate multiple services

---

## 🚀 Future Improvements

* Add validation for form inputs
* Send confirmation messages
* Store data in database instead of sheets
* Add error handling

---

## 👨‍💻 Author

Rutwik Patil
