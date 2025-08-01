# service-now-urgent-incident-notification-workflow

# Urgent Incident Notification Workflow

## System Overview
This system ensures that all Critical priority incidents related to network outages trigger immediate email notifications to the Network Operations team to avoid SLA breaches and service disruptions.

## Implementation Steps
1. Reviewed priority lookup rules.
2. Investigated and remediated 'Kura Workload 1' flow.
3. Renamed to 'Urgent Network Incident Notification'.
4. Configured condition: Priority = 1 AND Category = Network.
   <img width="981" height="646" alt="Screen Shot 2025-08-01 at 12 22 14 PM" src="https://github.com/user-attachments/assets/aa056590-422d-47da-b41b-3385faba2cc2" />


5. Created email notification linked to the incident table.
   - Before the Send Email step, insert a "Lookup Records" action to get users from the sys_user_grmember table, then plug into email action.
   <img width="1203" height="572" alt="Screen Shot 2025-08-01 at 12 45 49 PM" src="https://github.com/user-attachments/assets/424b7602-016d-46d6-ab96-61c3be4aa333" />

6. Verified email records in sys_email after testing.

## AI Scenario
To improve global response, an AI agent could route incidents based on engineer expertise, availability, and workload. The AI would analyze time zones, assign incidents to the most capable available engineer, and use historical resolution data to optimize future routing. This reduces resolution times and prevents overload on unavailable or less experienced team members.

## Architecture Diagram
See Diagram.png for a complete visual workflow.

![WorkFlow Diagram](https://github.com/CodeWithLuwam/service-now-urgent-incident-notification-workflow/blob/main/Images/Screen%20Shot%202025-08-01%20at%202.38.40%20PM.png?raw=true)
