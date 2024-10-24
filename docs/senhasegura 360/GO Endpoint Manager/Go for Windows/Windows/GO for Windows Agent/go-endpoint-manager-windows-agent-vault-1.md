# Vault 

The application enables the cache of credentials, viewing, and copying of credentials. These actions are equivalent to using a proxy, preview, or copy through the web interface. All these actions will be audited and forwarded via SIEM.
When opening the application, it displays the following image:
Vault initial screen
 
In the top left corner is the search bar.
In the top right corner is the 
Refresh
 button.
Below the Search bar, you have the titles:
User:
 the default credential for privilege elevation actions inside and outside the 
Vault
.
Domain:
 the name of the domain of the device.
Device:
 the device associated with the credential.
If the default credential has no domain registered, the machine name will be displayed instead.
Use a credential
Vault
 users are always linked to their accounts used to log into Windows.
Caution
The workstation username must have an equivalent user in the senhasegura platform. If you are not sure about the username, read the article 
Requirements
.
Access the user's desktop.
Start 
Vault
.
Select the credential you want to use from the list of credentials.
Right-click on the automation.
Click 
Copy
 or 
Show
 to access the password.
Use a credential in case of unavailability
In cases of unavailability of the senhasegura platform. The Vault stores the user and password credentials locally. It is encrypted and keeps the information from the last update. So the user can view and copy the credentials and password.
Access the senhasegura platform.
Go to 
GO Endpoint Manager➔Settings➔Parameters➔go Windows.
In modules, activate the option 
“Enable credentials?”.
Click on 
Save.
Access the user's workstation, and follow the steps to 
use a credential
. 
Caution
This feature does not work in conjunction with offline mode.
Configure Token requests to view or copy credential
Access the senhasegura platform.
Configure MFA OTP token.
Go to 
GO Endpoint Manager➔Settings➔Parameters➔Security.
Check the option 
Force Multi-Factor Authentication to view password?*
 or 
Force Multi-Factor Authentication to login?*
 to 
Yes.
The user will be prompted to fill in a token to copy or view the credential.
Configure verification of local privileged credentials
Access the senhasegura platform.
Access the menu 
GO Endpoint Manager➞Settings➞Parameters➞go Windows.
Go to the 
Report
 section.
Check the option 
Enable local privileged credentials checking?.
Set days and times for execution.
Click 
Save.
Learn more
Synchronizing politics or credentials
Language settings