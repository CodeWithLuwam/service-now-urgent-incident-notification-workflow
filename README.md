# Urgent Incident Notification Workflow

## System Overview 

This system ensures that all Critical priority incidents related to network outages trigger immediate email notifications to the Network Operations team to avoid SLA breaches and service disruptions.

### Original Broken Workflow
#### Broken Email 
![Trigger](https://github.com/CodeWithLuwam/service-now-urgent-incident-notification-workflow/blob/main/Images/og%20Kura%20WL1%20Flow%20-%20Action.png?raw=true)
#### Broken Trigger
![Action](https://github.com/CodeWithLuwam/service-now-urgent-incident-notification-workflow/blob/main/Images/og%20Kura%20WL1%20Flow%20-%20Trigger.png?raw=true)

## Architecture Diagram
See Diagram.png for a complete visual workflow.
![Workflow Diagram](https://github.com/CodeWithLuwam/service-now-urgent-incident-notification-workflow/blob/main/Images/UrgentNetworkIncidentNotification.drawio.png?raw=true)

## Implementation Steps
1. Reviewed priority lookup rules.
2. Investigated and remediated 'Kura Workload 1' flow.
3. Renamed to 'Critical Network Incident Notification'.
4. Configured condition: Priority = 1 AND Category = Network.
 ![](https://github.com/CodeWithLuwam/service-now-urgent-incident-notification-workflow/blob/main/Images/Conditions.png?raw=true)
5. Created email notification linked to the incident table.
   ![](https://github.com/CodeWithLuwam/service-now-urgent-incident-notification-workflow/blob/main/Images/Notification%20Email.png?raw=true)
6. Verified email records in sys_email after testing.

## AI Scenario
To improve global response, an AI agent could route incidents based on engineer expertise, availability, and workload. The AI would analyze time zones, assign incidents to the most capable available engineer, and use historical resolution data to optimize future routing. This reduces resolution times and prevents overload on unavailable or less experienced team members.



