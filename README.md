# Critical Incident Notification Workflow

## System Overview 

This system ensures that all Critical priority incidents related to network outages trigger immediate email notifications to the Network Operations team to avoid SLA breaches and service disruptions.

### Original Broken Workflow
#### Broken Email 
![Trigger](https://github.com/CodeWithLuwam/service-now-urgent-incident-notification-workflow/blob/main/Images/og%20Kura%20WL1%20Flow%20-%20Action.png?raw=true)
#### Broken Trigger
![Action](https://github.com/CodeWithLuwam/service-now-urgent-incident-notification-workflow/blob/main/Images/og%20Kura%20WL1%20Flow%20-%20Trigger.png?raw=true)

## Architecture Diagram
![Workflow Diagram](https://github.com/CodeWithLuwam/service-now-urgent-incident-notification-workflow/blob/main/Images/UrgentNetworkIncidentNotification.drawio.png?raw=true)

## Implementation Steps
1. Reviewed priority lookup rules.
2. Investigated and remediated 'Kura Workload 1' flow.
3. Renamed to 'Critical Network Incident Notification'.
4. Configured condition: Priority = 1 AND Category = Network.
   ![](https://github.com/CodeWithLuwam/service-now-urgent-incident-notification-workflow/blob/main/Images/Conditions.png?raw=true)
5. Created email notification linked to the incident table.
   ![](https://github.com/CodeWithLuwam/service-now-urgent-incident-notification-workflow/blob/main/Images/Notification%20Email.png?raw=true)
6. Testing:
   ![](https://github.com/CodeWithLuwam/service-now-urgent-incident-notification-workflow/blob/main/Images/Email%20Outbox.png?raw=true)
  

## AI Scenario
To improve global incident response, an AI agent could intelligently route incidents by analyzing engineer expertise, current availability, and overall workload. It would take time zones into account, assigning tasks to the most capable and available engineers across regions. By using historical resolution data and performance metrics, the AI can optimize future routing decisions, improving both speed and efficiency. This approach significantly reduces resolution times, balances workload distribution, and helps avoid overwhelming engineers who are either unavailable or less experienced. Over time, the system can learn and adapt, continuously improving incident management and enhancing overall team performance worldwide.



