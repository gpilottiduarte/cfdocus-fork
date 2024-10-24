# Automation 

The application allows GO Endpoint Manager for Windows to authenticate installed applications or web pages accessed directly from the user's workstation. The automation uses the selected credential in GO Endpoint Manager for Windows to fill in the username and password. 
When opening the application, it displays the following image:
Automation
 
 
In the top left corner is the search bar.
In the top right corner is the 
Refresh
 button.
Below the Search bar, you have the titles:
Associated Credential: 
this shows which credential is associated with the automation.
Automations registered in 
RemoteApp
 in 
PAM Core
 are always associated with a credential. If you can view the credential, you can run the automation. Assume you have authentication parameters configured on 
RemoteApp
. In this case, the associated credential information will run the automation.
The automation registered in 
GO Automation
 is available to the user through access lists categorized as automation. Suppose you have authentication parameters configured in automation. In this case, the Automation application will ask the user to choose a credential to run the automation. If you don't have any authentication parameters configured in the automation, you don't need to select a credential.
Automation runs the automation configured in Go Endpoint Manager for Windows and 
RemoteApp
 in 
PAM Cor
e. When executing one automation, the Automation elevates privileges.
Automation recording
To record the automation registered in GO Endpoint Manager, check if the recording option in the general parameters and the access list is active. If you only mark the general parameter as active and the access list as inactive, the system only records the execution of the RemoteApp automation. Thus, four situations are possible:
Access list - Record the session of these applications?
General Parameter/Segregated Parameter - Allow Session Recording?
Automation
Active
Inactive
Not recorded.
Active
Active
Recorded.
Inactive
Active
Only RemoteApp is recorded.
Inactive
Inactive
Not recorded.
To configure session recording, check the instructions at: 
configure parameters for recording
.
Masks for RemoteApp on GO Windows
The following table presents the supported masks for RemoteApp on Go Windows during automation execution. These masks are used to replace information contained in credentials.
Tag
Description
[username]
Replaces the mask with the credential's 
Username.
[password]
Replaces the mask with the credential's 
Password.
[domain]
Replaces the mask with the credential's 
Domain.
[hostname]
Replaces the mask with the device's 
Name.
[host_ip]
Replaces the mask with the device's 
IP address.
Configure automation on the senhasegura platform - GO
Caution
Automation doesn't work when Offline mode is active.
Step (1/2) - Create the automation
Access the senhasegura platform.
Navigate to 
GO Endpoint Manager ➔ General ➔ Automation
.
Create one automation by clicking on the 
(
⁝) 
icon and 
New
.
Complete the 
Automation Register 
form:
Name
: the name of your automation.
Type
: determine which kind of automation - 
App Authentication
 or 
Web Authentication
.
Info
For 
Web Authentication
, senhasegura uses the default browser decided by the user. But only the 
Google Chrome
 and 
Mozilla Firefox
 browsers are supported. 
Microsoft Edge
 and 
Microsoft Internet Explorer
 are not supported.
Enabled
: define if this automation will be working or not.
View TAGs
: use the tags below to build your automation. Fill in the Value field.
[#USERNAME#]
: credential username.
[#PASSWORD#]
: credential password.
[#DOMAIN#]: 
credential domain.
[#HOSTNAME#]:
 hostname.
[#HOST_IP#]: 
hostname IP.
Application path
: the application path on the system. For example, for applications : C:\Program Files (x86)\Microsoft SQL Server\110\Tools\Binn\ManagementStudio\Ssms.exe, and %windir%\system32\mmc.exe, etc. For the Web: https://facebook.com, etc.
Tags
: define
 tags
 to help in the automation search.
Script
: already programmed sequence of actions of the automation. You can rearrange actions by clicking and dragging, changing the execution order.  Click on any action to edit its properties.
Actions
: you can automate
 Button
 clicks, navigate to the 
Menu
, and input text with 
Input
. When clicking on one of the options, it will be added as the last element in the 
Script
, and its properties can be edited.
Button: 
used when you want to click on the element that acts as a button. Its
 label
 property must be filled in with the visible text that defines it.
Menu: 
application menu path. Write the 
path
 property to automate. Separate levels with the '
;
' symbol. E.g.: 
Edit;Preferences;Font
 automates the path 
Edit ➔ Preferences ➔ Font.
Input:
 fill in the info for the application or website. Write the
 Label
 property with the name visible to the user, identifying the field. And write in the 
Value
 property the value to be inserted in the field of the application.
Property
: fill in the respective field name and, if necessary, its value. You can save or delete the added action.
Description
: briefly describe what this automation does and why it is used.
Save
.
Step (2/2) - Add to the access list
Access the senhasegura platform.
Navigate to 
GO Endpoint Manager ➔ Policies ➔ Windows ➔ Access List
.
In the actions menu, choose 
New general segregation
 or 
New segregation for workstations
.
Choose 
Automation
.
Complete the fields in the 
General list 
form.
Name
: define the name of the access list.
Status
: define if this list will be active or not.
Record session for these applications
: define whether recording sessions is allowed while the automation runs.
In the 
Automations
 tab, select the created automation. 
Check the checkbox and 
Add
.
In the 
Workflow
 tab, define the elevation of privileges settings. 
Save
.
Configure automation on the senhasegura platform - PAM/RemoteApp
Step (1/2) - Create the automation
Access the senhasegura platform.
Navigate to 
PAM Core
 ➔ Settings ➔ Access ➔ RemoteApp
.
Create the automation by clicking the 
(
⁝) 
icon and 
New
.
Complete the fields on the 
RemoteApp
 
form:
Name
: define the name of your automation.
Type
: choose the 
User Simulation
 option for GO Endpoint Manager for Windows automation.
Tags
: define tags to help you to search the automation by separating each tag with a comma.
Enabled
: define if this automation will be active or not.
Application path
: application path on the system. For example: C:\Program Files (x86)\Microsoft SQL Server\110\Tools\Binn\ManagementStudio\Ssms.exe.
Parameters:
 write the parameters in double-quotes. For example: "-S [hostname] -U [username] -P [password]".
Script
: contains the steps that you will add in 
Actions.
Actions:
 you can only add actions like 
Wait
, 
Key
, 
KeyPress
, 
KeyRelease
, 
Text
, and 
Type
.
Properties
: write the respective field name. If necessary, add the value. You can save or delete the added action.
Description
: briefly describe what this automation does and why it is used.
Save
.
Step (2/2) - Create credential to add RemoteApp
Go to the senhasegura platform.
Register the device where the automation will run.
Navigate to 
PAM Core
 ➔ Credentials ➔ All. 
Click the 
(
⁝)
 icon and 
New
.
Complete the fields in the 
Credential
 
form.
Username
: enter the username that will access the device.
Password type:
 select which type of user on the system 
Domain User, Local Administrator, 
or
 Local User.
Domain:
 fill in the domain of the device, if it has one.
Device:
 select the device where the automation will run.
Additional information:
  add other important information. For example, the name of the database.
Status
: define if it will be enabled or not.
Password:
 enter the password that will access the device.
Tags:
 define tags to help you to search for the credential.
Go to the 
Session Settings
 tab.
Click 
Automation Macro (RemoteApp)+
.
Add the automation you created.
Save
.
Execute automation
Access the user's desktop.
Start 
Automation
. 
Select the automation you want to run. 
Right-click on the automation and 
Run
. 
Choose which credential will be used by the script of the automation.
Wait for the automation to run.
Learn more
Synchronizing politics or credentials
Language settings