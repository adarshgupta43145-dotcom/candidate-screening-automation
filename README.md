# Candidate Screening & Interview Scheduling Automation

An automated candidate screening and interview scheduling workflow built using **n8n, Google Sheets, Gmail, and OpenAI**.

## 📌 Project Overview

This project automates the candidate recruitment process from resume submission to candidate status updates and email notifications.

The workflow processes incoming resumes, extracts candidate information, stores the data in Google Sheets, checks for duplicate candidates, and automatically sends notifications based on the candidate's selection status.

## 🔐 Account & Credentials Setup

Before running the workflow, connect the required accounts and credentials in n8n.

### 1. Gmail Account

1. Open n8n and go to **Credentials**.
2. Create a new **Gmail OAuth2** credential.
3. Sign in with the Gmail account that will receive candidate resumes and send automated emails.
4. Grant the required permissions.
5. Select this credential in the Gmail Trigger and Gmail email nodes.

### 2. Google Sheets Account

1. Go to **Credentials** in n8n.
2. Create a new **Google Sheets OAuth2** credential.
3. Sign in with the Google account that contains the candidate tracking sheet.
4. Grant Google Sheets access.
5. Select this credential in the Google Sheets nodes.
6. Update the Spreadsheet and Sheet references if required.

### 3. OpenAI Account

1. Create an OpenAI API credential in n8n.
2. Add your OpenAI API key.
3. Select the credential in the AI/OpenAI node used for candidate information extraction.

## ⚙️ Workflow Setup

1. Import the workflow JSON file into n8n.
2. Configure the Gmail credentials.
3. Configure the Google Sheets credentials.
4. Configure the OpenAI API credentials.
5. Update the Google Sheet references if required.
6. Activate or publish the workflow.
7. Send a resume to the configured Gmail account to test the automation.

## 🚀 Features

- Resume received through Gmail trigger
- Attachment validation
- Resume PDF parsing
- AI-powered candidate detail extraction
- Candidate information normalization
- Duplicate candidate detection
- Candidate data storage in Google Sheets
- Candidate status monitoring
- Automatic selection email
- Automatic rejection email
- HR notification for selected candidates
- Google Sheet status updates

## 🔄 Workflow Process

1. A candidate submits a resume through email.
2. The Gmail Trigger starts the workflow.
3. The resume attachment is extracted and validated.
4. The PDF resume is parsed.
5. Candidate details such as Name, Email, Phone, Skills, Experience, Applied Role, and Resume Summary are extracted.
6. The candidate data is normalized.
7. Duplicate candidates are detected.
8. Unique candidate information is stored in Google Sheets.
9. HR can update the candidate status in Google Sheets.
10. Based on the status:
   - Selected candidates receive a next-round confirmation email.
   - Rejected candidates receive a respectful rejection email.
   - HR receives a notification to schedule the second-round interview.
11. Candidate processing status is updated in Google Sheets.

## 🛠️ Technologies Used

- n8n
- Gmail
- Google Sheets
- OpenAI
- JavaScript
- PDF Resume Parsing

## 📊 Candidate Information Stored

The following information is maintained in Google Sheets:

- Candidate ID
- Name
- Email
- Phone
- Skills
- Experience
- Applied Role
- Resume Summary
- Resume File/Link
- Status
- Received Date
- Processed Date
- Candidate Status
- Last Processed Status
- Candidate Email Sent
- HR Notification Sent

## 📸 Screenshots

### Complete n8n Workflow

![Complete Workflow](screenshots/screenshots/workflow.png.png)

### Google Sheet

![Google Sheet](screenshots/screenshots/google-sheet.png.png)

### Selected Candidate Email

![Selected Candidate Email](screenshots/screenshots/selected-candidate-email.png.png)

### Rejected Candidate Email

![Rejected Candidate Email](screenshots/screenshots/rejected-candidate-email.png.png)

### HR Notification Email

![HR Notification Email](screenshots/screenshots/hr-notification-email.png.png)

## 📂 Repository Structure

```text
candidate-screening-automation/
│
├── Candidate-Screening-Automation.json
├── README.md
│
└── screenshots/screenshots
    ├── workflow.png.png
    ├── google-sheet.png.png
    ├── selected-candidate-email.png.png
    ├── rejected-candidate-email.png.png
    └── hr-notification-email.png.png
