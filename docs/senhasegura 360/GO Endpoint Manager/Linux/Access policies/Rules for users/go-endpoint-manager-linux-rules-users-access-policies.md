# Register default access policies 

Caution
GO Endpoint Manager for Linux doesn’t grant permission to a directory or file to a user if the operating system doesn’t allow access.
Access the senhasegura platform.
Navigate to 
GO Endpoint Manager➔Policies➔Linux➔Access Policies.
Click 
⁝
 and select the option 
New rule
 for user.
At the
 Rules register by user
 
form, in the 
Main 
tab, complete the fields:
Policy name: 
define an easy-to-identify name. 
Enabled:
 if enabled, the policy will be applied across devices.
Guideline: 
select a policy type.
Caution
If the user already has the command embedded in the shell itself, GO Endpoint Manager for Linux won’t search to execute the system command. In this way, the command embedded in the shell won’t be filtered by the policy. To check the built-in shell commands in the Linux terminal, type the 
help
 command.
Checker (path or executor): 
fill in the directory path (e.g.: path="/usr/bin/ls") or the executor for symlinks (e.g.: exec="/etc/alternatives/vim"). To get the path, type the command 
which [the command you want]
, and to validate if it is a symbolic link, type the command 
ls -la [the command path you want]
.
Important
Failure to complete or incorrectly complete this field can lead to the complete unusability of the device. Follow 
CaitSith's syntax
 to fill in correctly.
Enable audit?: 
the field is required and enabled by default. It allows auditing of actions performed. 
Include general denial rule?:
 if this option is checked, no Linux workstation user will be able to execute something not allowed by the access policy. If unchecked, all Linux workstation users will be allowed to run everything except what the rule blocks.
Allow or block:
 choose whether the registered policy allows or denies access to the user or group.
Rule text: 
fill in a rule in the format of the
 CaitSith
policies. For example, for users: task.uid="user". For groups: task.gid=”group”. It must be the user's primary group.
Caution
The first rule added takes precedence over rules entered later. If you create a rule that allows the binary to run and then add another rule to block the same binary from running, the first rule will be considered, and the second not.
Click 
Add.
Go to the 
Users
 
tab.
Select 
Users
+.
Choose the users you want to add to the segregation.
Click 
Add.
Click 
Save.
Info
All commands that go through a filtering process will be logged. This includes defined rules to allow running on 
CaithSith
 access policies or rules for sudo. You can change the general rule of a policy to include more rules, such as controlling directories and files, by clicking the 
Change user rule
 icon in the 
Action
 column of an existing policy. The 
(⁝) Display rule
 icon allows you to check the formatted policy.
Caution
Avoid reusing existing policies; prefer creating new policies. Constantly editing current policies can cause errors in the policy you’re creating.
Policies added to the device
To validate that the policy has been added to the device:
Access the Linux terminal.
Enter the command:
cat /sys/kernel/security/caitsith/policy