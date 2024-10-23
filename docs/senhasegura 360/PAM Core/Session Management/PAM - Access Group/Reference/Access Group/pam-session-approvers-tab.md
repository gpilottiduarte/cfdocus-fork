## Metadata_Start 
## code: en
## title: Approvers tab 
## slug: pam-session-approvers-tab 
## seoTitle: Approvers tab 
## description:  
## contentType: Markdown 
## Metadata_End
In this document, you’ll  find all the information about the  tab from the registration screen to a new access group. In this section, all users who will be approvers for requests made by the access group will be added.

:::(info) ()
To find out how to register an access group, access the  document.
:::

### Path to access

1. On senhasegura, in the upper-left corner, click the , represented by the nine squares, and select .
2. In the side menu, select  >  >  > .

---
## Access group registration - Approvers

* : when clicking on the plus icon, the window with the user from the senhasegura open for selection and addition.

:::(warning) ()
For an approving user to access the approval workflow, they must have the minimum PAM Operator profile.
:::

#### List of selected approvers
* : user registration code number.
* : username.
* : name used by the user to log in.
* : user email.
* : the type of creation was carried out in the user registration.
* : which department the user belongs to.
* : name of the user who registered the user.
* : date the user was registered.
* : drop-down menu with possible approval levels. Values ​​are from 1 to 3.

When selecting an approver, the field Level from the list presents a drop-down menu with options for *Level 1*, *Level 2*, and *Level 3*. This configuration determines the sequence of calls for approval of the operation, allowing the application of a hierarchy.

For example, we can have an access group with three authorization levels. Approvers configured as *Level 1* will be the first to receive the access request.

The approvers of *Levels 2* and *3* will only be notified after the first level approvers grant access. If they don’t, then access will be denied without the other levels being notified.
Likewise, if the approver of *Level 1* grants access, but the approver of *Level 2* rejects the access request, the approver of *Level 3* won’t be notified.

It’s important to remember that if you register more than one approver for the same level, the first approver at that level who grants access will already result in a notification for the next level, thus making the process faster.
