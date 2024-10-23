## Metadata_Start 
## code: en
## title: How to manage RADIUS servers 
## slug: how-to-manage-radius-servers 
## seoTitle: How to manage RADIUS servers 
## description:  
## contentType: Markdown 
## Metadata_End
RADIUS (Remote Authentication Dial-In User Service) is a network protocol that offers centralized authentication and authorization services for users connecting to and using a network resource. Thus, the RADIUS protocol becomes an alternative to consider when discussing system security, since it allows user credentials to be managed centrally, making it easier to implement strict security policies. senhasegura allows you to use RADIUS servers, all you have to do is configure them within your senhasegura instance.

## Register new server

1. In senhasegura, in the upper-left corner, click the , represented by the nine squares, and select .
2. In the side menu, select .
3. Click on , represented by the three dots, and select .
4. In the  window, fill in the fields:
   1. : IP or hostname of your RADIUS server.
   2. : port on which your RADIUS server is listening.
   3. : select Yes to register your server as active in senhasegura.
   4. : your RADIUS server's secret key.
   5. : enter the timeout time that senhasegura should wait for a response from the RADIUS server.
   6. : enter the maximum number of attempts that senhasegura will make on the RADIUS server.
5. Click on .

## Edit a server

1. In senhasegura, in the upper-left corner, click the , represented by the nine squares, and select .
2. In the side menu, select .
3. In the  report, identify the one you want to change.
4. In the  column, click , represented by the pencil and paper icon.

The  window will open in edit mode. Change the information you want and click .

:::(info) (Info)
If the secret key isn't changed, the current value will be kept in the register.
:::

## Test authentication

On senhasegura, you can test the authentication of your RADIUS server. To do this, follow the steps below:

1. On senhasegura, in the top left corner, click the , represented by the nine squares, and select .
2. In the side menu, select .
3. In the  report, identify the one you want to test authentication on.
4. In the  column, click on the icon of the three vertical dots and select .
5. In the  window, enter the  and  of the user you want to test authentication on.
6. Click .

A message will indicate whether authentication was successful.

---

Do you still have questions? Reach out to the .