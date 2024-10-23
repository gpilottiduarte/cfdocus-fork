## Metadata_Start 
## code: en
## title: Reference for authorization by application 
## slug: reference-for-authorization-by-application 
## seoTitle: Reference for authorization by application 
## description:  
## contentType: Markdown 
## Metadata_End
You can access the secrets list report through 

On the screen, you'll find the following information.

## Top bar

| Item                      | Description                                                                                              |
| ------------------------- | -------------------------------------------------------------------------------------------------------- |
|     | Represented by the magnifying glass icon, it hides or shows the filter options.                          |
|           | Represented by the counterclockwise arrow icon, it updates the information on the screen.                |
|     | Represented by the three vertical dots, it opens a drop-down menu witht the option for the module. |
|  | Opens the registration window for a new application.                                                     |
|     | Identified by the printer icon. It opens a new page for printing the report.                             |
|       | Identified by the sheet of paper icon, downloads the report.                                             |
|  | Identified by the clock icon, it opens the window for scheduling the report.                             |

When you click on , a series of fields are displayed. These are used to refine your search results by:

| Item                    | Description                                                                                                                                             |
| ----------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- |
|    | Application name.                                                                                                                                       |
|  | Authorization code.                                                                                                                                     |
|                | Authorization name.                                                                                                                                     |
|              | This field is used for segmentation within senhasegura DSM. Register systems through .      |
|         | This field is used for segmentation within senhasegura DSM. Register environments through  |
|       | Opens a calendar for you to choose the creation date. This will indicate that all authorizations created from this date will be filtered out.           |
|               | Opens a calendar for you to choose an end date for the filter. This will indicate that all authorizations created up to this date will be filtered.     |
|             | Indicates the status of the authorization. The available options are:  or .                                                                           |

In addition to these options, you have two buttons: , which applies the parameters passed in the fields; and , which clears all the parameters.

Authorizations are grouped according to the application to which they belong. When an application has multiple authorizations, it will appear listed under the application name.

:::(info) (Info)
The application name is clickable. If you click on the application name, you'll be taken to the  window in edit mode.
:::

## Application Authorization window

The  window will be displayed whenever you register or change an application authorization. It contains the following fields:

### Aba segurança

| Item                                                  | Description                                                                                                                                                                                           |
| ----------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|                         | Three checkboxes:  Indicates which resources that application will have access to.                                                                    |
|                         | Two fields. The first one opens a calendar for you to enter the authorization expiration date of this authorization. The second opens a drop-down menu to indicate the authorization expiration time. |
|                                      | Indicates the status of the authorization. Can be  or .                                                                                                                                             |
|  | Indicates whether or not you want the information marked as sensitive to be encrypted by senhasegura.                                                                                                 |
|         | Indicates whether the application should be able to create DSM applications.                                                                                                                          |
|                                  | Drop-down menu for selecting the authorization environment.                                                                                                                                           |
|                                       | Drop-down menu for selecting the authorization system.                                                                                                                                                |
|                                  | Field to indicate which IP addresses will be allowed in the authorization. Fill in the fields with  to allow any address.                                                                        |
|                       | Field to indicate which HTTP referrers will be allowed in the authorization. Fill in an empty list (blank) to allow any referer.                                                                      |
|                      | In the  section, you can paste the certificate fingerprint into the text field.                                                                                        |

### Secrets tab

When you click on the  tab, you see the plus icon next to the word . Clicking on this icon takes you to the  modal, where you can add a secret to the authorization.

In the  modal, you have the following fields:

| Item        | Description                                                                        |
| ----------- | ---------------------------------------------------------------------------------- |
|      | Secret code. Can be used to filter secrets according to code or code snippets.     |
|  | Secret name. Can be used to filter secrets according to name or parts of the name. |
|  | Button to apply the filter parameters.                                             |
|   | Button to clear the filter parameters.                                             |

Below is a list of the secrets according to the parameters passed.

| Item               | Description                     |
| ------------------ | ------------------------------- |
|  | It's used to select the secret. |
|             | Secret code.                    |
|         | Secret name.                    |

Below the list, you have two buttons: , which cancels the search and closes the modal, and , which adds the secrets selected through the checkbox. The secrets added via this modal will be associated with the authorization and shown in the  tab.

### Encryption keys tab

When you click on the  tab, you see the sum icon next to the word . Clicking on this icon takes you to the  modal, where you can add a secret to the authorization.

In the Encryption keys modal, you have the following fields:

| Item                      | Description                                               |
| ------------------------- | --------------------------------------------------------- |
|                    | Registration code for the encryption key in senhasegura.  |
|        | Name of the encryption key, as registered in senhasegura. |
|  | Algorithm used in the encryption key.                     |

Below, you have a list of the encryption keys according to the parameters passed in.

| Item                      | Description                             |
| ------------------------- | --------------------------------------- |
|              | It's used to select the encryption key. |
|                    | Encryption key code.                    |
|        | Encryption key name.                    |
|  | Algorithm used by that encryption key.  |

Below the list, you have two buttons: , which cancels the search and closes the modal, and , which adds the encryption keys selected through the checkbox. The encryption keys added via this modal will be associated with the authorization and shown in the list on the  tab.

## View the authorization through the Application Authorization window

In the list of authorizations by application, you can view authorization details. To do this, in the  column, click on the key icon to open the  window in view mode. In this window, you have the following fields:

| Item                       | Description                                                                                                      |
| -------------------------- | ---------------------------------------------------------------------------------------------------------------- |
|  | Informs the authorization authentication method.                                                                 |
|            | Informs which application that authorization is associated with.                                                 |
|             | Available only when the application is configured to use AWS authentication and has at least one associated ARN. |
|              | Client identification. To view it, click on the eye icon.                                                        |
|          | Client secret. To view it, click on the eye icon.                                                                |

### Secrets session

| Item                  | Description                                                                                 |
| --------------------- | ------------------------------------------------------------------------------------------- |
|                | Code of the secret associated with the authorization.                                       |
|              | Name of the secret associated with the authorization.                                       |
|          | The secret's identity. When creating a secret, it's mandatory to add the name and identity. |
|  | The magnifying glass icon opens the window to request authorization to view the secret.     |