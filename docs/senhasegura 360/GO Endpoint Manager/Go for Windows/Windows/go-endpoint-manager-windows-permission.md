# Permission 

Overview
To manage situations where it is necessary to manage permissions for applications, users, and workstations, GO Endpoint Manager for Windows offers denylists and allowlists.
Often, the administrator does not want to allow some applications (e.g., Microsoft Powershell or Windows Command Line) for all users. In these cases, you can:
Create global deny list rules.
Create segregation access list rules by workstation
Allow only certain users to have access to chosen applications.
Create access lists for 
applications
, 
automation
, and 
uninstallers.
Info
It's possible to separate the submodules records of 
application, automation, uninstaller, control panel
, and 
DLL 
using deny and allow lists. Furthermore, it's possible to segregate these records using global levels and by workstations.
Priority flow in an access list
Priority order:
Allowlist (elevating possibility)
Allowlist (no elevating)
Denylist
Segregated parameter (elevating possibility)
Segregated parameter (no elevating)
Global parameter (elevating possibility)
Global parameter (no elevating)
Important
This priority flow works differently from the PAM Core module, where the denylists are more restrictive than the allowlists. In GO Endpoint Manager for Windows, allowlists override denylists.
Allowlist (override the other rules): 
it allows the application of rules created for specific programs. Any item not included in the rule is handled through segregated parameters, if any. The execution of an application on the allowlist can be restricted through the access workflow. It's possible to define restrictions that require justification and approval to access the application.
Denylist: 
it denies all applications that are part of the rule and allows everything outside it.
Segregated parameters:
 these parameters override the general system parameter.
Parameters: 
these parameters are applied to all workstations. They are not applicable if there is a denylist or allowlist access list.
Info
The administrator must register an Approving user in the system if approval is necessary.
Read more
Typical screen
Automation
Approval workflow