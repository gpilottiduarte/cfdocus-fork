## Metadata_Start 
## code: en
## title: How to add an access group 
## slug: pam-session-how-to-add-an-access-group 
## seoTitle: How to add an access group 
## description:  
## contentType: Markdown 
## Metadata_End
This document, will guide you through a step-by-step process on how to add access groups and their rules in PAM Core module.

### Requirements

* Be an admin user.
---
## Add an access group
:::(info) ()
For more information on the access groups fields, access the  documents.
:::

1. On senhasegura, in the upper-left corner, click , identified by the nine squares icon, and then select .
2. In the side menu, select  >  .
3. In the upper-right corner, click the three vertical dots icon and select .
4. At the  window, fill in the mandatory fields identified with the asterisk.
    1. *: type a name for the group identification.
    2. *: select the option .
    3. : if needed, type a group description.
5. At the  tab, select the desired settings for this group.
6. At the  tab, fill in the available fields and select the *, *, and * associated with the group.
7. At the  tab, click the add icon, located on the right side of the  word, and add the users associated with the group.
8. At the  tab, click the add icon, located on the right side of  word, and add the users associated with the group.
    :::(info) ()
    To ensure that the approver user can access the approval workflow screen, they must possess a minimum of a PAM Operator profile.
    :::
9. At the  tab, set up the permissions that will be valid for this group.
10. Click .

senhasegura will display a confirmation notice and the group will be displayed in the Access groups list on the main screen.

:::(info) ()
By default, when a user is registered in more than one group with different access settings, the platform will follow the restriction rule by the credential and device combined. However, if the standard option is changed, senhasegura will follow the most restricted rule for that group. To know how to change the default option, access the document.
:::

---
## Next:



Do you still have questions? Reach out to the .