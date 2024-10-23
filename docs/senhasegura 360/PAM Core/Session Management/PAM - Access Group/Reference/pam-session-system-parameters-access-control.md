## Metadata_Start 
## code: en
## title: System parameters - Access Control 
## slug: pam-session-system-parameters-access-control 
## seoTitle: System parameters - Access Control 
## description:  
## contentType: Markdown 
## Metadata_End
In this document, you'll find all the information about  section present in .

## Path to access

:::(warning) ()
All fields are filled in with a default value, recommended by senhasegura. However, you can make modifications as needed.
:::

1. On senhasegura, in the upper-left corner, click the , represented by the nine squares, and select settings.
2. In the side menu, select  >  > .

---
## Access Control tab
### In the General section
|
|---|---|
*|The number of parts into which the password will be divided for groups with multiple custody. You can choose from 1 to 5. By default: 2
*|Maximum time in seconds that the password window will be open. Select 0 to not close. By default: 30.
*|The time that the justification of access to a password is worth. During this period, the user will not need to provide another justification to access the password again. By default: 60.
*|Standard time that approval of a request will take in minutes. By default: 60.
*|Parameter to allow for the approver to change the approval validity parameter. By default: Yes.
*|Parameter to define whether or not a user can be part of more than one access group. By default: No.
*|Parameter to decide whetherOnly approvers with permission can be listed. By default: No.
*|Parameter to setWhether an approver can approve the request itself. By default: No.
*|Parameter to set whether duplicate credentials can be registered. By default: No.
*|Parameter to set whether it will be allowed to register devices with duplicate IP. By default: Yes.
*|Parameter to set whether batch import will be allowed. By default: No.
*|Parameter to define whether approval will be required to change user roles. If there are no approvers for User Management, the changes will be applied without approval. By default: Yes.
*|Parameter to disable the most restrictive rule for groups. Each device's request follows the access group configuration of its respective group. By default: Yes.
|Defines whether it will be mandatory for Users and Approvers to fill in the following fields. By default: Users and Approvers.
|Parameter to set whether the requester will be notified about the request via E-Mail and/or Screen. By default: Email and Screen.
|Parameter to set whether the approver will be notified for requests via E-Mail and/or Screen. By default: Email and Screen.
*|Parameter to set a message to Governance Code. By default: Governance Code.

### In the Mobile app section
|||
|---|---|
|*|Parameter to define whether all users have access to the mobile application. By default: Yes.|
|*|Parameter to define whether it’ll be necessary to request approval from the device being used for access. The App connection request must be approved by an administrator. By default: No.|


