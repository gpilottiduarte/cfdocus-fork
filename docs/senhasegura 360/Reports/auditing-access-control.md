## Metadata_Start 
## code: en
## title: Access control reports 
## slug: auditing-access-control 
## seoTitle: Access control report 
## description:  
## contentType: Markdown 
## Metadata_End
Controlling access to a security system is necessary to prevent unauthorized access to privileged credentials, assets, and other sensitive information stored on the system.

The "Reports" section allows you to print log reports of user and group activities performed through senhasegura. These logs include information such as the date of the action, credentials and user access, and more.

To access these reports, navigate to the "Reports ➔ Access Control" menu, where you will find the following reports:

## 

This report shows the access control history of the activities made by each system user and the approvals requirements when needed. This report is essential to understand if the privileges of each user are still in compliance with the access flow set by the company's * Also, it informs if the users need approval or not to execute activities.

The  report will print the following information:

- * day and time the change was performed;
- * performed by the user;
- * is the name of the user that will be detailed;
- * of device the user operated;
- * of the password which was accessed ;
- * that was accessed;
- * that was accessed;
- * is the type of justification the user gives to access the credential;
- * it is the code used to track the access in senhasegura ;
- * is the justification text the user gives to perform the view;
- * is what the system prints to the requester related to the permissions and more;
- * indicate the platform used to access;

It's also possible to see more details about the access by clicking on the action icon of the register.

## 

This report shows the access logs from the access group perspective with logs of the group modifications made by each system user, such as group creation, user removal, and more.

The  report will print the following information:

- * the group was modified;
- * the user performed on the group;
- * is the name of the user that performed the modification;
- * that was modified;
- * is the name of the user that admitted the modification;
- * is what the system print after the modification;

## Users by group

This report shows the list of users associated with each access group in the system. This information is important to ensure that users are assigned to the correct access groups according to their job functions and responsibilities.

The  report will print the following information:

- * the name of the access group.
- * the name of the user associated with the access group.
- * the type of credential associated with the user.
- : This refers to the access group name linked to a user. Access groups determine which users can access specific resources or privileges in the system.
- : Refers to the type of credential used for user authentication and system access.
- : This is the date on which the user was assigned to the access group.
- : This is the name of the person who assigned the user to the group.

This report helps to ensure that the correct permissions are assigned to each user and that access to sensitive information is limited to only those who need it.


## Approvers by group

This report lists all users assigned as approvers in the system, making it easier to track those involved in the approval process.

The * report will print the following information:

- : the name of the user assigned as an approver in the system.
- : the selected username to be used in the system, pending approval.
- : the group of users to which the assigned user belongs.
- : the group that has access to the approval process.
- : the type of approver assigned, such as primary or secondary.
- : the date the user requested approval.
- : the name of the user who assigned the approver.
