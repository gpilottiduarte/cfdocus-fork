# Automatic update 

You can update the GO Endpoint Manager para Windows version by the senhasegura server. A New version verification is performed every time the workstation application is started.  
Configure automatic update
Step (1/4) — Get the installer
Go to 
PAM Solution
.
Select the agent version compatible with your version of the senhasegura platform.
Download the installer with the 
new version
 of 
GO Endpoint Manager for Windows.
Step (2/4) - Register the installer for an update
Access the senhasegura platform. 
Go to the menu 
GO Endpoint Manager ➔ Settings ➔ Installers
. 
Click the 
(
⁝)
 icon and choose the 
New 
option. 
Select the official 
GO Endpoint Manager for Windows
 MSI file in the 
Installation File
 field. 
Click 
Save
.
Step (3/4) - Approve an installer
When you approve an installer, it means you state your awareness of the latest version and the changes, features, and impacts it will bring to your business.
On the senhasegura platform, access the menu 
GO Endpoint Manager ➔ Settings ➔ Installers
. 
Click the 
(⁝) 
icon and choose the 
Approve Installation
 option.
Caution
Approving a version does not automatically make it available for upgrade. You need to register a schedule to complete the process.
Agent installers report
 
The records also allow you to disapprove a version of GO Endpoint Manager for Windows.
A deprecated version will prevent its use if it is already installed on any workstations.
After banning, the user will be alerted with the code 2028.
Important
Banning a version will disable it completely. You cannot reverse this action.
Step (4/4) - Register an update
On the senhasegura platform, access the menu 
GO Endpoint Manager ➔ Reports ➔ Updates
.
Click on the
 (⁝) 
icon and choose 
New
.
Fill in the fields in the 
Update registration
 form.
On the 
Criteria 
tab:
Define if the update will be mandatory or not.
Caution
Non-mandatory
 updates allow the user to decide whether to install the new version.
Mandatory
 updates do not allow the user to use the previously installed version.
In 
mandatory
 updates, when the user starts the application, it will be automatically updated.
Define if there will be an installation 
date/time
 limit. This field is only used for mandatory updates.
Choose a registered and approved installer.
After the update, you must enter a new installation key.
 On the 
Workstations 
tab:
 Add the workstations you want to register.
Click 
Save
.
Info
After creating the schedule, an update alert will appear when the user starts the GO Endpoint Manager application if the version added on the workstation is different from the version on the senhasegura platform.
Update events
To view ongoing update events and senhasegura logs, go to 
GO Endpoint Manager ➔ Reports ➔ Windows ➔ Events,
 and select 
Update
 in 
Event
.
Update event report
 
Read more
Install agent
Typical screen