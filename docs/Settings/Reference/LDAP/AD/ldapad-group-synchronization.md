## Metadata_Start 
## code: en
## title: LDAP/AD group synchronization 
## slug: ldapad-group-synchronization 
## seoTitle: LDAP/AD group synchronization 
## description:  
## contentType: Markdown 
## Metadata_End
## Path to access

1. On senhasegura, in the upper-left corner, click the , represented by the nine squares, and select .  
2. In the side menu, select .

## Top bar

| Item  | Description |
| :---- | :---- |
|   |  |
|  | Represented by the magnifying glass icon, it displays or hides the search fields on the screen. |
|  | Represented by the counterclockwise arrow icon, it refreshes the page. |
|  | Represented by the three vertical dots icon, it shows all the possible actions for the report. |
|  | Represented by the plus icon, it opens the LDAP/AD group. |
|  | Represented by the printer icon, it opens a new page for printing the report. |
|  | Represented by the paper sheet icon, it downloads the report. |

## Search fields

| Item | Description |
| :---- | :---- |
|  | Name of the LDAP/AD group. |
|  | LDAP/AD server. |
|  | In this context, DN refers to Distinguished Name. A DN is a string that uniquely identifies an object in the AD directory, specifying the object's full path, including the object's name and location in the directory's hierarchical structure. Enter the string required to identify the group you are looking for. |
|  | Drop-down menu that filters according to synchronization status. Choose  to apply no filter;  to filter records with active synchronization and  to filter records that do not have active synchronization. |
|  | Drop-down menu that filters according to the group's status in senhasegura. It can be  or . |

## Report fields

In the list of synchronizations, you have the following fields:

*   
*   
*   
*   
*   
*  indicates when the last successful synchronization took place.  
*  indicates when the last synchronization error occurred.  
*   
*   
* In the  column, you have two options:  
  * epresented by the pencil and paper icon, opens the  window in edit mode  
    * When you click on the button represented by the three vertical dots, the drop-down menu shows three options:  
    *  opens the  form.  
    *  opens the  form.  
    *  opens the  form to test synchronization.

## LDAP/AD group window

By selecting the  option, accessed via , or the  option, accessed via , the  window will be displayed. This window contains the following fields.

### Settings tab

| Item | Description |
| :---- | :---- |
|  | Text field where you fill in the name of the group. |
|  | Drop-down menu to choose the server on which the search will be performed. |
|  | Drop-down menu for choosing the user group to which the current group will belong. : this field is responsible for defining the groups defined for synchronized users. |
|  | Radio button for choosing the status of the group when it is created. |
|  | Radio button for choosing whether the group can be automatically synchronized. |
|  | Text field where you must fill in the base DN. |
|  | Text field for entering the attributes associated with the username. |
|  | Text field for linking the user's real name to the respective field in Active Directory. |
|  | Text field where you fill in the group's search parameters. |

### Domum tab

| Item | Description |
| :---- | :---- |
|  | Radio button to choose whether you want to enable synchronization with senhasegura Domum. |
|  | Radio button for you to choose which type of senhasegura Domum user will be allowed in the group. |
|  | Drop-down menu for choosing the group in senhasegura Domum to which the LDAP/AD group will belong. |

### Roles tab

| Item | Description |
| :---- | :---- |
|  | Open the Role modal. |
|  | Name of the paper chosen. |
|  | Text field used to indicate whether the paper is one of the standards provided by senhasegura or whether it is a custom paper created by a user. |
|  | Description of the paper chosen. |

## LDAP/AD Group for synchronization test window

By selecting the  option in the  column from the  report, the  window will open to test the synchronization. This window has the following fields:

| Item | Description |
| :---- | :---- |
|  | Field for entering the base DN parameter that will be tested for synchronization. |
|  | Checkbox. If you check this box, the reply will be sent in plain text. |
|  | Field for entering the user filter parameter |