## Metadata_Start 
## code: en
## title: How to manage TACACS servers 
## slug: how-to-manage-tacacs-servers 
## seoTitle: How to manage TACACS servers 
## description:  
## contentType: Markdown 
## Metadata_End
TACACS (Terminal Access Controller Access-Control System) is a remote authentication protocol to communicate information between a network server and a client. Originally developed by Cisco Systems, the protocol controls access to terminals and network services, allowing system administrators to restrict user command options. TACACS allows passwords to be managed centrally, which is ideal for systems that access many network devices.

senhasegura allows you to use TACACS servers to authenticate yourself simply by configuring them within your senhasegura instance.

## Register a new server

1. On senhasegura, in the upper left corner, click the , represented by the nine squares, and select .
2. In the side menu, select .
3. Click on , represented by the three dots, and select .
4. In the  window, fill in the fields:
   1. : IP or hostname of your TACACS server.
   2. : port on which your TACACS server is listening.
   3. : select Yes to register your server as active in senhasegura.
   4. : your TACACS server's secret key.
   5. ): Enter the timeout time that senhasegura will wait for a response from the TACACS server.
   6. : enter the maximum number of attempts that senhasegura will make on the TACACS server.
5. Click on .

## Edit a server

1. On senhasegura, in the upper left corner, click the , represented by the nine squares, and select .
2. In the side menu, select .
3. In the  report, identify the one you want to change.
4. In the  column, click , represented by the pencil and paper icon.

The  window will open in edit mode. Change the information you want and click .

:::(info) (Info)

If you don't change the secret key, the current value will be kept in the register.

:::

## Test authentication

In senhasegura, you can test the authentication of your TACACS server. To do this, follow the steps below:

1. On senhasegura, in the upper-left corner, click the , represented by the nine squares, and select .
2. In the side menu, select .
3. In the  report, identify the one you want to test authentication on.
4. In the  column, click on the icon represented by the three vertical dots and select .
5. In the  window, enter the  and  of the user you want to test authentication.
6. Click on .

A message will indicate whether authentication was successful.

---

Do you still have questions? Reach out to the .