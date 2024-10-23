## Metadata_Start 
## code: en
## title: How to create and manage encryption keys 
## slug: dsm-how-to-create-and-manage-encryption-keys 
## seoTitle: Como criar e gerenciar chaves de criptografia 
## description:  
## contentType: Markdown 
## Metadata_End
This tutorial is a step-by-step guide on creating and managing encryption keys in the  of senhasegura.

## Requirements
- You must have the necessary permissions in the role to which it is associated.

## How to Create Encryption Keys
1. On the senhasegura platform, click the  in the top left corner, represented by the nine squares, and select .
2. On the side menu, select .
3. Click on the icon , represented by the three vertical dots, and click .
4. Clicking this action will open a pop-up window named , and you need to fill in the following fields:
    - *: name of the cryptographic key.
    - *: choose the encryption algorithm.
    - : key expiration date and time.
    - : choose between Yes or No.
    - : description associated with the key.
   

5. With each key update, the version field will also be updated; the version history can be accessed through the  button within the three vertical dots icon in the  column.
6. Click on  to complete the process.

## How to View Encryption Keys
1. In the  column, click on , identified by the magnifying glass icon, to open a pop-up window.
2. In the open pop-up window, you can view the fields , ,  , , , and .
:::(Info) (Info)
  With each key update, the version field will also be updated; the version statement can be accessed through the button  inside the three vertical dots icon in the column Action.
:::
 ## How to Encrypt Data
1. In the  column, click on  identified by the gear icon to open a pop-up window.
    1. In the open pop-up window, you can view the fields , , , , , and , insert the value to be encrypted through the field , and view the encrypted value through the field .
2. Enter the value that should be encrypted in the  field.
3. Click on the  button.
4. The field  will display the encrypted value.

In the menu , it’s possible to check the logs for each encryption attempt.

## How to decrypt data
:::(Info) (Info)
The key must contain the same encryption algorithm for decryption to be performed.
:::

1. In the  column, click on  identified by the gear icon to open a pop-up window.
    1. In the open pop-up window, you can view the fields , , , , , and .
2. Click on the button.
3. Enter the value that should be decrypted  in the  field.
4. Click on the  button.
5. The field  will display the encrypted value.