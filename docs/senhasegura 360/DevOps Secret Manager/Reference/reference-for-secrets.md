## Metadata_Start 
## code: en
## title: Reference for bulk actions 
## slug: reference-for-secrets 
## seoTitle: Reference for bulk actions 
## description:  
## contentType: Markdown 
## Metadata_End
Bulk actions for secrets within the senhasegura DevOps Secret Manager are accessible through , represented by the button at the bottom of the page.

The bulk action process is divided into 3 steps: *Choice of operation, Choice of secrets,* and *Confirmation*.

## Step 1: Choosing an operation

| Item                     | Description                                             |
| ------------------------ | ------------------------------------------------------- |
|  | Option to start the bulk disabling process for secrets. |
|   | Option to start the bulk enabling process for secrets.  |
|   | Option to start the bulk expiration process of secrets. |

In the bottom right corner, you have the  button to move on to step 2.

## Step 2: Choosing the secrets

| Item               | Description                                                                                                                                                                                |
| ------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
|  | Option to add the secrets you want to perform a bulk operation on. By clicking the add sign, you'll be directed to the  modal, where you can choose the secrets to be changed. |

### Secrets modal

| Item                 | Description                                                         |
| -------------------- | ------------------------------------------------------------------- |
|               | Code used to register the secret in senhasegura.                    |
|             | Name of the secret in senhasegura.                                  |
|         | Name of the identity associated with the secret within senhasegura. |
|           | Name of the engine associated with the secret within senhasegura.   |
|  | Expiration date associated with the secret within senhasegura.      |

To perform the search, click on the  button; to clear the fields and restart the process, click on the  button.

The results of the secrets will be presented in the form of a list in the  modal, following the existing fields in the filter, plus:

* : select to add this secret to your selection.
* : environment associated with the secret in senhasegura.
* : button to cancel the selection of secrets for the bulk operation. By clicking, no action will be taken, and the modal will be closed.
* : button to add the selection of secrets to the bulk operation. By clicking, the selected secrets will be added to the bulk action, and the modal will be closed.

There are two buttons in the bottom right corner: , to advance to step 3; , to go back to step 1.

## Step 3: Confirmation

| Item                        | Description                                                                                                                                                                                                                                                                                                                                                                                                    |
| --------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|            | Indicates which change is being made. It can be of the type  (the  field is assigned the value ),  (the  field is assigned the value ), or  (the   field is assigned the value of the current time on the user's system in the format ). |
|  | Indicates the secrets (entities) that will be affected by the change.                                                                                                                                                                                                                                                                                                                                          |

The secrets affected by the changes are listed below the  section and have the following fields:

| Item                 | Description                                                     |
| -------------------- | --------------------------------------------------------------- |
|               | Secret registration code within senhasegura.                    |
|             | Secret registration name within senhasegura.                    |
|         | Name of the identity associated with the secret in senhasegura. |
|           | Name of the engine associated with the secret in senhasegura.   |
|  | Expiration date associated with the secret in senhasegura.      |

In the bottom right corner, you have two buttons: , to finish the process and save the bulk operation request; , to go back to step 2.