# Uninstaller access lists 

Configure access lists for applications in general segregation
Access the senhasegura platform.
Navigate to 
GO Endpoint Manager➔Policies➔Windows➔Access Lists.
Click 
View actions (⁝).
Select 
New general segregation.
Choose 
Uninstallers.
In the window that appears, complete the fields:
Name:
 define a name for the list.
Action:
 choose between 
Allowlist 
or 
Denylist.
Status
: choose between 
Enabled
 or 
Disabled.
Record session for these applications:
 choose between 
Enabled
 or 
Disabled.
Under 
Uninstallers
, complete:
Criteria: 
choose one or more.
Certificate:
 the certificate in the application has a fixed value called 
Trusted Only
, The certificate with this rule active will be validated.
COM class ID:
 information in GUID format present in all applications.
Directory:
 application path. The registered path must be identical to the file to be checked with the rule.
File hash: 
unique information that each file has. With each change made to the file, a new hash is generated.
Caution
If you have a rule that uses the File hash criterion, only this criterion will be considered. The Product name and Directory criteria will be ignored. If the access list contains multiple file hashes, they will be evaluated with an "OR" condition.
File version:
 the version of the file.
Internet zone identifier: 
refers to the source of the file downloaded from the internet. Usually, all downloaded files are classified as ‘Internet Zone’. However, installed executables have this information classified as ‘Local Zone’.
Product name: 
the name of the program. It evaluates both the filename and the program name.
Product version:
 version specification.
Source URL:
 refers to the URL from which the file was downloaded. The file can only be executed if the source URL is correct and validated.
Upgrade code: 
this information is also a GUID for each program and can be found in the Windows registry.
Vendor name: 
vendor's name.
Windows store publisher: 
refers to apps downloaded from the Microsoft Store. It is validated in the file directory: ProgramFiles (and x86) and the hidden WindowsApps folder.
Info
DLLs work like applications and can be filtered by 
Product name, Product version, Certificate, File version, Directory, File hash, Internet zone identifier
, and
 Windows store publisher.
Rule:
 fill in according to the chosen criteria.
Caution
When populating the list with more than one criterion - 
Product version, Product name
 - the evaluation condition will be 
"AND"
. The final result matches the rule only if these two conditions are satisfied.
When populating the list with multiple criteria and different rules for one of them - 
Product version 10, Product name A, Product name B
  - the evaluation condition will be 
"AND"
 for the criteria and 
"OR"
 for the rules. In other words: 
Product Version 10 AND (Product Name A OR Product Name B)
.
Click 
Add.
If you chose 
Denylist
, select 
Save
. You will receive a confirmation message.
If you chose 
Allowlist
, continue completing the information on the 
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
Require approval to elevate applications
, set the number of times for each specific action:
Approvals required
 so the user can elevate the privilege and perform the action.
Disapprovals required
 to cancel the privilege elevation.
Choose 
Yes 
or 
No
 to the 
Access request settings.
Governance ID required when justifying?*
Always add user manager to approvers?*
Save.
Configure access lists for applications in specific workstations
Access the senhasegura platform.
Navigate to 
GO Endpoint Manager➔Policies➔Windows➔Access Lists.
Click 
View actions (⁝).
Select 
New segregation for workstation.
Choose 
Uninstallers.
In the window that appears, complete the fields:
Name:
 define a name for the list.
Action:
 choose between 
Allowlist
 or 
Denylist.
Status:
 choose between Enabled or Disabled.
Record
 session for these applications: choose between Enabled or Disabled.
Under 
Uninstallers
, complete:
Criteria: 
choose one or more.
Certificate:
 the certificate in the application has a fixed value called 
Trusted Only
, The certificate with this rule active will be validated.
COM class ID: 
information in GUID format present in all applications.
Directory:
 application path. The registered path must be identical to the file to be checked with the rule.
File hash: 
unique information that each file has. With each change made to the file, a new hash is generated.
Caution
If you have a rule that uses the File hash criterion, only this criterion will be considered. The Product name and Directory criteria will be ignored. If the access list contains multiple file hashes, they will be evaluated with an "OR" condition.
File version: 
the version of the file.
Internet zone identifier:
 refers to the source of the file downloaded from the internet. Usually, all downloaded files are classified as ‘Internet Zone’. However, installed executables have this information classified as ‘Local Zone’.
Product name: 
the name of the program. It evaluates both the filename and the program name.
Product version:
 version specification.
Source URL:
 contains information having video files.
Upgrade code: 
this information is also a GUID for each program and can be found in the Windows registry.
Vendor name:
 vendor's name.
Windows store publisher:
 refers to apps downloaded from the Microsoft Store. It is validated in the file directory: ProgramFiles (and x86) and the hidden WindowsApps folder.
Info
DLLs work like applications and can be filtered by 
Product name, 
Product version
,
 Certificate, File version, 
Directory,
 
File hash
, 
Internet zone identifier
, and 
Windows store publisher.
Rule:
 fill in according to the chosen criteria.
Caution
When populating the list with more than one criterion - 
Product version, Product name
 - the evaluation condition will be 
"AND"
. The final result matches the rule only if these two conditions are satisfied.
When populating the list with multiple criteria and different rules for one of them - 
Product version 10, Product name A, Product name B
  - the evaluation condition will be 
"AND"
 for the criteria and 
"OR"
 for the rules. In other words: 
Product Version 10 AND (Product Name A OR Product Name B)
.
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
Save.
If you chose 
D
enylist
, select 
Save. 
You will receive a confirmation message.
If you chose 
A
llowlist
, continue completing the information on the 
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
Approvers report
.
If you checked to 
Require approval to elevate applications
, set the number of times for each specific action:
Approvals required
 so the user can elevate the privilege and perform the action.
Disapprovals required
 to cancel the privilege elevation.
Choose 
Yes
 or 
No
 in the 
Access request settings.
Governance ID required when justifying?*
Always add user manager to approvers?*
Save.
Info
Rules will be applied for applications launched on GO Endpoint Manager agents and those launched outside of GO Endpoint Manager. Segregation rule values can be filled with regular expressions.
Read more
Typical screens
Automation
Approval workflow for applications