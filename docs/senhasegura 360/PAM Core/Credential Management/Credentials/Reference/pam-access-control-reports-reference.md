## Metadata_Start 
## code: en
## title: Reference for access control reports 
## slug: pam-access-control-reports-reference 
## seoTitle: Access control reports reference 
## description:  
## contentType: Markdown 
## Metadata_End
Controlling access to a security system is necessary to prevent unauthorized access to privileged credentials, assets, and other sensitive information stored on the system.

The  section allows you to print log reports of user and group activities performed through senhasegura. These logs include information such as the date of the action, credentials, user access, and more.

To access these reports, navigate to the  >  menu, where you will find the reports below.

## Access control report

This report shows the access control history of the activities made by each system user and the approval requirements when needed. This report is essential to understand if the privileges of each user are still in compliance with the access flow set by the company's policy. Also, it informs if the users need approval or not to execute activities.

The  report will print the following information:

* : identification code for the operation.
* : day and time the change was performed.
* : operation performed by the user.
* : the name of the user that will be detailed.
* : IP of the device the user operated.
* : credential of the password that was accessed.
* : device that was accessed.
* : username that was accessed.
* : justification type.
* : code used to track the access in senhasegura.
* : justification text the user.
* : justification message given by the user.
* : this option appears when there is an approval workflow configured for the credential.
* : the platform used to access.

It's also possible to see more details about the access by clicking on the action icon of the register.

## Access group changes report

This report shows the access logs from the access group perspective with logs of the group modifications made by each system user, such as group creation, user removal, and more.

The  report will print the following information:

- : the date on which the group was modified.
- : the operation that the user performed on the group.
- : the name of the user that performed the modification.
- : the group that was modified.
- : the name of the user that admitted the modification.
- : the system prints after the change.

## Session events

This report shows a list of events that occurred during a session. This information is important for tracking and auditing the actions in each session.

The  report will list the following information for each session:

- : identifier code for the record.
- : identifier code for the session.
- : date and time of the event that occurred.
- : event that occurred.
- : note about the event.
- : IP from which the action originated.
- : type of protocol used for connection.
- : IP of the session host.
- : username of the user that performed the action.
-  informs the session's start time with the credential indicated.
-  informs the end of the session with the credential indicated.

## Users by group report

This report shows the list of users associated with each access group in the system. This information is important to ensure users are assigned to the correct access groups according to their job functions and responsibilities.

The  report will print the following information:

-  the name of the access group.
-  the name of the user associated with the access group.
-  the type of credential associated with the user.
- : refers to the access group name linked to a user. Access groups determine which users can access specific resources or privileges in the system.
- : refers to the type of credential used for user authentication and system access.
- : the date on which the user was assigned to the access group.
- : the name of the person who assigned the user to the group.

This report helps to ensure that the correct permissions are assigned to each user and that access to sensitive information is limited to only those who need it.

## Approvers by group

This report lists all users assigned as approvers in the system, enhancing the tracking of those involved in the approval process.

The  report will print the following information:

- : the name of the user assigned as an approver in the system.
- : the selected username for use in the system, pending approval.
- : the group of users to which the assigned user belongs.
- : the group that has access to the approval process.
- : the type of approver assigned, such as primary or secondary.
- : the date the user requested approval.
- : the name of the user who assigned the approver.

## Next
1. .
2. .