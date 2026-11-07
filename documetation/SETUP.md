Installation and Setup Guide

This guide explains how to import and configure the Employee Leave Management Automation workflows in n8n.

1. Prerequisites

Before starting, make sure you have:

A running n8n instance (self-hosted or cloud).

Access to n8n Data Tables.

An SMTP email account for sending notifications.

The exported workflow JSON files from the workflows directory.

2. Import Workflows

Open your n8n instance.

Navigate to the Workflows section.

Select the option to import a workflow from a file.

Import the following JSON files individually: 

employee-data-practice.json

leave-approval-workflow.json

leave-reports.json

Save the imported workflows.

3. Configure Data Tables

Create the following n8n Data Tables:

LeaveRequests

Approval History

Configure their columns according to the database structure described in DATABASE.md.

Make sure the column names and data types match the workflow configuration.

4. Configure Email Credentials

The workflows use SMTP integration to send employee notifications, manager approval requests, and reports.

Open the email nodes in n8n.

Configure your own SMTP credentials.

Set the appropriate sender email address.

Update recipient addresses and other email settings as needed.

Test the email connection.

Security Note: Never publish personal email addresses, passwords, SMTP credentials, or access tokens in a public repository.

5. Review Workflow Configuration

After importing the workflows:

Verify Data Table references.

Check form fields and validation rules.

Review email settings.

Verify manager approval logic.

Confirm that all node connections are correct.

6. Testing

Before using the system, test the following scenarios:

Submit a valid leave request of three days or fewer.

Submit a leave request exceeding three days.

Submit a duplicate leave request.

Test manager approval.

Test manager rejection with a rejection reason.

Generate and receive a leave statistics report.

7. Important Notes

Configure your own credentials before execution.

Data Tables must be created and configured in the target n8n instance.

Review all imported workflow settings before enabling them.

This repository contains workflow exports and documentation, not a hosted n8n service.