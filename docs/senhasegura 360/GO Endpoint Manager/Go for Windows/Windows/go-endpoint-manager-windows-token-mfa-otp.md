# Token MFA OTP 

Overview
If the setting 
Enable multifactor authentication on login
 is enabled in the parameters screen, and the linked user has an MFA token configured in senhasegura, that user either logs into the workstation or accesses the workstation via RDP connection, the application will request the MFA token.
Caution
The time of the senhasegura server and the workstation must be synchronized.
How to enable the token MFA
Go to the senhasegura platform.
Access 
GO Endpoint Manager ➔ Settings ➔ Parameters ➔ go Windows.
Go to the 
Authentication 
section.
Check the 
Enable multifactor authentication on login
 as 
Yes.
Enable the 
token MFA
 for your user.
Configure token MFA OTP
Go to the 
senhasegura 
platform.
Click on your username.
Configure MFA
 
Click on 
Configure MFA.
Select 
Yes.
Choose the 
OTP 
option.
Open your authenticator application.
Add a new account by scanning the 
QR code
 on the screen.
Click on 
click here
 to validate it on the same screen.
Type the 
MFA token
 of your authenticator application
Click on 
Validate.
Use token on workstation login
Start the workstation.
Fill in your 
username
.
Fill in the 
Token
 generated in your authenticator application.
Click 
Sign in
.
Info
When 
Enable multifactor authentication at login?
 
is enabled, your user photo is changed at the login screen. 
Windows user login using Token