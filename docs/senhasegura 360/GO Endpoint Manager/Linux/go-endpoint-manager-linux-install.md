# Agent installation 

Requirements
Linux dependencies and versions are listed on the page 
Getting started.
Administrative permission on the user's workstation.
Users must have a user with the same username on the senhasegura platform.
When installing GO Endpoint Manager for Linux, it is necessary to restart the machine.
Info
✔ If necessary, see the article 
Add a user.
Install
After you meet all the requirements, you can start the installation.
Shell
Step (1/7) - Get the installer
Go to the 
PAM Solution portal.
Select the agent version that is compatible with your version of the senhasegura platform.
Download the agent that is compatible with your operating system.
Caution
If you want to use the solution on another unavailable Linux-based operating system, please contact the support team to receive system-specific instructions.
Step (2/7) - Validate the URL
Access the senhasegura platform.
Go to
 Orbit Config Manager➔Settings➔Application.
Fill in the application URL field with the URL of the senhasegura server. 
Example:
 https://senhasegura.mycompany
Step (3/7) - Start the installation
Log in to your Linux machine.
Run the following command to install GO Endpoint Manager for Linux.
Shell
Shell
root@debian: sudo /bin/bash secpack-installer-3.28.0-0_distro.run

$ Verifying archive integrity... 100% MD5 checksums are 0K. All good. 

$ Uncompressing senhasegura security package 100% 

$ Verifying archive integrity... 100% MD5 checksums are 0K. All good. 

$ Uncompressing caitsith-installer 100% 

$ Uninstalling previous version of kernel module... 0K 

$ Building and installing kernel module.. .OK 

$ Installing caitsith—tools... 0K $ Installing debian packages... 

$ Packages installed successfully! 

$ senhasegura security pack v3.28.0—5 

$ Enter the license code:
Copy
Step (4/7) - Generate an installation key
Access the senhasegura platform.
Go to 
GO Endpoint Manager➔Settings➔Installers.
Click the blue footer button 
Installation Key.
In the Client field, select 
PEDM Linux.
Copy the text from the generated user license into the
 Installation Key 
field.
You can choose to download the license by clicking
 Download.
Step (5/7) - Activate GO Endpoint Manager
Log in to your Linux machine.
After the Start installation step.
Enter the copied key when 
"Enter license code:" 
is displayed.
Click 
Enter.
After entering the key, you should see this message
 "Installation complete!".
Step (6/7) - Approve a workstation for installation
Access the senhasegura platform.
Go to 
GO Endpoint Manager➔General➔Workstations.
Find the workstation you install the agent.
Go to the action column 
⁝
Click the 
Authorize option.
Type the following command in Linux. You should see this message:
Shell
Shell
root@debian: sudo secpack-register
senhasegura security pack v3.28.0-0
Workstation already registered!
Copy
Step (7/7) - Approve the user for installation
Access the senhasegura platform.
Go to 
GO Endpoint Manager➔General➔Users.
Find the user related to a workstation where the agent is installed.
Go to the action column 
⁝
Click on the 
Authorize option.
Click Yes to authorize.
You can define an 
Expiration Date
 on the 
Authorize Local User Usage
 screen. (not mandatory field)
Click 
Save.
Related articles
Learn more about GO Endpoint Manager for Linux:
Introduction
Getting started
New rule
Troubleshooting
If you encounter any issues, you can try the following articles:
Failure in the implementation of access policies
.
Error messages when recording sessions
.
Still not able to find your answer? Send your question to our
 senhasegura Community.