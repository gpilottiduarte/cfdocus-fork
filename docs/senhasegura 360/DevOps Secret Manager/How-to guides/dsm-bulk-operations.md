## Metadata_Start 
## code: en
## title: How to use bulk actions for secrets 
## slug: dsm-bulk-operations 
## seoTitle: Bulk actions for secrets 
## description:  
## contentType: Markdown 
## Metadata_End
You can use bulk operations to enable, disable, or expire the secrets registered in the senhasegura DevOps Secret Manager (DSM) when necessary.

:::(info) (Info)
As visual feedback, you can follow the stage you are currently at. To do this, look at the top portion of the credentials list screen to see where you are in the bulk operation process.
:::

## Perform bulk operations to DSM secrets

1. On senhasegura, in the top left corner, click , represented by the nine squares, and select .
2. In the side menu, select .
3. On the secrets list page, select the ones you want to change and, in the bottom right corner, click .
4. Choose the type of change. You can choose three options: *Inactivate DSM secrets, Activate DSM secrets*, and *Expire DSM secrets*.

:::(warning) (Caution)
To carry out any of the bulk operations, there must be approvers. For more information, see the documentation on How to register an approver user.
:::

## Enable secrets in DSM using Bulk Actions

:::(info) (Info)
The bulk action option allows you to activate or reactivate several secrets simultaneously. Note, however, that only disabled secrets can be selected for activation.
:::

1. After selecting the  option, click the  button.
2. Now, you can choose the secrets you want to enable. To do this, click on the sum icon next to the word Secrets.
3. In the  modal, select all the secrets you want to enable. You can use the search tools at the top of the modal.
4. Click .
5. Click .
6. In the third step, you have two sections:
   1. : displays the fields that have been changed, in this case: .
   2. : displays information about the entities affected by the bulk operation, such as *Code, Secret name, Identity, Engine, Environmen*t, and *Expiration Date*.
7. Click .

## Disable secrets in DSM using Bulk Actions

:::(info) (Info)
The Bulk action option allows you to disable several secrets simultaneously. Note, however, that only active secrets can be selected for disabling.
:::

1. After selecting the  option, click the  button.
2. Now, you can choose the secrets you want to disable. To do this, click on the sum icon next to the word .
3. In the  modal, select all the secrets you want to disable. You can use the search tools at the top of the modal.
4. Click .
5. Click .
6. In the third step, you have two sections:
   1. : displays the fields that have been changed, in this case: .
   2. : displays information about the entities affected by the bulk operation, such as *Code, Secret name, Identity, Engine, Environmen*t, and *Expiration Date*.
7. Click .

## Expire secrets in DSM using Bulk Actions

:::(info) (Info)
The bulk action option allows you to expire several secrets simultaneously. Note, however, that only enabled secrets can be expired.
:::

1. After selecting the  option, click the  button.
2. Now, you can choose the secrets you want to expire. To do this, click on the sum icon next to the word Secrets.
3. In the  modal, select all the secrets you want to expire. You can use the search tools at the top of the modal.
4. Click .
5. Click ext.
6. In the third step, you have two sections:
   1. : displays the fields that have been changed, in this case: .
      1. The expiration date will take the value of the current date and time on the user's system.
   2. : displays information about the entities affected by the bulk operation, such as *Code, Secret name, Identity, Engine, Environmen*t, and *Expiration Date*.
7. Click .

If no errors have occurred, you'll see a success message: ". The operation will be executed after approval by those responsible. Together with a shortcut button to the  section of senhasegura.

Once the process has been completed, a user who is registered as an approver for the DSM module will need to approve the changes for them to be applied.

---

Do you still have questions? Reach out to the 