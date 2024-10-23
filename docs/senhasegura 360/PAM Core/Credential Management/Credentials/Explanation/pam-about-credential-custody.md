## Metadata_Start 
## code: en
## title: About credential custody 
## slug: pam-about-credential-custody 
## seoTitle: About credential custody 
## description:  
## contentType: Markdown 
## Metadata_End
Credential escrow in Privileged Access Management (PAM) systems refers to the practice of keeping the credentials used to authenticate access to privileged resources securely and encrypted. This practice helps protect critical information from unauthorized access, ensuring that only authorized people can access the credentials needed to perform important tasks on the system.

## My custody on the senhasegura platform

:::(info) (Info)
On senhasegura, the credential custody process is analogous to the account check-in procedure, while the custody release is analogous to the account check-out procedure.
:::

Access the credential custody area of the senhasegura platform from the , identified by the nine squares in the top left corner, and then select . On the  side menu, select the  option.

The credentials the user in question has custody of will be listed on the main page.

:::(Info) (Info)
To obtain custody of a credential, the user simply needs to view the password via the password list on the senhasegura platform. This custody will be used to release access and allow other users to access that credential.
:::

Password custody is organized according to the device to which the credential is linked (For example: , , among others). To find out more about devices in the context of senhasegura, go to the documentation about . To find out more about credentials, go to the  documentation.

## Filter credentials

You can filter the credentials that the user has custody of. To do this, use any filter field at the top of the home page. This filter has the following fields:

| Field | Description |
| --- | --- |
|  | Credential ID. |
|  | Credential type. It can be: Domain user, Local administrator, Local User, SSH key. |
|  | Device to which the credential belongs. |
|  | The username registered for the credential. |
| | Additional information registered for the credential. |
|  | Credential status. It can be Enabled or Disabled. |
|  | Button to filter the results according to the values entered. |
|  | Button to clear the fields and restart filtering. |

There are other information in the credentials list:

- : the date when the credential expires.
- : the date of the most recent modification in the custody of the credential.
- : the start date of credential custody.
- : the date when the credential was last viewed.
- : the duration of the last credential view.
- : uncheck to release the credential for other users. When the confirmation modal appears, answer  to release the credential.