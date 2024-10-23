## Metadata_Start 
## code: en
## title: SMTP Configuration 
## slug: smtp-configuration 
## seoTitle: SMTP Configuration 
## description:  
## contentType: Markdown 
## Metadata_End
In this document, you'll find all the information about the  report.

## Path to access

1. In senhasegura, in the upper left corner, click the , represented by the nine squares, and select .  
2. In the side menu, select .

## Top bar

| Item  | Description |
| :---- | :---- |
|  | Represented by the magnifying glass icon, it displays or hides the search fields on the screen. |
|  | Represented by the counterclockwise arrow icon, it refreshes the page. |
|  | Represented by the three vertical dots icon, it shows all the possible actions for the report. |
|  | Represented by the plus icon, it opens the  window. |
|  | Represented by the printer icon, it opens a new page for printing the report. |
|  | Represented by the paper sheet icon, it downloads the report. |
|  | Represented by the clock icon, it opens the  form. |

## Search fields

| Item | Description |
| :---- | :---- |
|  | SMTP account code in senhasegura. |
|  | SMTP account name. |
|  | E-mail address of the SMTP account representative. |
|  | Reply-to e-mail address of the SMTP account. |
|  | Return e-mail address (Return-Path) of the SMTP account. |
|  | SMTP account confirmation e-mail address. |
|  | *Radio button* for filtering according to SMTP account status. Can be  or . |

## Report fields

*   
*   
*   
*   
*   
*   
*   
*  indicates whether this SMTP account is the default one used in senhasegura.  
*  indicates whether the SMTP account uses a secure connection.  
*  indicates whether the SMTP account should be forced to use the configuration section.  
*  indicates whether the SMTP account receives a confirmation that the message has been read  
*  indicates whether the account sends a footer in the e-mail.  
* In the  column, you have two options:  
  *  is used to change the server's settings. It opens the  window.  
  * : is used to test the sending configuration of the . Open the  window.

:::(info) (Info)
The report displays 30 records per screen. To go to the next screen, click on the next button at the end of the report.
:::

## SMTP server settings window

Clicking on the  or  option takes you to the , which contains the following information.

| Item | Description |
| :---- | :---- |
|  | SMTP account name. |
|  | *Radio button*. Indicates whether the SMTP account is active. Can be  or . |
|  | E-mail address of the SMTP account representative. |
|  | Reply e-mail address of the SMTP account. |
|  | Return e-mail address of the SMTP account. |
|  | SMTP account confirmation e-mail address. |
|  | *Radio button*. Indicates whether the account is the default account used in senhasegura. Can be  or . |
|  | *Radio button*. Indicates whether the SMTP account will receive a confirmation that the message has been read. Can be  or . |
|  | *Radio button*. Indicates whether the SMTP account should be forced to use the configuration. Can be  or . |
|  | *Radio button*. Indicates whether the account sends a footer in the e-mail. Can be  or . |
|  | Host address of the SMTP account. |
|  | Port on which the host listens. |
|  | *Radio button*. Indicates whether the SMTP account should use a secure connection. Can be  or . |
|  | *Radio button*. Indicates which type of secure connection the SMTP account should use. It can be  or . |
|  | *Radio button*. Indicates whether the SMTP account should use a credential to authenticate itself. Can be  or . |
|  | *Radio button*. Indicates whether the SMTP account should ignore any certificate errors. Can be  or . |
|  | *Radio button*. Indicates whether the SMTP account should use a Network Connector previously registered with senhasegura. Can be  or . |
|  | Drop-down menu. Select the  to use for the SMTP account connection. Note: this option will only be enabled if you select  on the  radio button. |
|  | A drop-down menu. Select the credential that will be used to authenticate the SMTP account. Note: if you select  in the  option, selecting a credential is mandatory; the credential must have been previously registered with senhasegura. |

## Test e-mail \- Account window

Clicking on  takes you to the  window, which contains the following fields.

| Item | Description |
| :---- | :---- |
|  | Text field. Fill in the e-mail address where senhasegura should send the test message. |
|  | Text field. Fill in the subject of the test e-mail. By default, it’s filled in with the string  |
|  | Text field. Fill in the body of the test e-mail. By default, it’s filled with the string  |