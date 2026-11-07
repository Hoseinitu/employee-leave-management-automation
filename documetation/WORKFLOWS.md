Workflow Documentation

This document describes the three workflows that form the Employee Leave Management Automation system.

1. Employee Data Practice

Purpose: Automate employee leave request submission, validation, and initial processing.

Main Process

1. Receive leave request information through an n8n form.
2. Validate the submitted data and leave duration.
3. Calculate the number of requested leave days.
4. Check for duplicate requests based on employee name and leave dates.
5. Save valid requests in the "LeaveRequests" data table.
6. If the requested leave exceeds three days, send an approval request to the manager.
7. Send an appropriate notification email to the employee.

Key Features

- Form-based leave submission
- Input validation
- Automatic leave duration calculation
- Duplicate request detection
- Conditional manager approval
- Automated email notifications

2. Leave Approval Workflow

Purpose: Handle manager decisions for leave requests requiring approval.

Main Process

1. Present a manager decision form.
2. Retrieve the corresponding leave request.
3. Process the manager's approval or rejection decision.
4. Update the request status.
5. Record the decision in the "Approval History" data table.
6. Notify the employee of the final decision.

Key Features

- Manager approval and rejection
- Rejection reason capture
- Automatic request status updates
- Approval history tracking
- Employee email notifications

3. Leave Reports

Purpose: Generate and email statistical reports about leave requests.

Main Process

1. Start the workflow manually.
2. Retrieve leave request records from the data table.
3. Calculate leave management statistics using JavaScript.
4. Generate a report containing:
   - Total requests
   - Approved requests
   - Rejected requests
   - Pending requests
   - Total approved leave days
   - Approval rate
   - Rejection rate
5. Send the report by email.

Key Features

- Automated statistical calculations
- JavaScript-based data processing
- Approval and rejection rate calculation
- Pending request monitoring
- Email-based reporting

Workflow Architecture

The system consists of three interconnected automation workflows:

- Employee Data Practice: Receives and processes employee leave requests.
- Leave Approval Workflow: Handles manager decisions and records approval history.
- Leave Reports: Generates management statistics and sends reports.

The workflows use n8n Data Tables for data storage and SMTP email integration for notifications and reporting.

Data Storage

LeaveRequests

Stores employee leave request information, including employee details, leave duration, request status, dates, and email address.

Approval History

Stores manager decisions, including the related request ID, employee information, decision, rejection reason, and decision date.

Technologies Used

- n8n
- JavaScript
- n8n Data Tables
- SMTP / Gmail
- Git and GitHub