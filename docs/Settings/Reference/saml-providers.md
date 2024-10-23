## Metadata_Start 
## code: en
## title: SAML providers 
## slug: saml-providers 
## seoTitle: SAML providers 
## description:  
## contentType: Markdown 
## Metadata_End
This document provides a general overview about the SAML providers functionality.

## Path to access

1. On senhasegura, in the top left corner, click , represented by the nine squares, and select 
2. In the side menu, select 

## Top bar

| Item                      | Description                                                                                                                                                                                              |
| ------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|     | Represented by the magnifying glass icon, it displays or hides the search fields on the screen.                                                                                                          |
|           | Represented by the counterclockwise arrow icon, it refreshes the page.                                                                                                                                   |
|     | Represented by the three vertical dots icon, it shows all the possible actions for the report.                                                                                                           |
|     | Represented by the plus icon, it opens the  screen.                                                                                                                                |
|     | Represented by the printer icon, it opens a new page for printing the report.                                                                                                                            |
|       | Represented by the paper sheet icon, it downloads the report.                                                                                                                                            |
|  | Represented by the clock icon, it opens the  form. |

## Search fields

| Item                                 | Description                                                                                                               |
| ------------------------------------ | ------------------------------------------------------------------------------------------------------------------------- |
|                          | SAML provider code in senhasegura.                                                                                        |
|                        | Drop-down menu to select the type of SAML provider. The options are *Azure, KeyCloak, Okta*, and *SAML provider*. |
|                   | ClientIdorEntityIdof the SAML application.                                                                                |
|  | URL responsible for the provider's metadata.                                                                              |
|                     | Drop-down menu to select the status of the SAML provider. The options are  or .                   |
|                 | Drop-down menu to select the SAML provider environment. The options are              |

## Report fields

The results of the list are shown below:

* .
* .
* 
* 
* .
* .
* In the  column, you have two options:
  * : represented by the pencil and paper icon, opens the  window.
  *  represented by the trash can icon, deletes the SAML provider.

## SAML provider registration window

By clicking on r, the registration window for the new SAML provider will open. You'll see the following fields:

### General information tab

| Item                                           | Description                                                                                                                                        |
| ---------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------- |
|                                  | Drop-down menu for registering the type of SAML provider.                                                                                          |
|                               | Radio button for selecting the status of the SAML provider to be opened. By default, it is set toYes.                                              |
|                           | Radio button for selecting the environment in which the SAML provider will be involved. It can be or  |
|                             | Field to register theClientIDorEntityID.                                                                                                           |
|            | Field for registering application/realm metadata.                                                                                                  |
|  | Field for registering senhasegura's domain or public IP.                                                                                           |
|                          | URL do redirect.                                                                                                                                   |
|                               | Field for registering comments relating to the SAML provider.                                                                                      |
|                       | .                                                                                                                             |
|                      | .                                                                                                                             |
|              | Drop-down menu for choosing the type of  for the .                                                 |

### Aba SAML de segurança

It only contains the , where you must paste your certificate.

Please note that all the settings in the SAML security tab must be strictly the same as those configured in the  to ensure that SAML works properly. Any discrepancies will result in authentication failures.