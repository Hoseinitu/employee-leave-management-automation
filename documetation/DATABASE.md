Database Documentation

This document describes the data structure used in the Employee Leave Management Automation system.

The project uses n8n Data Tables to store employee leave requests and manager approval records.

1. LeaveRequests Table

Purpose: Stores employee leave requests and their processing status.

ColumnDescriptionidUnique identifier of the leave requestnameEmployee namedepartmentEmployee departmentleaveDaysNumber of requested leave daysstatusCurrent request statusrequestDateDate the request was submittedstartDateLeave start dateendDateLeave end dateemailEmployee email addresscreatedAtRecord creation timestampupdatedAtLast record update timestamp 

Request Status Values

Pending Approval: Waiting for a manager's decision.

Approved: Leave request approved.

Rejected: Leave request rejected.

2. Approval History Table

Purpose: Stores a history of manager decisions for leave requests.

ColumnDescriptionidUnique approval history record identifierrequestidID of the related leave requestemployeeNameEmployee nameemployeeEmailEmployee email addressdecisionManager's approval or rejection decisionrejectionReasonReason provided when a request is rejecteddecisionDateDate of the manager's decisioncreatedAtRecord creation timestampupdatedAtLast record update timestamp 

3. Relationship Between Tables

The requestid field in the Approval History table references the id field in the LeaveRequests table.

This relationship allows the system to associate each manager decision with its corresponding leave request.

One leave request can have an associated approval history record.

4. Data Management

The system uses these tables to:

Store employee leave requests.

Track request statuses.

Record manager decisions.

Maintain rejection reasons.

Generate statistical reports.

5. Data Flow

Employee submits a leave request.

The request is validated and stored in LeaveRequests.

Requests requiring approval are sent to a manager.

The manager's decision updates the request status.

The decision is recorded in Approval History.

The reporting workflow retrieves request records to calculate statistics.