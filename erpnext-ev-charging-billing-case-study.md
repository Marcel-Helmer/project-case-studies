# ERPNext EV Charging Billing — Case Study

## Context

This case study describes an anonymized ERPNext/Frappe-based project developed during my practical training as an IT Specialist for Application Development.

The goal was to support a payroll-related workflow for reimbursing employee EV charging costs from private charging points.

No confidential code, internal data, customer data, company-specific screenshots, credentials, or proprietary business logic are included.

## Problem

The existing workflow required manual handling of charging data, electricity tariffs, reimbursement rates, and payroll-related values.

This created unnecessary manual effort and increased the risk of calculation errors, transfer mistakes, and inconsistent documentation.

## Goal

The goal of the project was to automate the import, calculation, and transfer of EV charging reimbursement data into an ERPNext-based payroll workflow.

The system needed to process charging data from CSV files, calculate reimbursement amounts, and transfer the calculated values into payroll-related ERPNext structures.

## My Role

My responsibilities included:

- Requirements analysis
- Technical planning
- Data model planning
- Backend implementation
- CSV import logic
- Calculation logic for fixed and time-variable electricity tariffs
- ERPNext/Frappe form integration
- Testing and documentation

## Tech Stack

- ERPNext
- Frappe Framework
- Python
- JavaScript
- MariaDB / MySQL
- CSV data processing

## Technical Approach

The solution was designed as an ERPNext/Frappe extension.

The backend logic handled CSV import, data normalization, tariff processing, and reimbursement calculation. The frontend integration supported user interaction inside ERPNext forms.

The CSV import logic needed to handle different CSV structures, delimiters, column names, and decimal formats. Consumption values were normalized and converted into a consistent format for further processing.

## Key Features

- CSV upload and parsing
- Detection of relevant consumption columns
- Normalization of decimal formats
- Conversion of energy values into kWh
- Support for fixed electricity tariffs
- Support for time-variable electricity tariffs
- Calculation of reimbursement amounts
- Transfer of calculated values into payroll-related fields
- Creation or update of a payroll-related compensation component
- Integration into an ERPNext-based payroll workflow

## Time-Variable Tariff Logic

One important part of the project was the calculation of time-variable electricity tariffs.

Charging sessions can overlap multiple tariff windows or continue across midnight. The calculation logic therefore needed to split charging intervals and calculate a weighted average electricity price based on the overlap with different tariff periods.

This made the calculation more robust and closer to realistic electricity pricing scenarios.

## Testing

The project was tested using multiple approaches:

- Functional testing from the user's perspective
- Internal logic testing
- Unit testing for tariff calculation logic

Special attention was given to edge cases such as charging sessions across tariff boundaries, sessions across midnight, decimal format differences, and invalid CSV input.

## Result

The prototype automated a previously manual workflow and connected CSV-based charging data with ERPNext payroll processing.

The project improved traceability, reduced manual calculation effort, and made reimbursement values easier to process in a structured ERP environment.

## What I Learned

This project helped me deepen my understanding of:

- ERPNext and Frappe-based development
- Backend logic in Python
- JavaScript form scripting in ERP systems
- Data normalization
- CSV parsing
- Business process automation
- Payroll-related data workflows
- Testing calculation-heavy application logic

## Confidentiality Notice

This case study is intentionally anonymized.

It does not include:

- Internal source code
- Company names
- Customer data
- Employee data
- Real payroll data
- Credentials
- Internal screenshots
- Proprietary templates
- Confidential business logic
