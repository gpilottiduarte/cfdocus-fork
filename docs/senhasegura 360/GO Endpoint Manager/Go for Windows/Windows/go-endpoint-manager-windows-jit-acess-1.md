# JIT Access 

Just-in-Time (JIT) 
access allows users to elevate privileges as system administrators. So when JIT is active, the user will appear in the Administrators group.
Configure JIT access
Access the senhasegura platform.
Go to the menu 
GO Endpoint Manager ➔ Settings ➔ Parameters ➔ go Windows
.
In the 
JIT/Elevation methods
 section, check 
Enable JIT access? 
as 
Yes
.
Set 
Block elevation of privilege
 to 
No
.
Enable JIT access
Access the workstation desktop of the user.
Start Core.
Enable JIT by clicking the 
Just-In-Time
 button.
Activate JIT access
 
Info
Configure the application to record to visualize what happened during the JIT access. In 
Recording reports
, the recording will be available. It may take 10 to 20 minutes after the end of the session to view the recording on the senhasegura platform.
Disable JIT access
Access the workstation desktop of the user.
Start Core.
Turn off JIT by clicking the
 Just-In-Time
 button.
Disable JIT access
 
Important
When JIT is disabled:
The user will be logged out.
The user will be removed from the Administrator's group.
The machine will restart.
Manage system administrators
To confirm that the user has been added or removed from the 
System Administrators
 group, follow the steps:
Access the workstation desktop of the user.
Go to 
Computer Management ➔ Local Group Users ➔ Groups ➔ Administrators.
View if the user is part of the admin user group.