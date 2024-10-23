## Metadata_Start 
## code: en
## title: How to manage SSH keys 
## slug: pam-how-to-manage-ssh-keys 
## seoTitle: How to manage SSH keys 
## description:  
## contentType: Markdown 
## Metadata_End
This document provides details on how to check registered SSH keys.

## How to access SSH keys

1. In the top left corner, click the , indicated by the nine-square box, and select .
2. In the side menu, select .

## Operations for SSH keys

In the  column, click the icon identified by the three vertical dots and select the desired operation:

1. : start a remote session with the registered key.
2. : access to view, copy, or download the keys.
3. : edit the SSH key settings information as desired.
4. : access to view, copy, or download the keys.
5. : shows a history of operations performed on the SSH key.
6. : inactivates the SSH key.

By clicking the  option, a pop-up window will open with the following details of the SSH key, divided into sections:

### Details tab

#### General

-  name of the user of this SSH key.
- : type of SSH key.
-  expiration date of the SSH key.
- : the SSH key date of creation.
- : date of change of the SSH key; if no change has occurred, this field is blank.
- : date of the last SSH key query.

#### Device

-  hostname of the device that the SSH key connects to.
- : IP or hostname that the switch manages.
- : manufacturer of the device.
- : type of device.
- : device model.
- : connection protocol of the switch to the device.

#### Change configuration

- : informs whether the switch has automatic swapping enabled or not.

#### Policy

- : name of the policy used.
- : can be one of the three available values: *Low, Default or High*.
- : how long the key is valid.
- : how long the password is available for a query before it’s automatically changed.
- : indicates whether the key can be viewed by more than one user at the same time.
- : indicates whether the key can be used to access more than one device at the same time.

:::(Info) (Info)
Please note that the option to view a password will be available for 30 seconds after clicking  button.
:::

### Overview tab

In the overview tab, you can view various information about the SSH key divided into cards along the interface.

- : indicates the period (time) of greatest usage of that key.
- : shows if this SSH key has a parent credential.
- : the number of times the SSH key has been viewed.
- : total number of accesses made with the SSH key.
- : average duration of sessions using this SSH key.
- : number of devices on which the SSH key is used.
-  indicates a pie chart showing the access groups to which this SSH key is linked.
- : indicates a pie chart showing how many users have access to this SSH key.
- : shows a timeline indicating the actions on the SSH key consulted. The timeline details the action, the day and time, and the user who performed the action.
- : indicates the last accesses made by the SSH key.
- : indicates which user has custody of the SSH key.
- : indicates which devices are associated with this SSH key.

### Top bar

Use the top bar of the SSH Key window to quickly obtain information about the key and for quick actions.

The top bar of the window contains the following information:

- : name of the user who owns the SSH key.
- : type of user. It can be one of three types: *Local User, Local Administrator, or Domain User*.
- : indicates the device associated with the SSH key.
- : indicates the status of the SSH key. It can be  or .
- : shortcuts to the main actions that can be performed with the SSH key:
    - : represented by the arrow icon towards the right, which allows you to start a session on the indicated device.
    - : represented by the key icon, allows you to view the key's information. Note that viewing a key gives you custody of it.
    - : represented by the pencil and paper icon, allows you to edit all the SSH key settings.
    - : represented by the clock icon, this allows you to view the key's history. This history allows you to view the executions on the key, who carried them out, and the date they were carried out.
    - : represented by the trash can icon, this allows you to inactivate the SSH key.

***
Do you still have questions? Reach out to the .