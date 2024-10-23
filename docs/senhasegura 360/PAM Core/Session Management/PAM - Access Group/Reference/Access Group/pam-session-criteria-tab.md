## Metadata_Start 
## code: en
## title: Criteria tab 
## slug: pam-session-criteria-tab 
## seoTitle: Criteria tab 
## description:  
## contentType: Markdown 
## Metadata_End
In this document, you’ll find all the information about the  tab from the registration screen for a new access group. In this section, it’ll be decided which devices and credentials the group's users can access.

:::(info) ()
To find out how to register an access group, access the  document.
:::

### Path to access

1. On senhasegura, in the upper-left corner, click the , represented by the nine squares, and select .
2. In the side menu, select  >  >  > .
3. Or on the list select the group that you desire to edit, by clicking on the pencil and paper icon.

---

## Access group registration - Criteria

|
---|---
|Device registration name. In the text  there are possible ways to fill in this field.
|Device model.
|Credential username. In the text  there are possible ways to fill in this field.
|Text with additional information about registration.
|Tags registered for devices.
|Tags registered for credentials.
*|Checkbox to select the types of sites that will be visible to the group. The options are: *All* and *Default*.
*|Checkbox to select the types of devices that will be visible to the group. The options are defined according to the types of registered devices.
*|Checkbox to select the types of credentials that will be visible to the group. The options are: *All, SSH Key, Domain Admin, Domain User, Local User* and *Local administrator*.

### Device field
The  field can be filled with some combinations that facilitate the choice of devices that will be available for that access group.

The combinations are:

* The device’s name plus the device IP number. For example: , the group will be able to device which has exactly that name and IP.
* One asterisk at the beginning plus a part that contains the device’s name plus an asterisk at the end. For example:  will be available to the group the device that contains the word device  in the name.
* The beginning of the device’s name plus an asterisk at the end. For example:  will be available to the group the device that contains the word device at the  of the name.
* The beginning of the device’s name with an asterisk in the middle and the end of the device name. For example:  will be available to the group the device that starts with  in the name, has some  and ends the name with the word .

### Username field
When the credential’s username matches the senhasegura’s username, you can use the mask  to ensure that only visible credentials are those with the same senhasegura’s login username.

For example, the username used to access the senhasegura instance is , and the group rule will be that only John will have access to credentials with the same username, which means, only credentials in which the credential's username is also .

For this to be possible, the following syntax will be used to fill the field:

*  which will bring only the credentials that have exactly the name of john.
*  which will bring all the credentials that have john at the beginning, regardless of how the ending turns out.
*  which will bring all the credentials that have john in the middle of the credential name, regardless of how the beginning and the end are.

To understand more about senhasegura Access groups, access the .

