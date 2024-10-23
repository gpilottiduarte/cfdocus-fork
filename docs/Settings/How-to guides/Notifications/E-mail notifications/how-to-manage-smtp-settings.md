## Metadata_Start 
## code: en
## title: How to manage SMTP settings 
## slug: how-to-manage-smtp-settings 
## seoTitle: How to manage SMTP settings 
## description:  
## contentType: Markdown 
## Metadata_End
To enable the efficient sending of notifications in an e-mail notification system, it's essential to configure the SMTP (Simple Mail Transfer Protocol) parameters correctly. SMTP is the standard protocol used to send emails over the Internet and requires precise configuration specifications to ensure proper connectivity and security. Initially, you need to define the SMTP server address, which can be provided by your email service provider or your internal infrastructure.

## Setup an SMTP server

1. In senhasegura, in the upper-left corner, click the , represented by the nine squares, and select .  
2. In the side menu, select .  
3. In the  report, click on , represented by the three vertical dots in the top bar, and select  from the drop-down menu.  
4. In the   window, fill in the following fields:  
   1. : fill in the name of your account.  
   2. : select whether you want to create an active account. By default, this option is set to .  
   3. : e-mail address that will be used as the sender.  
   4. : e-mail address that will be used to forward replies to the notification e-mail.  
   5. : e-mail address that will be used to forward notification delivery error messages.  
   6. : e-mail address that will be used to confirm readership  
   7. : select  if you want this account to become senhasegura's default account.  
   8. : select  if you want to receive a read confirmation of the notification email.  
   9. : select  if you want to use the settings in the configuration section  
   10. : select  if you want to enable the footer to be sent with the notification email.  
5. In the  section, fill in the fields:  
   1. : address of the SMTP server for sending e-mail messages.  
   2. : port for listening to the SMTP server.  
   3. : select  if you want to use an encryption method when sending e-mails.  
   4. : select which encryption protocol you want to use:  
      1. : Secure Sockets Layer is an essential security protocol that establishes an encrypted connection between a web server and a browser, ensuring that all data transmitted is kept private and secure.  
      2. : Transport Layer Security is an advanced security protocol that has evolved from SSL to provide even more secure communication between web servers and browsers.  
   5. : select  if you want to use credential authentication for the SMTP server.  
   6. : select  to ignore certificate errors.  
   7. : select  to use the Network Connector to connect to the SMTP server.  
      1. If you select Yes for this option, you must select the  you want to use by selecting it from the  drop-down menu next to the option.  
         1. You must have a previously configured Network Connector.  
   8. : select a credential to use to authenticate yourself to the SMTP server.  
      1. Note that if you have selected  for the  field, you must choose a credential in this option.  
6. Click on .

## Edit an SMTP server

You can change the settings of an SMTP server previously registered with senhasegura. To do this, follow the steps below:

1. In senhasegura, in the upper-left corner, click the , represented by the nine squares, and select .  
2. In the side menu, select .  
3. In the  report, in the  column, click , represented by the pencil and paper icon.  
4. The   window will open in edit mode.  
5. Change the information you want and click .

## Test the configuration of an SMTP server

You can test the configuration of an SMTP server to ensure that it is correctly configured. To do this, follow the steps below:

1. In senhasegura, in the upper-left corner, click the , represented by the nine squares, and select .  
2. In the side menu, select .  
3. In the  report, in the  column, click on the three vertical dots and select  from the drop-down menu.  
4. In the  window, fill in the fields:  
   1. : fill in the e-mail address to which you want to send the test e-mail.  
   2. : fill in the subject of the test message. By default, this field is filled in with the string   
   3. Message: fill in the test message you want to send. By default, this field is filled with the string   
5. Click .

***

Do you still have questions? Reach out to the .