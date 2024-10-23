## Metadata_Start 
## code: en
## title: How to manage group synchronization 
## slug: how-to-manage-group-synchronization 
## seoTitle: How to manage group synchronization 
## description:  
## contentType: Markdown 
## Metadata_End
Group synchronization in an Active Directory (AD) environment refers to the process of replicating information about user groups between different domain controllers or between AD and other systems. This ensures that groups and their respective user associations are consistent throughout the environment, allowing users to have consistent access to resources and permissions, regardless of the domain controller to which they are connected.

To synchronize LDAP/AD groups in senhasegura, follow the steps below.

## Create a new LDAP/AD group

To create a new LDAP/AD group in senhasegura, do the following:

1. In senhasegura, in the top left corner, click , represented by the nine squares, and select .  
2. In the side menu, select .  
3. In the  report, click on View , represented by the three vertical dots, and select .

## LDAP/AD group window

When you click on , the  window will appear. Fill in your group information as shown below

### Settings tab

1. : fill in the name of your group. For example: .  
2. : in the drop-down menu, select the server for the group. This server must have been registered previously.  
3. : in the drop-down menu, select the user group to which this group belongs. This group must have been registered previously.  
   1. You can add a new group by clicking the sum icon next to the  drop-down menu.  
4.  indicates the group's status at the time of creation. By default, this option is set to .  
5. : indicate whether this group can be synchronized with other groups. By default, this option is set to .  
6. : indicate the DN parameter of this group. For example: .  
7. : indicates the attributes related to the users of this group.  
8. : in the drop-down menu, select the attribute that will indicate the AD user name. The options are *Name*, *Display Name,* and *Username*.  
9. : in the drop-down menu, indicate which department this group belongs to. This department must have been registered previously.  
10. : AD query refers to locating and retrieving information stored in AD. This can include searching for users, groups, computers, organizational units (OUs), and other directory objects. For example: 

:::(info) (Info)
For more information, access the .
:::

### Domum tab

1. : Select whether you want to enable group synchronization with senhasegura Domum. By default, this option is set to .  
2. : select the type of user that will be part of this group in senhasegura Domum. By default, this option is set to   
3. : in the drop-down menu, select the group you want this group to be part of in senhasegura Domum.

### Roles tab

1. To add roles to the user group, click on the button represented by the plus sign next to the word .   
2. The  modal will be opened.  
3. In the  modal, select the roles you want to add to the group.  
4. Click  to add the roles or  to cancel the operation.

To finish registering the user group, click  on any tabs.

## Edit an LDAP/AD group

1. On senhasegura, in the top left corner, click , represented by the nine squares, and select .  
2. In the side menu, select .  
3. In the  report, identify the group you want to change and click the , represented by the pencil and paper icon, in the  column.

The  window will open in edit mode. Change the settings you want and click .

## Synchronization test for LDAP/AD groups

1. On senhasegura, in the top left corner, click , represented by the nine squares, and select .  
2. In the side menu, select .  
3. In the  report, identify the group you want to change and, in the  column, click on the icon represented by the three vertical dots and, in the drop-down menu, select the  option.  
4. In the LDAP/AD Groups window, fill in the following fields:  
   1.  fill in the group's DN parameters.  
   2.  by selecting this option, the synchronization log will be shown in plain text format. This option is unchecked by default.  
   3.  fill in the group's user filtering parameters.  
5. Click .

Just below the text box for , a message indicating the output of the synchronization command will be displayed, showing possible synchronization errors.

If you haven't checked the  option, the message will be shown as a table. For example:

| User | Username | Operation |
| :---- | :---- | :---- |
|  | John Doe |  |
|  | Jane Doe |  |

However, if you have checked the Raw View option, this output will be shown as plain text. For example:   

---

Do you still have questions? Reach out to the .