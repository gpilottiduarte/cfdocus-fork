# Register alias policies 

When creating a 
New rule
, the 
Alias
 tab allows the creation of aliases (alternative names for commands) through GO Endpoint Manager for Linux. You can create shortcuts to manage the most used commands, streamlining the use of the terminal.
Access the senhasegura platform.
Navigate to 
GO Endpoint Manager➔Policies➔Linux➔Access Policies.
Click
 ⁝
 and select the option 
New rule
 to create a general policy.
At the 
Access policy register
 form, in the 
Main 
tab, complete the fields:
Policy name:
 define an easy-to-identify name. 
Enabled:
 if enabled, the policy will be applied across devices.
Guideline: 
select a policy type.
Allow or block: 
set to 
Allow.
Rule text: 
fill with handler="/usr/bin/secpack-trec-triggered"
Click
 Add
.
Go to the
 Alias 
tab.
Caution
Be careful when filling out the alias for commands that may affect the use of the system.
Complete the fields:
Alias: 
fill in the full path of the command you want to use.
Command: 
fill in the full path of the command you want to replace.
Click 
Save.
Info
In the Linux terminal, use
 which [the command you want]
 to find out the path of the binary.
Check created aliases
Access the Linux terminal.
Enter the command:
cat /etc/senhasegura/aliases