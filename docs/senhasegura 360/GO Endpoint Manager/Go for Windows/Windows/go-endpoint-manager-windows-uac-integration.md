# UAC integration 

GO Endpoint Manager integrates with UAC authentication in cases where an application needs to elevate the privilege on demand. In these cases, besides the Windows authentication options, the GO Endpoint Manager logo will be displayed.
You must type select which credential from senhasegura you want to use to perform the elevation. If the user has an MFA token configured, he must also enter the token in a second step.
Being fully integrated into Windows, the entire process is clear to the user.
Configure UAC integration
Access the senhasegura platform.
Register the User Token.
Access 
GO Endpoint Manager ➔
Settings ➔
Parameters ➔ go Windows.
Check 
Enable 
UAC 
integration?
 as
 Yes
.
Caution
The elevation process through UAC is not registered in the senhasegura events.
Use a credential through UAC
Start the application that requires administrative privileges on the user's workstation.
At the user selection window, choose senhasegura.
Run as a different user
 
 3. Enter the name of the senhasegura credential you want to use to perform the elevation.
 4. Click
 Yes 
to confirm
 5. If multi-factor authentication is enabled, enter the token in a second step.