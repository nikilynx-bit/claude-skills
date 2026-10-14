# Skill: Nominal Roll & Compliance Tracker Generator

## Objective
Extract the list of employees who have not completed their ESG training or data submission, format it as a "Nominal Roll", and generate actionable follow-up tasks.

## Instructions
1. **Filter Non-Compliant Employees**: Identify all rows where `ESG_Training_Completed` = "No" OR `ESG_Report_Submitted` = "No".
2. **Generate Nominal Roll**: Create a clean, tabular "check-off" list. Include Employee Name, Department, Manager (if available/inferred), and the specific missing action (Training vs. Report).
3. **Draft Follow-up Communications**: 
   - Generate a standardized, polite, but firm email template addressed to the non-compliant employees.
   - Generate a summary escalation email for their respective Department Heads.
4. **Tracking Mechanism**: Provide a markdown checklist format so the ESG admin can literally "check off" employees as they complete the requirements.

## Expected Output Format
1. **The Nominal Roll Table**: A markdown table with a `[ ]` checkbox column for tracking.
2. **Email Templates**: Two distinct email drafts (one for the employee, one for the manager).
3. **Action Plan**: A brief 3-step workflow for the ESG admin to close the compliance gap.
