# Core 

It is the application with the most features and is already selected for installation by default. With Core, you can:
Run an application with or without privilege elevation.
Elevate an application of the list.
Manage Windows Control Panel.
Configure adapters and network sharing.
Access privileged folders.
Uninstall applications.
Perform Just-in-time (JIT) accesses.
Run administrative commands.
Perform Single Sign-On (SSO) in the senhasegura platform.
When opening the application, it displays the following image:
GO Endpoint Manager Core splash screen
 
On the left, you have the GO Endpoint Manager main menus.
In the top right corner:
the
 Access senhasegura server
 and 
Offline Mode
 icons.
the 
Just-in-Time (JIT)
 and 
GO Shell
 buttons.
Above the header are the 
filters
 and the 
search bar.
Next to the filter is the 
Refresh
 button.
Activate and deactivate modules
GO Endpoint Manager for Windows
 allows you to make modules active or not. To configure, follow the steps.
Access the senhasegura platform.
Navigate to 
GO Endpoint Manager ➔ Configurações ➔ Parâmetros ➔ go Windows.
In the 
Modules
 section, choose which module you want to make visible.
Check 
Yes
 or 
No 
for the options:
Enable applications?
Enable Control Panel?
Enable Network Sharing?
Enable Network Interface?
Enable Uninstall?
Enable credentials?
For the changes to take place, restart the application.
Caution
If the 
C
redentials 
are deactivated, accessing the Vault won't be possible. 
Synchronize politics or credentials
Policies and credentials synchronizations happen automatically every 15 minutes. However, it is possible to synchronize through the application. 
To do this, follow the steps:
Access the GO Endpoint Manager application 
(Core, Vault, or Automation)
.
In the Windows hidden icons menu, right-click the senhasegura icon.
Click one of the options: 
sync policies, sync credentials,
 or 
sync local groups
 to perform the sync.
Caution
Credential sync time may vary depending on the number of credentials synced.
Sync notifications
Info
When restarting an application, the synchronization of the politics and credentials is automatically performed.
Credentials synchronization
Start
Synchronizing credentials. This may take a few minutes if it is not possible to communicate with the server. Please wait.
End
Credentials synchronized successfully.
Policy synchronization
Start
Synchronizing policies. This may take a few minutes if it is not possible to communicate with the server. Please wait.
End
Policies synchronized successfully.
Local group sync
Start
Synchronizing local groups. This may take a few minutes if it is not possible to communicate with the server. Please wait.
End
Users and groups discovered successfully.
Info
The execution of the Synchronization of local groups respects the execution days and times configured in the GO Windows parameters. See how to configure in 
Configure verification of local privileged credentials
.
Language settings
After installing one application in the workstation, you can change its language:
Access a Go Endpoint Manager application (
Core
, 
Vault
, or 
Automation
).
In the Windows hidden icons menu, right-click on the senhasegura icon.
Select 
Change GO Endpoint Manager language
.
Choose the desired language.
Restart the application.