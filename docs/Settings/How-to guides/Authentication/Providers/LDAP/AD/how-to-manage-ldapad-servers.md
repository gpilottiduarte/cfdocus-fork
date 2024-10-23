## Metadata_Start 
## code: en
## title: How to manage LDAP/AD servers 
## slug: how-to-manage-ldapad-servers 
## seoTitle: How to manage LDAP/AD servers 
## description:  
## contentType: Markdown 
## Metadata_End
senhasegura allows you to use Active Directory (AD) for identity management. If you want to use AD with senhasegura, follow the steps below.

## Register an LDAP/AD server

1. On senhasegura, in the top left corner, click the , represented by the nine squares, and select .  
2. In the side menu, select .  
3. In the  form, click on  in the taskbar in the top-right corner and select  from the drop-down menu.  
4. In the  window, fill in the fields below:  
   1. : enter the address of the LDAP host.  
   2. : enter the port of the LDAP host.  
   3. : indicate whether the server is active or not. By default, this option is set to .  
   4.  select the credential that will be used to authenticate to the LDAP server from the drop-down menu.  
   5. : select from the drop-down menu which connector will be used with the LDAP server.  
   6. : enter the starting location of the directory from which the search or operation will begin. This will be the starting point for searching, adding, modifying, or deleting objects on the LDAP server.  
   7. : select the type of account form from the drop-down menu. The options are: *DN, Username, Backslash*, and *Main*.  
   8.  .  
      1. In this case, the fields are:  
         1. : the type of the object must be .  
         2. : the user's SAM (Security Account Manager) account name must be .  
   9. : specify the domain of the account. For example, .  
   10. : enter the account's short name, specifically. For example: .  
   11. : indicate whether you want to use a domain credential. By default this option is set to .  
   12. : enter the account's unique username.  
   13.  enter the DN that will be used as the unique identifier. For example   
   14. : select  if the user is identified by their DN  
   15.  select  if the bind process needs to use DN.  
   16.  enter the account group.  
   17.  enter the account's DN.  
   18.  enter the attributes of the group.  
   19.  enter the group scope.  
   20.  enter a filter expression for the group. For example:  which will return all objects within the LDAP/AD server that are of type .  
   21.  enter the attributes of the group members.  
   22.   
   23.  select whether you want to use the SSL protocol. By default this option is set to   
5. Click .

## Edit an LDAP/AD server

1. On senhasegura, in the top left corner, click the , represented by the nine squares, and select .  
2. In the side menu, select .  
3. In the  form, select the server you want to edit and, in the  column, click , represented by the pencil and paper icon.

The  window will open in edit mode and you can modify the necessary attributes. Then click  to save the changes.

## Test the authentication of an LDAP/AD server

1. On senhasegura, in the top left corner, click the , represented by the nine squares, and select .  
2. In the side menu, select .  
3. In the  form, select the server you want to edit and, in the  column, click on the three vertical dots icon and select  from the drop-down menu.  
4.  In the  window, fill in the following fields:  
   1. : fill in the Base DN value. For example: .  
   2. : fill in the username. For example:   
   3. : fill in the user's password.  
5. Click .

A message will appear below the fields indicating whether authentication succeeded or failed.  

---

Do you still have questions? Reach out to the .