## Metadata_Start 
## code: en
## title: Identity management providers (IGA) 
## slug: identity-management-providers-iga 
## seoTitle: Identity management providers (IGA) 
## description:  
## contentType: Markdown 
## Metadata_End
This document provides a general overview of the ) functionality.

## Path to access

1. On senhasegura, in the top left corner, click the , represented by the nine squares, and select 
2. In the side menu, select .

## Top bar

| Item                      | Description                                                                                                                                                                                            |
| ------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
|     | Represented by the magnifying glass icon, it displays or hides the search fields on the screen.                                                                                                        |
|           | Represented by the counterclockwise arrow icon, it refreshes the page.                                                                                                                                 |
|     | Represented by the three vertical dots icon, it shows all the possible actions for the report.                                                                                                         |
|              | Represented by the plus icon, it opens theRegister Identity Management Providerscreen.                                                                                                                 |
|     | Represented by the printer icon, it opens a new page for printing the report.                                                                                                                          |
|       | Represented by the paper sheet icon, it downloads the report.                                                                                                                                          |
|  | Represented by the clock icon, it opens the  form. |

## Search field

| Item                        | Description                                                                                                   |
| --------------------------- | ------------------------------------------------------------------------------------------------------------- |
|                 | Provider registration code in senhasegura.                                                                    |
|               | Name of the provider in senhasegura.                                                                          |
|               | Tags associated with the provider.                                                                            |
|           | Drop-down menu for choosing the provider's authentication protocol.                                           |
|  | Opens a calendar for choosing the provider's registration date. This date will be the filter's start date.    |
|              | Opens a calendar for choosing the provider's registration date. This date will be the end date of the filter. |
|             | Drop-down menu for choosing the provider's status. It can be  or .                            |

## Report fields

The list contains the following fields:

* .
* 
* .
* .
* : indicates the authentication method used by the provider.
* 
* .
* : indicates whether the authentication provider synchronizes users with senhasegura Domum.
* In the  column, you have two options:
  * : represented by the pencil and paper icon, opens the  window in edit mode.
  * : by clicking on the three vertical dots icon, you have two options:
    * : represented by the magnifying glass icon, opens the  window.
    * r: represented by the trash can icon, deletes the provider.

## Register Identity management provider window

By clicking on Update provider in the  column, or on , you'll have access to the window for registering new providers. It contains the following fields:

### Settings tab

| Item                          | Description                                                                                                   |
| ----------------------------- | ------------------------------------------------------------------------------------------------------------- |
|                 | Name of the authentication provider.                                                                          |
|             | Authentication protocol used by the provider.                                                                 |
|  | Drop-down menu to indicate which users will be synchronized with senhasegura Domum.                           |
|              | Radio button to indicate whether or not the provider is active in senhasegura. It can be  or . |
|          | Text fields for entering the description of the authentication provider.                                      |
|                 | Text field with the tags associated with the authentication provider.                                         |

### Authentication tab

| Item                                                   | Description                                                                                                                                                                                                                                                                |
| ------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|                              | Drop-down menu to indicate which authentication method the authentication provider is using.                                                                                                                                                                               |
|                               | The first field opens a calendar for selecting the expiration date. The second field opens a drop-down menu for choosing the expiration time. Note that the time is given in fifteen-minute intervals, but you can enter a custom time as long as it is valid. |
|                | Label to indicate from which IP addresses API requests can be made.                                                                                                                                                                                                        |
|                                            | IP addresses where API requests can be made.                                                                                                                                                                                                                               |
|                                   | Deletes the selected IP.                                                                                                                                                                                                                                                   |
|  | Label for the referers allowed by the authentication provider.                                                                                                                                                                                                             |
|                                            | HTTP referers, to which authentication will be allowed.                                                                                                                                                                                                                    |
|                                   | Deletes the selected HTTP Referer.                                                                                                                                                                                                                                         |
|                                           | In the bottom-right corner of the page, it indicates the changes made to the authentication provider and the user has made them.                                                                                                                                     |