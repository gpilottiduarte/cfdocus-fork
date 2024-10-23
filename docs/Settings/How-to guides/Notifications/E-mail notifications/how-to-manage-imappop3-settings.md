## Metadata_Start 
## code: en
## title: How to manage IMAP/POP3 settings 
## slug: how-to-manage-imappop3-settings 
## seoTitle: How to manage IMAP/POP3 settings 
## description:  
## contentType: Markdown 
## Metadata_End
To manage e-mails efficiently in a system, it's essential to configure the IMAP (Internet Message Access Protocol) or POP3 (Post Office Protocol 3\) protocols correctly. These protocols are responsible for communication between the e-mail client (such as a web browser or e-mail application) and the e-mail server, allowing e-mails to be received, organized, and accessed.

IMAP allows e-mails to be synchronized across multiple devices, with the inbox being accessed simultaneously from different locations. POP3, on the other hand, downloads e-mails to the device and deletes them from the server. This can be useful for users who prefer to access their e-mails offline or who want a local copy of all their e-mails.

Setting up IMAP or POP3 requires information such as the server address, username, and password, as well as checking compatibility with the latest version of the protocol and the availability of security, such as SSL/TLS. The choice between IMAP and POP3 depends on the user's needs, since IMAP synchronizes e-mails on multiple devices, while POP3 downloads e-mails to the device, deleting them from the server, ideal for offline access or local copying.

## Configure an IMAP/POP3 account

1. In senhasegura, in the upper-left corner, click the , represented by the nine squares, and select .  
2. In the side menu, select   
3. In the  report, click on , represented by the three vertical dots in the top bar, and select  from the drop-down menu.  
4. In the  window, fill in the following fields:  
   1. : fill in the name of your account.  
   2. : select  to keep a copy on the server or  to delete the message from the server as soon as it is downloaded to senhasegura.  
   3. : select  to perform automatic verification of new messages or  to perform verification manually only.  
   4. : select whether you want to create an active account. By default, this option is set to .  
5. In the  section, fill in the fields:  
   1. : host's imap/pop3 address.  
   2. : the host's IMAP or POP3 listening port.  
   3. : drop-down menu. Choose which server you want to use:  or .  
   4. : select  to use the Network Connector to connect to the incoming message server.  
      1. If you select  for this option, you must select the  you want to use by selecting it from the  drop-down menu next to the option.  
      2. You must have a previously configured Network Connector.  
   5. : select the credential that will be used to authenticate yourself on the message receiving server.  
   6. : ignores the server's certificate. This is set to  by default.  
   7. : use a secure connection to the server. By default, this is set to .  
   8. : indicate the security protocol that will be used for the connection:  or .  
6. Click .

## Edit an IMAP/POP3 account

You can edit the settings of an IMAP/POP3 account previously registered with senhasegura. To do this, follow the steps below:

1. On senhasegura, in the upper-left corner, click the , represented by the nine squares, and select .  
2. In the side menu, select .  
3. In the  report, in the  column, click , represented by the pencil and paper icon.  
4. The  window will open in edit mode.  
5. Change the information you want and click .

## View the inbox of an IMAP/POP3 account

To view the inbox of just one account, follow the steps below:

1. On senhasegura, in the upper-left corner, click the , represented by the nine squares, and select .  
2. In the side menu, select .  
3. In the  report, in the  column, click on the three vertical dots and select  from the drop-down menu.  
4. You will be taken to the  report, containing all incoming messages.

***

Do you still have questions? Reach out to the .