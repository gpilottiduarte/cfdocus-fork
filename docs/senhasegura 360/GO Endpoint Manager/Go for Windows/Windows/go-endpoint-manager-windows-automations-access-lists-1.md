# Automation access lists 

Configure access lists for automation in general segregation
Access the senhasegura platform.
Navigate to 
GO Endpoint Manager➔Policies➔Windows➔Access Lists.
Click 
View actions (⁝).
Select 
New general segregation.
Choose 
Automations.
In the window that appears, complete the fields:
Name:
 define a name for the list.
Status: 
choose between 
Enabled
 or 
Disabled.
Record session for these applications: 
choose between 
Enabled
 or
 Disabled.
Under 
Automations
, complete:
ID:
 the identifying number in the list of automation.
Automation: 
the automation name.
Click 
Add.
Continue completing the information on the 
Workflow
 tab.
 Check the options for 
Elevation settings:
Users can elevate applications.
Require reason to elevate applications.
Require approval to elevate applications.
Allow emergency access.
Approval in levels. 
To work, approvers must be registered in levels in the Approvers report.
 If you checked to 
Require approval
to elevate applications, set the number of times for each specific action:
Approvals required 
so the user can elevate the privilege and perform the action.
Disapprovals required 
to cancel the privilege elevation.
Choose 
Yes 
or 
No
to the Access request settings.
Governance ID required when justifying?*
Always add user manager to approvers?*
Save.
Configure access lists for automations in specific workstations
Access the senhasegura platform.
Navigate to 
GO Endpoint Manager➔Policies➔Windows➔Access Lists.
Click 
View actions (⁝).
Select 
New segregation for workstation.
Choose 
Automations.
In the window that appears, complete the fields:
Name:
 define a name for the list.
Status: 
choose between 
Enabled
 or 
Disabled.
Record session for these applications:
 choose between 
Enabled
 or 
Disabled.
Under 
Automations
, complete:
ID: 
the identifying number in the list of automations.
Automation:
 the automation name.
Click 
Add.
Under 
Workstations
, click on the + icon, and choose a workstation according to the criteria.
ID:
 identifier number in the list of workstations.
UUID: 
the unique identifier of the workstation.
Hostname:
 the name of the machine.
IP:
 the IP address of the workstation.
Click 
Add.
Still, in 
Workstations
, you will see more information.
Includer: 
the user who added the workstation.
Include:
 when the workstation was added.
Continue completing the information on the 
Workflow
 tab.
Check the options for 
Elevation settings:
Users can elevate applications.
Require reason to elevate applications.
Require approval to elevate applications.
Allow emergency access.
Approval in levels. 
To work, approvers must be registered in levels in the 
Approvers
 report.
 If you checked to 
Require approval
to elevate applications, set the number of times for each specific action:
Approvals required
 so the user can elevate the privilege and perform the action.
Disapprovals required 
to cancel the privilege elevation.
 Choose 
Yes
 or 
No
in the Access request settings.
G
overnance ID required when justifying?*
Always add user manager to approvers?*
 Save.