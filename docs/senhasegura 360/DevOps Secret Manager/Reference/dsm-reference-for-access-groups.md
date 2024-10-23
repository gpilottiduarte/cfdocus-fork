## Metadata_Start 
## code: en
## title: Reference for access groups 
## slug: dsm-reference-for-access-groups 
## seoTitle: Reference for access groups 
## description:  
## contentType: Markdown 
## Metadata_End
# Reference for Access groups

The access groups within senhasegura DevOps Secret Manager are accessible through 

## Top bar

| Item                 | Description                                                                                  |
| -------------------- | -------------------------------------------------------------------------------------------- |
|     | Represented by the magnifying glass icon. Displays or hides the search fields on the screen. |
|           | Represented by the counterclockwise arrow icon. Refreshes the page.                          |
|     | Represented by the three vertical dots icon. Displays the possible actions for the page.     |
|        | Represented by the plus symbol. Opens the window for registering a new access group.         |
|     | Represented by the printer icon. It opens a new page for printing the report.                |
|       | Represented by the sheet of paper icon, downloads the report.                                |
|  | Represented by the clock icon. It opens the window for scheduling the report.                |

When you click on , a series of fields are displayed. These are used to refine your search results. They are:

| Item                            | Description                                                                                                         |
| ------------------------------- | ------------------------------------------------------------------------------------------------------------------- |
|                     | Code of the access group registered with senhasegura.                                                               |
|                   | Access group's name.                                                                                                |
|  | Drop-down menu. Filters according to users' permission to view secrets. Can be set to or . |
|                | Drop-down menu. Filters according to the status of the access group. Can be set to  or .             |

In addition to these options, you have two buttons: , which applies the parameters that have been passed into the fields, and , which clears all the parameters.

Next, we have the list field containing all the groups, filtered or not, which are displayed with the following fields:

* .
* .
* 
*  indicates whether this access group requires a justification from the user to be viewed.
*  indicates whether this access group requires approval from an approving user to be viewed.
*  indicates whether this access group requires approval in different levels.
*  indicates whether the access group allows the user to have emergency permission, bypassing the need for approval.
* .

## Access group registration window

In the  column, when you click on the Refresh icon, the  window opens.

| Item                        | Description                                                             |
| --------------------------- | ----------------------------------------------------------------------- |
|  | Name of the group registered with senhasegura.                          |
|            | Access group status in senhasegura. This is set to  by default. |
|        | Access groups description.                                              |

### Settings tab

#### In the Secrets preview setting section:

| Item                                           | Description                                                                                                                                                   |
| ---------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|                | Checkbox. This allows you to select whether users in this access group will have access to viewing secrets.                                                   |
|                             | Checkbox. This allows you to select whether users in this access group must fill in a justification for viewing.                                              |
|                           | Checkbox. This allows you to select whether users in this access group must be approved for viewing.                                                          |
|                         | Allows you to indicate how many approvals are required for granting access.                                                                                   |
|            | Allows you to indicate how many failures are necessary for access to be denied.                                                                               |
|                         | Checkbox. Allows you to indicate whether approval should be in levels.                                                                                        |
|    | Allows you to indicate whether users of this access group must fill in the justification with a governance code. Can be set to  or .           |
|  | Allows you to indicate whether the user's manager will automatically be added as an approving user for that justification. Can be set to  or . |

### Criteria tab

#### In the Application section:

| Item                                     | Description                                                                                                                                  |
| ---------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------- |
|  | Name of the applications that will be part of the access group. To indicate more than one application, enter the names separated by a comma. |
|   | Tags das aplicações que farão parte do grupo de acesso. Para indicar um grupo de tags, insira-as separadas por vírgula.                  |
|                     | Checkbox. Allows you to indicate the lines of business that the applications are part of. Allows more than one item to be selected.          |
|                    | Checkbox. Type of application. Allows more than one item to be selected.                                                                     |

#### In the Authorizations section:

| Item                                | Description                                                                                                                        |
| ----------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------- |
|       | Systems to which the access group has authorization. To indicate more than one system, enter the names separated by a comma.       |
|  | Environments to which the access group is authorized. To indicate more than one environment, enter the names separated by a comma. |

#### In the Secrets section:

| Item                                       | Description                                                                                                                                               |
| ------------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
|         | Secrets that the access group will be allowed to access. To indicate more than one secret, enter the names separated by a comma.                          |
|  | Environments of the secrets that the access group will be allowed to access. To indicate more than one environment, enter the names separated by a comma. |
|          | Tags of the secrets that the access group will be allowed to access. To indicate more than one tag, enter the names separated by a comma.                 |

#### In the Users section:

This section lists all the users who are part of the access group. These users are presented in the form of a list with the following fields:

| Item                  | Description                                                          |
| --------------------- | -------------------------------------------------------------------- |
|  | Serve para excluir aquele usuário do grupo de acesso.               |
|                | User registration code in senhasegura.                               |
|              | Name of the user in senhasegura.                                     |
|          | Username in senhasegura.                                             |
|            | User's e-mail address in senhasegura.                                |
|     | Type of user creation.                                               |
|        | Department to which the user belongs.                                |
|          | Name of the user who added the user in question to the access group. |
|          | Date and time the user was added to the access group.                |

#### On the Approvers section:

This section lists all the users who are part of the access group with the role of approving user. These users are presented in the form of a list with the following fields:

| Item                       | Description                                                                                                                           |
| -------------------------- | ------------------------------------------------------------------------------------------------------------------------------------- |
|  | This is used to remove the user from the approvers group.                                                                             |
|                | User registration code in senhasegura.                                                                                                |
|          | Username on senhasegura.                                                                                                              |
|            | User's e-mail address in senhasegura.                                                                                                 |
|     | User creation type.                                                                                                                   |
|        | Department to which the user belongs.                                                                                                 |
|          | Name of the user who added the user in question to the access group.                                                                  |
|          | Date and time the user was added to the access group.                                                                                 |
|             | Drop-down menu. Allows you to indicate the approver level the user will have. It can take the values *Level 1, Level 2, or Level 3.* |

:::(info) (Info)
At the bottom of the window, you can view information about the access group. To do this, hover over the eye icon to display information about the user, date and time they created the group, and the user, date and time they last changed the access group settings.
:::