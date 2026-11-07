Employee Leave Management Automation

An automated employee leave management system built with n8n, JavaScript, and n8n Data Tables.

This project automates the employee leave request process, manager approval decisions, email notifications, and leave statistics reporting.

Project Overview

Managing employee leave requests manually can be time-consuming and difficult to track.

This project provides an automated workflow-based solution that helps streamline the process, reduce duplicate requests, maintain approval records, and generate management reports.

Key Features

Employee leave request submission through forms

Automatic leave duration calculation

Input validation

Duplicate request detection based on employee name and leave dates

Conditional manager approval for requests exceeding three days

Automated approval and rejection processing

Rejection reason tracking

Employee email notifications

Approval history management

Automated leave statistics and email reports

Workflow Architecture

The system consists of three main n8n workflows.

1. Employee Data Practice

Handles employee leave request submission and initial processing.

Main responsibilities:

Collect employee information.

Validate leave request data.

Calculate leave duration.

Detect duplicate requests.

Store valid requests.

Send manager approval emails when required.

Notify employees by email.

2. Leave Approval Workflow

Handles manager decisions for leave requests requiring approval.

Main responsibilities:

Collect manager decisions through a form.

Retrieve the corresponding leave request.

Approve or reject requests.

Capture rejection reasons.

Update request statuses.

Save approval history.

Notify employees of the decision.

3. Leave Reports

Generates statistical reports about employee leave requests.

Main responsibilities:

Retrieve leave request records.

Calculate total, approved, rejected, and pending requests.

Calculate total approved leave days.

Calculate approval and rejection rates.

Send reports through email.

Technologies Used

TechnologyPurposen8nWorkflow automationJavaScriptData processing and calculationsn8n Data TablesData storageSMTP / GmailEmail notifications and reportingGitVersion controlGitHubSource code hosting and documentation 

Project Structure

Employee-Leave-Management-Automation/ │ ├── workflows/ │ ├── employee-data-practice.json │ ├── leave-approval-workflow.json │ └── leave-reports.json │ ├── documentation/ │ ├── WORKFLOWS.md │ ├── DATABASE.md │ └── SETUP.md │ ├── screenshots/ │ └── README.md 

Data Storage

The project uses two n8n Data Tables.

LeaveRequests

Stores employee information, leave dates, requested leave days, email addresses, and request statuses.

Approval History

Stores manager decisions, rejection reasons, employee details, and references to the corresponding leave requests.

For more details, see Database Documentation.

Installation and Setup

Clone this repository:

git clone https://github.com/Hoseinitu/employee-leave-management-automation.git 

Open your n8n instance.

Import the three workflow JSON files from the workflows directory.

Create and configure the required Data Tables.

Set up your own SMTP credentials.

Review workflow settings and test each process.

For detailed instructions, see SETUP.md.

Documentation

Workflow Documentation

Database Documentation

Installation and Setup Guide

Security

Credentials and passwords should never be committed to the repository.

Configure your own SMTP credentials in n8n.

Review workflow exports before publishing them publicly.

Use placeholder email addresses in public examples.

Project Goals

This project demonstrates practical experience with:

Business process automation

Workflow design and development

JavaScript-based data processing

Data management

Conditional logic

Email integration

Version control and technical documentation

Author
Workflow Screenshots

1. Employee Data Practice

"Employee Data Practice" (screenshots/employee-data-practice.png)

2. Leave Approval Workflow

"Leave Approval Workflow" (screenshots/leave-approval-workflow.png)

3. Leave Reports

"Leave Reports" (screenshots/leave-reports.png)

Hosein

GitHub: Hoseinitu