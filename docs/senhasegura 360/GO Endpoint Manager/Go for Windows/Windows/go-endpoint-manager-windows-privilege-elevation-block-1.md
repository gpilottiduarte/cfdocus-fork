# Privilege elevation block 

When the 
Block elevation of privilege
 parameter is enabled, any attempt to run an application on the access list and not performed by GO Endpoint Manager will be blocked. Even if they are not elevated of privilege.
Configure the privilege elevation block
Access the senhasegura platform.
Navigate to 
GO Endpoint Manager ➔ 
Settings ➔ 
Parameters ➔ 
go Windows.
At 
B
lock elevation of privilege?, 
choose 
Yes
.
Privilege lock parameter
 
Caution
If the 
Block user
 option is set to
 Yes
, the user who tries to elevate an application exceeding the defined number of 
Occurrences 
will be blocked and unable to access the senhasegura platform. This process generates and sends blocking events to the senhasegura platform.
View events blocked
Access the senhasegura platform.
Navigate to 
GO Endpoint Manager ➔ Reports
 ➔ Windows
 ➔ Events
.
Choose the option 
Elevation of Privilege blocked
 at 
Event
.
Filter
.