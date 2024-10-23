## Metadata_Start 
## code: en
## title: How to manage notifications 
## slug: notification-how-to-manage-notifications 
## seoTitle: How to manage notifications 
## description:  
## contentType: Markdown 
## Metadata_End
senhasegura enables the sending of reports via email, as well as scheduling them. This allows you to schedule the sending of, for example, the remote sessions report to certain users. These users will receive the reports when these notifications are sent, thus always staying updated about new remote sessions conducted during the period.

## Requirements

* To use the SMS notification sending option, it's necessary to have the Zenvia integration properly configured.  
  * SMS notifications won’t be sent without this configuration. To learn how to configure the Zenvia integration, access the SMS Service Integration document.  
* For email notifications, ensure that a default email is correctly configured.  
* You can find more information on how to integrate the Zenvia service with senhasegura by accessing the document .

## Register a new notification

1. In senhasegura, in the upper left corner, click , represented by nine squares, and select .  
2. In the side menu, select .  
3. The  report will display the notifications registered on senhasegura.  
4. To create a new notification, in the top bar, click on , represented by the three vertical dots icon, and select  from the dropdown menu.  
5. In the  window, fill in the following fields:  
   1. : a name for the new notification.  
      1. Next to the Name field, select the means you wish to use to send the notification. The options are *Email, Screen*, and *SMS*. You must select one or more of these options.  
         2. Note that it's also possible to choose if the notification will be sent only to contacts who have access to credentials or devices.  
   2. In the  tab, click on the plus sign next to the word  to open the  modal. In this, select the notifications you wish to send. Notice that now the desired notification will appear within the notifications field.  
   3. In the  tab, click on the plus sign next to the word  to open the  modal. In this, select the contacts who will receive the notifications.  
6. Click .

:::(warning) (Attention!)  
To use the SMS notification sending option, the Zenvia integration must be properly configured. Without this configuration, SMS notifications will not be sent. To learn how to configure the Zenvia integration, access the  document.  
:::

## How to modify a notification

1. On senhasegura, in the upper left corner, click the , represented by nine squares, and select .  
2. In the side menu, select .  
3. The  report will display the notifications registered on senhasegura.  
4. In the  column, click on , represented by the pencil and paper icon.  
5. The  window will open in edit mode.  
6. Change the necessary information and click .

## How to deactivate a notification

1. On senhasegura, in the upper left corner, click the , represented by nine squares, and select .  
2. In the side menu, select .  
3. The  report will display the notifications registered on senhasegura.  
4. Identify the notification you wish to deactivate and, in the  column, click on the icon represented by three vertical dots and select .  
5. In the confirmation modal, click on .

## How to reactivate a notification

1. On senhasegura, in the upper left corner, click the , represented by nine squares, and select .  
2. In the side menu, select .  
3. The  report will display the notifications registered on senhasegura.  
4. In the search menu, in the top bar, click on the  dropdown menu and select the  option.  
5. Click .  
6. The listing will filter the registered notifications that are deactivated. They will be shown with the text in red color.  
7. Identify the notification you wish to reactivate. In the  column, click on the icon represented by three vertical dots and select .  
8. In the confirmation modal, click on .

## How to customize a notification

Some of the texts in the notification templates used by senhasegura can be modified according to your needs. To make this type of change, follow the steps below:

1. On senhasegura, in the upper left corner, click the , represented by nine squares, and select .  
2. In the side menu, select   
3. In the  report, identify the notification you wish to customize.  
4. In the  column, click , represented by the pencil and paper icon.  
5. The  window will open.

### Modify the text of a notification

In the  window, you have the following options:

1. : informs the name of the notification type being changed. For example: Request Created: Approver  
2. : select if you want the new text to be used. By default, it's marked as Yes.  
3. : expression for the subject of the email that will be sent in the notification. For example: 
4. : rich text editor that allows editing of the default text of the notification Email.

This text should contain the e-mail tags.

`
Hello [#APPROVER#],
The user [#REQUESTER#] requested [#ACTION#] of the user [#CREDENTIAL_USERNAME#] on the device [#DEVICE_HOSTNAME#] ([#DEVICE_IP#]).
[#ACTION_LIST#]
Reason: [#REASON#]
Code Governance: [#GOVERNANCE_ID#]
Justification: [#JUSTIFICATION#]
Period: [#START_TIME#] to [#END_TIME#]
To approve access to the system or click one of the links below:
[#LINK_APPROVE#] [#LINK_REJECT#]
Or reply to this email with one of the words:
APPROVE
REJECT
`

5. Click on .

### TAGs

An essential portion for creating notification email texts are the TAGs. They serve as placeholders for certain information about the user who will receive the report/notification. The TAGs used in senhasegura are:

Here's the text with the requested modifications:  

*   : Request code on format S000000.  
*   : Request status.  
*   : User who is requesting access to password.  
*   : Date of request.  
*   : Name of the approver who will receive the request email.  
*   : Name of approver who responded to the request.  
*   : Date when the request was answered by the approver.  
*   : Requested action.  
*   : Action requested on list format.  
*   : Action requested on list format using syslog template.  
*   : URL to approve access to password.  
*   : Link to approve access to password.  
*   : URL to reject access to password.  
*   : Link to reject access to password.  
*   : Device hostname.  
*   : Device IP.  
*   : Credential username.  
*   : Credential type.  
*   : Specified reason.  
*   : Reason specified by requester.  
*   : Governance ID.  
*   : Start date and time of requested access period on 08/27/2024 15:14:05 format.  
*   : End date and time of requested access period on 08/27/2024 15:14:05 format.  
*   : Start date and time of requested access period on Tuesday, August 27 03:14 PM format.  
*   : End date and time of requested access period on Tuesday, August 27 03:14 PM format.  
*   : Start date of requested access period on 08/27/24 format.  
*   : End date of requested access period on 08/27/24 format.  
*   : Start time of requested access period on 3:14 pm format.  
*   : End time of requested access period on 3:14 pm format.  
*   : Credential involved on request.  
*   : Name of certificate responsible.  
*   : Certificate environments separated by comma.  
*   : Certificate systems separated by comma.  
*   : Certificate tags separated by comma.  
*   : Certificate description.  
*   : Certificate common name.  
*   : Certificate issuer information.  
*   : Certificate validity start date.  
*   : Certification expiration date.