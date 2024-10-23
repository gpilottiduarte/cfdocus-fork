## Metadata_Start 
## code: en
## title: About the repetition of records in batch import 
## slug: pam-about-the-repetition-of-records-in-batch-import 
## seoTitle: About the repetition of records in batch import 
## description:  
## contentType: Markdown 
## Metadata_End
When performing a , it's essential to understand how repetitions are handled in each scenario:

1.  when a device populated in the spreadsheet has the same name as a device already registered in senhasegura, the existing device will be updated with the new information from the spreadsheet.
2.  if you want to register more than one user on the same device, you need to repeat the process of filling in the required fields of the device in the spreadsheet. This will keep the device intact and automatically associate the new credentials.
3.  in case any credential is added improperly and needs to be deleted, simply fill in the first column of the spreadsheet with the letter . This will perform the deletion action and deactivate the corresponding credential.

## Scenarios to be considered

When importing the file, the following scenarios will be considered:

-  if the devices and their credentials aren't currently registered in senhasegura, appropriate records will be created for them.

:::(Info) (Info)
When entering an unregistered credential, it’s important to include the hostname or IP of the device to which it’ll be associated.
:::

-  the records will be updated and credentials registered based on spreadsheet info.

-  the existing records will be updated with the information filled in the spreadsheet.