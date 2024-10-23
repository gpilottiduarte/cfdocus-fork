# Create vendor access group 

To grant access to a third-party user, you must first create a vendor access group. Domum aggregates third-party users into vendor groups like it organizes employees into employee groups.
Caution
The vendor access group has no relation to the PAM module access group. The settings determined in the vendor's form are independent.
Access the senhasegura platform.
Go to 
Domum Remote Access➔Access Control➔Access Groups.
In the upper-right corner, click the 
(⁝) View Actions
 icon.
Select 
+ New
.
Complete the information in the 
New access group
's registration window.
Access group name*
Enabled.* 
Choose between 
Yes
 or 
No
.
Description
On the 
Settings
 tab, complete the required information.
Under
 Password preview settings
, select the preferred options.
Users can view a password
Require approval to view a password
If you checked this option, you must specify the number of 
Approvals required for viewing
 and the number of 
Disapprovals required to cancel
.
Approval in levels.
 Flag whether approvers will be triggered in levels. Thus, you can define a hierarchy of approvers.
Under 
Remote session settings
, select the preferred options.
Users can start session
.
 Mark the checkbox to permit users to initiate a proxy session using the credentials associated with this group.
Require approval to start session
. 
Flag whether another user must act as an approver to start the proxy session. 
Once active, you need to define the number of 
Approvals required
 to view and the number of 
Disapprovals required
 to cancel.
Approval in levels
.
 Flag whether the approvers will be triggered in tiers. This way, you can define a hierarchy of approvers.
In 
Access request settings
, choose 
Yes
 or 
No 
for the options:
Governance ID required when justifying?*
 Flag whether the applicant must enter an ITMS code at the time of justification.
Always add user manager to approvers?*
 Flag whether the manager should be automatically queried as an additional approver to this group. Therefore, the manager and the other approvers in the 
Approvers
 tab will be alerted.
Can third-party users request their own access?*
If you haven't selected the option for the group to require approvers, click 
Save
.
If you have selected the option for the group to require approval, provide the necessary information on the 
Approvers
 tab.
Click the 
+
 icon to add an approver.
Click 
Add.
The name of the approvers appears on the report. Note that approving users have a 
Level
 setting in their registry. This setting determines the calling sequence for approving the operation, allowing a hierarchy to be applied.
Info
If you are an approver, pending approval requests will be in the 
Domum Remote Access➔Access Control➔My Approvals 
menu.
If you are a user that needs approval, you can view your requests in the 
Domum➔Access Control➔My Requests 
menu.
Save.