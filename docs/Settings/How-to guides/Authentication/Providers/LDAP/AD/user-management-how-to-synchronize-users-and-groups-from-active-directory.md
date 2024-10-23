## Metadata_Start 
## code: en
## title: How to Synchronize Users and Groups from Active Directory 
## slug: user-management-how-to-synchronize-users-and-groups-from-active-directory 
## seoTitle: How to Synchronize Users and Groups from Active Directory 
## description:  
## contentType: Markdown 
## Metadata_End
## 

To synchronize users, you will need the following:

- A user who is part of the Domain Admins group.
- An Active Directory (AD) Authentication Server registered with senhasegura. See  for details.
- The location's Distinguished Name (DN) in AD to synchronize the users.
- Have a senhasegura .

* * *

::: (info) (LDAP/AD Group Sync Time)
senhasegura's user synchronization services run every . The services check whether any users have been added or removed from your Active Directory group, and mirror any changes in the corresponding senhasegura User Group.
:::

## Create LDAP/AD Sync Group

Each group has its own set of synchronization rules, and senhasegura can use a different LDAP server for certain groups if necessary.

To synchronize your AD users with senhasegura:

1. Go to .
2. Click the Action button  in the upper right corner, then click .
3. Inside , fill in all the required information. For more details, check LDAP/AD group.
    1. Under the  tab:
        - Give the group a name.
        - Select the  created in the requirements.
        - Select the  that will be used.
    :::(Warning) (User permissions)
    Make sure to have an "Access Group" and "Role" within your "User Group," or else your users will not have any permission.
    :::
        - Set  to .
        - Select  to  to make synchronization active.
        - Insert the DN to be used to search for the users.
        - Add an AD username attribute to be used from your AD, for example: “sAMAccountName”.
        - Select an AD name attribute.
        - Give a Query Filter. You can access  to help create your own queries. For example, 

    :::(warning) (Query words limit)
    You can type up to 2,048 characters in the  field.
    :::
4. (Optional)  tab. Only use this tab if you are using this group to be used in the Domum Senhasegura.
5. Under Roles tab:
    1. Click the  button to add a role for all users in this group.
6. Click .


## Group Sync Test

To ensure that your group is synchronizing correctly and collecting the correct users, you can perform a sync test.

Follow these steps:

1. Under the Action column, locate the group you want to test.
2. Click on the group's Action button (  ), and choose .
3. In the  window, senhasegura fills in the DN and filter fields with the group's configuration values. You can change these fields for testing without affecting the original group settings.
4. Click .
5. A table will show the results of users being added, removed, or unchanged.
6. After the simulation, Senhasegura returns the list of users in the AD group. Users are listed as added, modified, or unchanged.

If any errors occur, check out our  article.
