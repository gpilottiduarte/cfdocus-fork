# How to use the Emergency panel 

This article provides a guide on performing essential configurations in the Emergency panel. This functionality allows you to end all ongoing sessions or freeze access for predefined devices. The panel also allows you to block access to senhasegura, even through API or GO Endpoint Manager, for a specified period.
Requirements
A user with the 
System Administrator
 role. This role is the only one with the System.EmergencyPanel.Control permission.
An 
active MFA
 for the user.
Terminate sessions
Caution
Performing this action will end all ongoing sessions managed by senhasegura. To prevent users from starting new sessions, activate the Freezing or Lockdown.
To terminate sessions, follow these steps:
In the top right corner, click 
Emergency panel
, identified by the caution icon.
Select 
Terminate sessions
.
On the new page, enter the 
Access token
 generated by your MFA solution.
Click 
Validate token
.
Enter the 
Justification
 and, if necessary, a 
Governance Code
. 
Click 
Apply
 to complete the termination.
Freezing
Caution
Users won’t be able to start new sessions on predefined devices when activating the Freezing. Only administrator users can start sessions during freezes.
Requirements
Enable the 
Block during freezes?
 field in the PAM Core Access group settings.
To prevent the start of sessions on specific devices, follow these steps:
In the top right corner, click 
Emergency panel
, identified by the caution icon.
Select 
Freezing
.
On the new page, enter the 
Access token
 generated by your MFA solution.
Click 
Validate token
.
Set the freeze 
Start
 and 
Duration
.
Enter the 
Justification
 and, if necessary, a 
Governance Code
. 
Click 
Save
 to set the freeze.
The freeze applies only to devices in 
Access Groups
 with the 
Block during freezes?
 field enabled. These users are informed that their access to devices is blocked until the end of the freeze. During the freeze period, the user can track the time left until it ends.
Caution
Editing an access group during the freeze period may change the list of affected devices.
Cancel freeze
In the top left corner, click 
Grid Menu ⁝⁝⁝
, identified by the box with nine squares, and select 
Reports
.
Select 
Emergency panel ➔ Freezing
.
Locate the freeze. You can suspend only freezes with pending or ongoing status.
Click 
Cancel
, identified by the trash bin icon.
On the new page, enter the 
Access token
 generated by your MFA solution.
Enter the 
Justification
 and, if necessary, a 
Governance Code
.
Click 
Save
 to end the freeze.
Info
In the 
Action
 column, you'll also find the 
Details
 and 
Devices
 items, which offer additional information about the events.
Lockdown
Caution
All accesses, including the web interface, API calls, and GO Endpoint Manager users, will be blocked when activating the Lockdown. All ongoing sessions will be terminated, and all users will be logged out. Only administrator users can access senhasegura via the web interface during the lockdown.
Attention
This option can cause downtime for services using senhasegura via API.
To interrupt all sessions, follow these steps:
In the top right corner, click 
Emergency panel
, identified by the caution icon.
Select 
Lockdown
.
On the new page, enter the 
Access token
 generated by your MFA solution.
Click 
Validate token
.
Set the lockdown 
Start
 and 
Duration
.
Enter the 
Justification
 and, if necessary, a 
Governance Code
.
Click 
Save
 to set the lockdown.
The platform informs users that their access to devices is blocked. During the lockdown period, users can track the time left until it ends.
API calls will receive the following message:
{
    "response": {
        "status": 503,
        "mensagem": "senhasegura is under Lockdown until 09/08/2022 22:54:00",
        "erro": true,
        "cod_erro": 100,
        "message": "senhasegura is under Lockdown until 09/08/2022 22:54:00",
        "error": true,
        "error_code": 100
    }
}
Cancel lockdown
In the top left corner, click 
Grid Menu ⁝⁝⁝
, identified by the box with nine squares, and select 
Reports
.
Select 
Emergency panel ➔ Lockdown
.
Locate the lockdown. You can suspend only lockdowns with pending or ongoing status.
Click 
Cancel
, identified by the trash bin icon.
On the new page, enter the 
Access token
 generated by your MFA solution.
Enter the 
Justification
 and, if necessary, a 
Governance Code
.
Click 
Save
 to end the lockdown.
Info
In the 
Action
 column, you'll also find the 
Details
 item, which offers additional information about the events.
Emergency Panel Notifications
To add notifications, follow these steps:
In the top left corner, click 
Grid Menu ⁝⁝⁝
, identified by the box with nine squares, and select 
Settings
.
Select 
Notifications ➔ Settings
.
In the top right corner, click 
View actions
, identified by the three vertical dots icon.
Select 
New notification
.
For the 
Notification name
, set a title.
Choose how to notify the user: Email, Screen, or SMS.
Check 
Send notifications only to contacts who have access to credentials or devices
 if you want to restrict the recipients.
In the 
Notifications
 tab, click on the icon identified by the plus sign.
In the 
Category
 field, select 
Emergency panel
.
Click 
Filter
.
Choose among the options linked to the Emergency panel.
Click 
Add
.
In the 
Contacts
 tab, click on the icon identified by the plus sign to add users who will receive the notifications.
Click 
Save
 to set the notification.
Info
To learn more about Notifications, refer to the 
section on this topic
.
Do you still have questions? Reach out to the 
senhasegura Community
.