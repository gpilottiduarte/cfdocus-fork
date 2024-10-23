## Metadata_Start 
## code: en
## title: Batch import template file 
## slug: batch-import-template-file 
## seoTitle: Batch import template file 
## description:  
## contentType: Markdown 
## Metadata_End
## Path to access

1. On senhasegura, in the upper-left corner, click the , represented by the nine squares, and select .  
2. In the side menu, select  and click on the  button in the bottom-right corner.

## Template file

Within the file, each line corresponds to a new group that will be imported. The information that must be entered in the file is the same as that entered via group registration on the senhasegura web interface.

| Item  | Description |
| :---- | :---- |
|  | Name of the Active Directory group. For example:  |
|  | Server address. For example:  |
|  | Defines whether the group will be active or inactive. It can be set to "Sim" or "Nao" |
|  | Defines whether synchronization with senhasegura will be activated. It can be set to "Enabled” or "Disabled”. |
|  | Address of AD elements that will serve as the basis for querying and synchronizing senhasegura. For example:  |
|  | User name attribute. For example:  |
|  | AD user name attribute. For example: . |
|  | Field for department. For example:  |
|  | Query parameters to retrieve information from AD. For example: . |
|  | AD roles. For example: . |
|  | Access groups with user roles. For example: .  if the access group has the level approval enabled, level 1 will always be considered. |
|  | Access groups with approver function. For example: .   if the access group has level approval enabled, level 1 will always be considered. |