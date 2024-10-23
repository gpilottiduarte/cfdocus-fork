## Metadata_Start 
## code: en
## title: How to configure a reconciliation credential 
## slug: pam-how-to-configure-a-reconciliation-credential 
## seoTitle: How to configure a reconciliation credential 
## description:  
## contentType: Markdown 
## Metadata_End
This tutorial shows you how to set up a credential reconciliation. It explains how to set up credentials, including choosing plugins and templates to make managing accounts easier.

***

## Requirements 
To use the reconciliation credential, you must have:
* The PAM Operator permission in senhasegura.
* A credential reconciliation active in senhasegura.

***

## How to configure a reconciliation credential
Follow the steps to set up a credential reconciliation in senhasegura:

1. In the top left corner, click the , represented by the nine-square box, and select .
2. On the side menu, select .
3. To edit the desired credential, click the icon with three vertical dots and select .
4. On the  tab, select  and choose the  field.
5. In the  field, select  if you want this process to be done automatically or  if you want this process to be done manually.

:::(Info) (Info)
With the  parameter for automated password reconciliation of a credential enabled, in case of an unsuccessful password change attempt, the credential's password reconciliation will be scheduled to run according to the chosen plugin and template.
:::

:::(Warning) (Caution)
To use the automatic password reconciliation functionality for a credential, there must be a reconciliation credential registered.
:::

6. Choose the .
7. Choose the  and .
8. Click the  button.

:::(Info)(Info)
The template determines the commands executed at reconciliation time. You can create new templates according to your needs.
:::

***

## Important note
To get reports on your passwords, activate automation with . Access it through the  path. This automation only checks if the password is valid and the access was successful. The scanning happens every fifteen minutes, always looking for passwords that still need to be verified. Once the credential is checked, it will remain unscanned for the next 24 hours.

:::(Warning) (Caution) 
It’s important to note that the automation  tests access via the  and  protocols. 
:::

: the automation accesses the user1 credential and tests its access on server1. If successful, the automation generates a report stating that the access worked. If unsuccessful, it generates a report indicating the access attempt failed. Please note that this password will no longer be tested, even if it changes, in a 24-hour period. 

The automation reports will be saved in .

***

## Next
1. .
2. .
3. .

***

Do you still have questions? Reach out to the .