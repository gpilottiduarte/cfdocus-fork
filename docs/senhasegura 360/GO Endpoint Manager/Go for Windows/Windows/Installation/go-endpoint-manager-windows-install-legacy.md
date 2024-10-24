# How to Install the Go Windows Legacy Agent 

In this article, you’ll learn how to install GO Endpoint Manager for Windows Legacy on your Workstation.
Requirements
Dependencies and Windows versions are described in the 
Requirements
 article
.
Administrative permission on the user's workstation.
A registered user on the senhasegura platform with the same username as the workstation.
Info
If you don't know the workstation username, open CMD and run 
whoami
.
If necessary, see the 
Add user
 article.
The minimum access profile for the user must be
 viewing passwords.
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
Step 1: Get the installer
Access the 
PAM Solution portal
.
Log in to the website.
Find the version of the GO Windows agent that is compatible with your version of the senhasegura platform.
In the column 
Link
, click 
Download
 to download the installer of 
GO Endpoint Manager for Windows.
Info
The language of the downloaded version is as per the language selected, in PAM Solutions.
Step 2: Install the agent
Access the 
File explorer
 and click on the folder 
Download
. Depending on the location configured to save the downloads, your folder may have a different name.
Extract the obtained installer files.
Open the folder and click on the Windows Installer package.
Click 
Next.
Read the 
End User License Agreement ("EULA")
 carefully. After reading, if you agree, select 
"I accept the terms of the License Agreement",
 and click on 
Next.
In the window that requests approval, select Yes to proceed with the installation.
Click
 Save.
Step 3: Ensure communication
Important
During licensing, confirm the existence of communication between the senhasegura platform and the GO Windows Agent. Before activating GO Windows, enter the URL registered on the platform (IP or DNS) in a browser and check if it opens.
Caution
If you have a balancer, you must ensure the DNS resolves to the correct IP.
On the senhasegura platform, in the upper left corner, click the 
Grid Menu
, identified by the nine squares, and select 
Orbit Config Manager.
On the side menu, select 
Settings ➔ Application.
Verify if the URL provided in the field 
Application URL
 corresponds to a URL that can be accessed by all Workstations that will run the GO Endpoint Manager for Windows.
 If necessary, change the address and confirm with the button 
Save
 in the footer.
Important
You must fill in the 
Application
 
URL 
field with the 
HTTPS
 protection layer. Otherwise, the server will be unavailable.
Step 4: Generate a use license
On the senhasegura platform, in the upper left corner, click the 
Grid Menu
, identified by the nine squares, and select 
GO Endpoint Manager.
On the side menu, select 
Settings ➔ Installers.
On the right footer, click on
 Installation Key.
In the 
Client 
field, select 
PEDM Windows.
Copy the text of the generated use license in the field below.
You can select it to download the license by clicking 
Download.
Info
You can use the license file if you perform a batch installation via Microsoft Active Directory.
Step 5: Activate the application
Access the workstation desktop.
Click on the GO Windows application.
Paste the license key you got in the previous step.
Click 
OK. 
Step 6: Configure approvals
Messages may appear during the installation process, depending on previous configurations on the senhasegura platform or how the workstation is shared. These messages indicate that workstation or user approval is required.
Info
These messages are not errors and are part of the installation process. The most common message is 1002.
To complete the installation, follow the steps below, if necessary:
How to authorize or revoke a user.
How to authorize or inactivate a workstation.
Approve user and workstation automatically
User and workstation approvals can be automated to avoid excessive interactions between the person installing the system on the workstation and the administrator who must approve registrations on the senhasegura platform.
By default, GO Endpoint Manager for Windows doesn’t come with auto-approval enabled, leaving this decision up to the administrator.
Caution
If automatic approval is enabled, any machine and user that is on the corporate network with a valid license is allowed to operate GO Endpoint Manager for Windows, without the need for administrator approval.
On the senhasegura platform, in the upper left corner, click the 
Grid Menu
, identified by the nine squares, and select 
GO Endpoint Manager.
On the side menu, select 
Settings ➔ Parameters ➔ go Windows.
Change the following parameters to 
Yes
:
Allow self-approval of the workstation links?
Allow self-approval of all other links?
Allow self-approval of the user's first link?
Confirm the changes and 
Save
.
Next steps
Workstation report.
User report.
Access list.
Do you still have questions? Reach out to the 
senhasegura Community.