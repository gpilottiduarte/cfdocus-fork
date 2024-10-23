## Metadata_Start 
## code: en
## title: How to manage the master key 
## slug: how-to-manage-the-master-key 
## seoTitle: How to manage the master key 
## description:  
## contentType: Markdown 
## Metadata_End
In this document, you’ll find a step-by-step guide on how to configure the  in senhasegura.

## 

* Have a System Administrator role.

## 

To define the master key, you should follow the steps below:

:::(info) (Info)
 This step is also called the Master Key Ceremony.
:::

1. On senhasegura, in the upper-left corner, click the , represented by nine squares, and select .  
2. In the side menu, select .  
3. When you click on , the  window will open.  
4. In this window, fill in the following fields:  
   1. : indicates the number of parts needed to recover the master key.  
      1. The minimum number of parts is 2, and the maximum is 10\.  
   2. : from the drop-down menu, select the user who should be one of the guardians of the .  
      1. To add more  users, click on the plus sign next to the word  above the  drop-down menu.  
          :::(info) (Info)  
          A recommended practice is to select between two and three times more guardians than key parts.  
         :::  
5. Click on 

:::(warning) (Attention)  
The electronic vault's master key is used to encrypt backup files created by the application. These files are encrypted using the AES algorithm with a 256-bit key and can be decrypted using the AESCrypt application.  
:::

## 

If necessary, you can redefine the . To redefine the , you have two paths:

### 

1. In senhasegura, in the upper left corner, click on , represented by nine squares, and select .  
2. In the side menu, select .  
3. In the  report, click on .

### 

1. On senhasegura, in the upper-left corner, click on , represented by nine squares, and select .  
2. In the side menu, select .

In both cases, the  window will open. When you define a new master key, however, you have an additional session in this window. To redefine the master key, follow the steps below:

1. In the  session:  
   3.  select whether you want to use  or  for your . In this case, the  field is locked.  
   4. : if you choose the  option, you must fill in the  field with the master key's value. In this case, the  field is locked.  
      :::(info) (Info)  
      To access the complete key, you must join the key parts at . For more information, see the Restore master key section at the end of this document.  
      :::  
   5. : if you choose the  option, you must fill in, in this field, which are the parts that make up the . Each part should be placed on a separate line. In this case, the  field is locked.  
2. In the  session you can follow the same instructions on the previous session of this document.  
3. Click on 

### 

* These users will be informed by *email, notification,* or *SMS* that they have been chosen to guard one of the key parts, so it’s important that the selected  have at least their emails registered in the system.  
* The user cannot be the guardian of more than one part of the key.

## 

It is possible to monitor the progress of the Master Key Ceremony. To do this, follow the steps below:

:::(info) (Info)  
To finalize the Master Key Ceremony process, the guardian user must view and/or download the  file containing the master key.  
:::

1. Access, through the side menu,   
2. In the  report, you can follow the process.  
3. The fields are:  
   1. : indicates the name of the user, as registered in senhasegura.  
   2. : indicates the user's phone, as registered in senhasegura.  
   3. : indicates the user's email address.  
      1. It is important that the user has an email registered in senhasegura to receive the guardian notification.  
   4. : indicates the state of the master key ceremony. It can assume the values  or .  
   5. : indicates the user's status within senhasegura. It can assume the values  or .  
   6. : indicates the date and time of the user's last login. It is displayed in the format   
   7. : indicates the date and time of the user's last view in relation to the key part they are guardian of. It is displayed in the format   
   8. : indicates the date and time of the last download made by the user of the key part they are guardian of. It is displayed in the format   
4. On the left side of the report, you find information about the master key ceremony. The information is:  
   1. : indicates the overall status of the ceremony. The status is only completed when all guardian users have viewed and/or downloaded their part of the master key. It can assume the values  or .  
   2. : indicates how many parts are needed for the restoration of the master key.  
   3. : indicates the date and time of the start of the master key ceremony.  
   4. : indicates the date and time of the end of the master key ceremony. If it has not yet been completed, the field will show only .  
   5.  link to define a new master key. Opens the  window to restart the process.

## 

Each guardian should access their account in senhasegura to view their part. If a guardian happens to have an inactive status, the system will report it as an incident via  and *SYSLOG*, displaying an alert message about the guardian's inactive status and suggesting that the master key ceremony procedure be redone.

:::(info) (Info)  
By default, to view a part of the , the  user must have MFA authentication configured. To turn off this requirement, go to  and, in the  section, select  for the option .  
:::

:::(warning) (Attention)  
Disabling MFA authentication for viewing the master key reduces the security of your vault.  
:::

To view a key, as a  user, follow the steps below:

1. On senhasegura, in the upper-right corner, click on the user's name and, in the drop-down menu, select .  
2. In the Master Key window, you have the following fields:  
   1. : indicates the part of the key that the user is a guardian of. It’s informed according to the pattern .  
   2. : indicates the date the part was generated. It is presented in the format .  
   3. : indicates the date and time the query was made. It is presented in the format .  
3. Below the informative fields, there are three buttons:  
   1.  displays the part of which the user is a guardian.  
      1. When clicking on , the  modal is opened. To view the part, slide the  control located at the bottom of the modal.  
   2.  copies the part in question to the clipboard.  
   3. : download the file, in  format, containing the key part.

## 

Once the Master Key Ceremony is finished, it is possible to perform the restoration process. To do this, follow the steps below:

1. Gather the guardians and access the  link.  
2. In the  text field, enter the key parts, obeying the order.

The key parts should be entered as in the example:

`
1-dbfcc9e0fef3542c6fe5494aerr284h 
2-dbfcc9e0fef3542c6fe5494ae45284g
`

3. In the  field, indicate the total number of parts that key has.  
4. In the  field, indicate the number of parts needed to restore the master key.  
5. Click on  to restore the master key.

---

Do you still have questions? Reach out to the .