On-Click Email n8n Workflow

This document describes the initial setup and node functions for creating an **on-click email workflow** in **n8n**.

 Initial Steps

1. Create a New Workflow

   * Open your n8n dashboard and click **“New Workflow”**.
   * Name the workflow something like: **On-Click Email Trigger**.

2. Add the Trigger Node

    Insert a **Webhook** node to serve as the “on-click” trigger.
    Set the HTTP method to **GET** or **POST** (depending on your use-case).
    Copy the generated webhook URL—this is what your button or system will call.

3. Add the Email Node

    Add the **Email Send** node.
   Select your email provider (SMTP, Gmail, Outlook, etc.).
    Configure credentials or select an existing one.
    Draft the email subject and body.

4. Connect the Nodes

Link the **Webhook** → **Email Send** node so the click event triggers the outgoing message.



 Node Descriptions

1. Webhook Node

Purpose: Triggers the workflow when an external click or request hits the webhook URL.
  Key Settings:

  HTTP Method: GET or POST
    Path: Custom URL segment (e.g., `/send-email`)
    Response Mode: Optional—may return a confirmation message
  Usage: Integrate into a button, script, or external system to start the workflow.


2. Email Send Node

Purpose: Sends an email once the webhook trigger is activated.
Key Settings:

  Email Service: SMTP, Gmail, Outlook, etc.
  Recipient(s): Single or multiple
  Subject and Body: Can include static text or dynamic data from webhook
Usage: Generates and sends the outgoing email based on the trigger event.

<img width="1920" height="1032" alt="▶️ My workflow 2 - n8n - Google Chrome 21-11-2025 14_32_27" src="https://github.com/user-attachments/assets/1eb91564-c613-4ac7-845a-8d7957e03eef" />
