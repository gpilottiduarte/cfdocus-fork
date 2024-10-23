# How to authenticate with Duo 

This tutorial presents a guide on how to integrate senhasegura and Duo. You can use Duo's multi-factor authentication to log in or start sessions on senhasegura.
Step 1: Create an application in Duo
Requirements
Duo Security Account
To create an application, follow these steps:
Log in to the Duo Admin Panel.
On the left sidebar, select 
Applications
.
Click 
Protect an Application
.
In the search bar, type 
Web SDK
.
On the right, click 
Protect
 to configure the application.
Copy the 
Client ID
, 
Client Secret
, and 
API hostname
. You'll need this information to complete the configuration.
On the left sidebar, select 
Settings
.
Enter the 
Name
 of the application.
Click 
Save
.
Step 2: Enable External MFA Solution
To enable MFA, follow these steps:
In the top-left corner of the senhasegura platform, click 
Grid Menu ⁝⁝⁝
, indicated by the box of nine squares, and select 
Settings
.
On the left menu, select 
System Parameters ➔ Security
.
In the 
Multi-factor authentication
 section, check 
Enable external Multi-Factor Authentication application
.
Caution
Enabling this function will deactivate some security mechanisms. The SameSite property will change from "Strict" to "Lax."
Ensure you have configured a firewall to deny unauthorized site access to your senhasegura server.
Close the warning message.
Click 
Save
. 
Step 3: Configure Duo MFA in senhasegura
Requirements
Authentication data from Duo API
To configure Duo in senhasegura, follow these steps:
In the top-left corner of the senhasegura platform, click 
Grid Menu ⁝⁝⁝
, indicated by the box of nine squares, and select 
Settings
. 
On the left menu, select 
Authentication ➔ Multi-factor authentication ➔ Providers
. 
In the top-right corner, click 
V
iew actions
, the icon represented by three vertical dots (⁝).
Select 
New
.
Choose 
Duo Security
.
In the 
Name
 field, set the provider's name.
Keep 
Enabled
 as 
Yes
.
In the 
Endpoint
 field, fill in the value of the Duo API hostname.
In the 
Client ID
 field, fill in the value of the Duo client ID.
In the 
Client Secret
 field, fill in the value of the Duo client secret.
Click 
Save
.
Step 4: Configure Duo as the User's MFA
Requirements
A direct network connection between senhasegura and Duo Security. Proxies are not supported. 
Duo mobile app
DNS configuration
Caution
senhasegura must have DNS configured and a valid certificate to establish connectivity with the DUO endpoint. The 
URL Application
 field should also have the instance's DNS in the 
Orbit
 configuration.
To configure Duo as MFA, follow these steps:
Log in to your Duo application.
Select 
Duo Mobile
 as the authentication method.
Choose your country from the dropdown list.
Enter your mobile number.
Click 
Add phone number
.
Click 
Yes, it's correct
 to confirm your phone number.
Click 
Next
.
Open the Duo Mobile app on your phone.
Add the account by scanning the QR code on the screen.
Once you receive confirmation that Duo Mobile has been added, click 
Continue
.
To finish, click 
Log in with Duo
.
When accessing senhasegura, you will receive a push notification on your Duo Mobile app to complete the authentication.
Do you still have questions? Reach out to the 
senhasegura Community
.