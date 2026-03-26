# Salesforce Case Management System

## Overview
This project is a Salesforce-based Case Management System built to simulate a real-world customer support solution. It helps support teams create, assign, track, escalate, and resolve customer issues efficiently while maintaining SLA compliance.

The project was designed to showcase Salesforce development skills including Apex, Lightning Web Components, Flow automation, integration patterns, and scalable design practices.

## Features
- End-to-end case lifecycle management
- Automatic case assignment based on priority/category
- SLA due date calculation
- Scheduled escalation for overdue cases
- Custom LWC dashboard for support teams
- External REST API integration for customer information
- Reports and dashboards for operational insights
- Bulk-safe Apex design and test coverage

## Tech Stack
- Salesforce Platform
- Apex
- Lightning Web Components (LWC)
- Flow
- SOQL
- REST API
- Named Credentials
- Salesforce DX
- Git and GitHub

## Architecture
The solution follows a layered design:
- LWC for user interaction and dashboards
- Apex trigger handler/service classes for business logic
- Flow for declarative automation
- REST integration layer for external customer data
- Reports and dashboards for visibility and analytics

## Core Objects
### Standard Objects
- Case
- Account
- Contact

### Custom Case Fields
- SLA_Due_Date__c
- Escalated__c
- Case_Category__c
- Customer_External_Id__c
- Resolution_Notes__c
- Assigned_Queue_Name__c

## Key Business Flows
1. A support case is created manually or through integration.
2. The system calculates SLA due date.
3. The case is assigned to the correct queue/agent.
4. A scheduled job checks for overdue cases.
5. Overdue cases are escalated automatically.
6. Support agents track and update case progress from the dashboard.

## Setup Instructions
1. Clone the repository
2. Authorize your Salesforce org
3. Deploy metadata using Salesforce DX
4. Assign permission sets
5. Configure Named Credentials for external API
6. Load sample data
7. Run Apex tests

## Sample Deployment Commands
```bash
sf project deploy start --target-org <alias>
sf apex test run --target-org <alias> --code-coverage --result-format human