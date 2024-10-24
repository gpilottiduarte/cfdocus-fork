# How to install the Go Windows agent 

In this article, you’ll learn how to install the GO Endpoint Manager for Windows on your Workstation.
Requirements
Dependencies and Windows versions are described in the article 
Requirements.
Administrative permission on the user's Workstation.
A user registered on the senhasegura platform with the same username as the workstation.
Info
If you don't know the workstation username, open CMD and run 
whoami
.
If necessary, see the article on 
How to create a user
.
The minimum access profile for the user must be 
password view.
Step-by-step instructions
Get the installer.
Install the agent.
Ensure communication.
Generate a license to use.
Activate the application.
Configure Approvals.
Your title goes here
Alternatively, you can install 
GO Endpoint Manager for Windows
 with the 
CMD Installation
.
Step 1: Get the Installer
Caution
After updating the senhasegura platform, it is mandatory to update the GO Endpoint Manager for Windows to ensure that both are in the same version.
Access 
PAM Solution portal
.
Log in to the website.
Find the version of the GO Windows agent that is compatible with your version of the senhasegura platform.
In the column of 
Link
, click in 
Download
 to download the installer of 
GO Endpoint Manager para Windows.
Step 2: Install the agent
Go to the user's desktop.
Access the 
File explorer
 and click on the folder 
Download
. Depending on the location configured to save the downloads, your folder may have a different name.
Extract the obtained installer files.
Open the folder and click on the Windows Installer package.
Select installer language (not available on legacy):
Portuguese.
English.
Click in 
OK.
Click 
Next
 to continue.
 Read the 
End User License Agreement ("EULA")
 carefully. After reading, if you agree, select the checkbox 
"I accept the terms of the License Agreement", 
and click on 
Next.
 Choose the type of installation:
Customized: 
check which features you want to install. The Core option is already checked by default.
Core:
 it's composed by 
Execute (Elevation of Privilege)
, 
Control Panel
, 
Network Adapters
, 
Network Sharing
, and 
Uninstall
.
Automation:
 is a feature that allows GO Endpoint Manager for Windows to perform automations, being possible to perform authentication on installed applications or web pages accessed directly from the workstation. This automation can use the values of a system credential to which the user has access or fixed values defined in the configuration. And permit to run RemoteApp automations associated with credentials available to the user.
Vault:
 is responsible for enabling the cache of credentials, for viewing and copying the credentials.
Complete:
 this option installs the features 
Core
, 
Automation
, and 
Vault.
Caution
This option is available in the 3.27 and higher versions.
Click 
Next.
In the window that requests approval, select Yes to proceed with the installation.
Click in 
Save.
Step 3: Ensure communication
Important
During licensing, confirm the existence of communication of the senhasegura platform and the GO Windows Agent. Before activating GO Windows, enter the URL registered on the platform (IP or DNS) in a browser and check if it opens.
Caution
If you have a balancer, you need to ensure that the DNS resolves to the correct IP.
On the senhasegura platform, in the upper left corner, click the 
Grid Menu
, identified by the nine squares, and select 
Orbit Config Manager. 
On the side menu, select 
Settings ➔ Application.
Verify if the URL provided in the field 
Application URL
 corresponds to a URL that is accessible to all Workstations that will run GO Endpoint Manager for Windows.
 If necessary, change the address and confirm with the button 
Save
 in the footer.
Important
It’s mandatory that the field 
Application URL
 is filled with the protective layer 
HTTPS
, otherwise, the server will be unavailable.
Step 4: Generate a use license
On the senhasegura platform, in the upper left corner, click the 
Grid Menu
, identified by the nine squares, and select 
GO Endpoint Manager.
On the side menu, select 
Settings ➔ Installers.
On the right footer, click on 
Installation Key.
In field 
Clien
t
, select 
PEDM Windows.
Copy the text of the generated use license in the field below.
You can choose to download the license by clicking 
Download.
Info
The license file can be used if you perform a batch installation via Microsoft Active Directory.
Step 5: Activate the application
Access the workstation desktop.
Click on the GO Windows application.
Paste the license key you got in the previous step.
Click 
OK.
Step 6: Configure approvals
Depending on previous configurations on the senhasegura platform or on how the workstation is shared, it’s possible that messages will appear during the installation process. These messages indicate that workstation or user approval is required.
Info
These messages aren’t errors, they’re part of the installation process. The most common message is 1002.
To complete the installation, follow the steps below if necessary:
How to authorize or revoke a user.
How to authorize or inactivate a workstation.
Approve user and workstation automatically
User and workstation approvals can be automated to avoid excessive interactions between the person installing the application and the administrator who must approve registrations on the senhasegura platform.
By default, GO Endpoint Manager for Windows doesn’t come with auto-approval enabled, leaving this decision up to the administrator.
Caution
If automatic approval is enabled, any machine and user on the corporate network with a valid license can operate GO Endpoint Manager for Windows without administrator approval.
To configure automatic approval, follow these steps:
On the senhasegura platform, in the upper left corner, click the 
Grid Menu
, identified by the nine squares, and select 
GO Endpoint Manager.
On the side menu, select 
Settings ➔ Parameters ➔ go Windows.
Change the following parameters to 
Yes:
Allow workstation links auto-approval?
Allow auto-approval of all other links?
Allow user first link self-approval?
Confirm the change and click 
Save.
Next steps
Troubleshooting.
Workstation report.
User report.
Access list.
Do you still have questions? Reach out to the 
senhasegura Community.