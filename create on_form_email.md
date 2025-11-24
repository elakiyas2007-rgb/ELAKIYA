Initial Steps

 1. **Create a New Workflow**

* Open your **n8n dashboard**.
* Click **Workflows → New**.
* Name it: `Form Submission Email Workflow`.

 2. **Add the Trigger Node**

Depending on how your form sends data, choose one of the following:

**Option A: Webhook Trigger**

* Add **Webhook Node**.
* Set **HTTP Method** → `POST`.
* Set **Path** → `/form-submit`.
* Save and activate to generate the public webhook URL.

 **Option B: Form Provider Trigger**

(Examples: Typeform, Google Forms, Jotform)

* Add the respective integration node.
* Authenticate using API keys/OAuth.
* Select the form you want to track.

---

 Node Descriptions

 1. **Webhook Node** (Trigger)

Captures form submission data and passes the form fields (name, email, message, etc.) to the next nodes.

**Purpose:** Entry point for data received from the form.

---
 2. **Set Node** (Data Structuring)

Used to clean, map, or prepare data before sending the email.

**Example fields to set:**

* `userName`
* `userEmail`
* `userMessage`

**Purpose:** Ensures consistent and structured data for the email node.

---

 3. **Email Node** (Mailer)

Sends an automated email using SMTP or any connected mail service.

**Supports:** Gmail, Outlook, SMTP, SendGrid, Mailgun, etc.

**Usage:**

* Configure SMTP credentials.
* Add subject, recipient email, and message template.

