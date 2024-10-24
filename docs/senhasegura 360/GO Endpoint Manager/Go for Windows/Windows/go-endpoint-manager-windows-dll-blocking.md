# DLL blocking 

GO Endpoint Manager for Windows offers a DLL blocking function, which occurs when an executable attempts to load the process.
Feature availability
✖3.26 and older versions        ✔3.27 and later versions
Register an untrusted DLL
Important
Use DLL blocking with caution. If a system DLL is blocked, system operation may be affected.
Access the senhasegura platform.
Navigate to 
GO Endpoint Manager ➔ Policies ➔ Windows ➔ Access Lists
.
Click on the 
Actions
 menu.
Choose the option 
New general segregation
 or 
New segregation for workstation
.
Choose the 
Applications
 category.
Fill in the following information on the 
General List 
screen:
Name
: define a name to identify the access list.
Action
: choose Denylist to block a DLL.
Allowlist restrictions
Make sure this DLL is not included in any Access List assigned as an Allowlist. The Allowlist is more restrictive, therefore, if this DLL is included in another list as an Allowlist, its execution will be allowed even if it is included in a Denylist.
Status
: set to Enabled or Disabled.
Record session for these applications
: set to Enabled or Disabled.
On the tab 
Applications:
For 
Criteria 
and 
Rule, 
choose:
Critério
Regra
Directory
The location of the .dll file.
File Hash
Enter the Hash of the file.
Click 
Add
After adding the criteria and rule, click 
Save
.