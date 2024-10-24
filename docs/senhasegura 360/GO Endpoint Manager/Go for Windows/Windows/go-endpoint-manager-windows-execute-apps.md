# Execute 

This feature allows the user to run applications with or without privilege elevation.
GO Endpoint Manager Core - Execute
 
Info
The 
Core
 application is customizable. The image displayed and the description of items may change according to the version of the user and the features allowed by the administrator.
Applications list
Not all applications may be listed. 
Refresh
 to search for new applications. 
If an application is not on the list, you can drag its shortcut or runtime binary into it.
EXE, LNK, MSC, and MSI files
 
are accepted. 
Execute an application inside of Go
Access the user's desktop.
Start 
Core
.
Click on the menu 
Execute
.
Choose an available application in the list.
Right-click on it and choose one of the options:
Execute
: run the application in a dedicated session.
Execute as a user
: you must choose a credential to run the application. Read the 
Impersonation
 article to learn more.
Info
For users in access groups that require approval, the application will only be allowed after the approval.
Execute an application outside of GO
Search for the application you intend to run.
Right-click on the application icon. 
E
xecute with senhasegura.go
 
In this case, the elevation outside of GO is 
Executed with privileges
. This application will run with all administrative privileges.
Executing an application outside senhasegura GO
  
Caution
Validate that there are no GPOs applied or not applied on the Workstation that could prevent the GO Endpoint Manager Windows client from working correctly.