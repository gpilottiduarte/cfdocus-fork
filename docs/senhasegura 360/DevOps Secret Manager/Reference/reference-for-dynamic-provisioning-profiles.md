## Metadata_Start 
## code: en
## title: Reference for dynamic provisioning profiles 
## slug: reference-for-dynamic-provisioning-profiles 
## seoTitle: Reference for dynamic provisioning profiles 
## description:  
## contentType: Markdown 
## Metadata_End
You can access a list of all available profiles via the  On the screen, you will find the following information:

## Top bar

| Field                         | Description                                                                          |
| ----------------------------- | ------------------------------------------------------------------------------------ |
|         | Represented by the magnifying glass button, it hides or shows the filter options.    |
|               | Represented by the counterclockwise arrow, it updates the information on the screen. |
|         | Represented by the three vertical dots, it opens a drop-down menu with four options. |
|          | Opens the window                           |
|         | Prints the report.                                                                   |
|           | Exports the report in  format.                                               |
|  | Opens the form to schedule the report.                                               |

## Search fields

When you click on , a series of fields are displayed. These are used to refine your search results. They are:

| Field                | Description                                                                                |
| -------------------- | ------------------------------------------------------------------------------------------ |
|          | Profile registration code in senhasegura.                                                  |
|  | Name of the profile indicated when registering with senhasegura.                           |
|        | Drop-down menu. Allows you to choose between the template types registered in senhasegura. |
|     | Drop-down menu. Indicates the status of the profile. Can be or .  |

In addition to these options, you have two buttons: , which applies the parameters passed into the fields, and , which clears all the parameters.

## Report fields

In the profile list, you have the following fields:

* .
* .
* .
* : profile lifetime in seconds.
* .
* In the  column you can find the  option, represented by the paper and pencil icon.

## Credential provisioning profile window

| Field                | Description                                                               |
| -------------------- | ------------------------------------------------------------------------- |
|  | Name to identify the dynamic provisioning profile within senhasegura.     |
|     | Indicates the status of the profile. Can be or . |

### Type section

| Field                                                      | Description                                                                                                                                                                                                                                                  |
| ---------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
|                                              | Drop-down menu to select the type of dynamic provisioning.                                                                                                                                                                                                   |
|  | Checkbox. Select this if you want to use an existing credential to access devices using the dynamic provisioning profile.                                                                                                                                    |
|               | Drop-down menu for selecting the access credential previously registered with senhasegura .Note: this menu is only enabled if you select the option.                                                |
|                               | Text field to indicate the username of the credential that will be used to access the devices via the dynamic provisioning profile.Note: this text field is only enabled if you don't select theoption. |

### Template section

| Campo                                  | Descrição                                                                                                                         |
| -------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------- |
|  | Drop-down menu to select the template responsible for creating the dynamic provisioning credential.                                 |
|                     | Next to the credential creation template drop-down menu. Clicking on the icon takes you to the form. |
|   | Drop-down menu to select the template responsible for removing the dynamic provisioning credential.                                 |
|                     | Next to theCredential removal templatedrop-down menu. Clicking on the icon takes you to the template registration form.             |
|                         | Text field for adding the roles to which the dynamic provisioning credential will be linked. Separate the roles with commas.        |
|            | Opens a modal explaining about the roles.                                                                                           |
|          | This is used to determine the lifetime, in seconds, of the dynamic provisioning credential. The default value is 3600 seconds.      |