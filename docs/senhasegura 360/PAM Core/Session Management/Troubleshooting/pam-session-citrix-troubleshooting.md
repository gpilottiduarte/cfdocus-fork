## Metadata_Start 
## code: en
## title: Citrix - Troubleshooting 
## slug: pam-session-citrix-troubleshooting 
## seoTitle: Citrix - Troubleshooting 
## description:  
## contentType: Markdown 
## Metadata_End
In this document, you’ll find a step-by-step guide on how to check and resolve possible problems related to .

---
### The desktop you want to connect is unavailable

: Citrix XenApp Application Launch Error: The desktop you want to connect to is currently unavailable. Please try later or contact an administrator if the problem persists.
: Verify that the application server is running or that there are no stuck sessions. In Citrix, access Delivery Groups, and (if you have sessions in use) double-click on the delivery group, select the session and click on the Log Off option.

---
### Unable to connect to "192.168.1.1 - AppName"

: Unable to connect to "192.168.1.1 - AppName". No file or directory. Check your connection settings and try again
: Check the network connection between the Bridge Server and the application server.

---
### Unable to connect to remote server URL

: Citrix XenApp - Cannot Contact the Citrix Server: Unable to connect to remote server URL . The remote server URL may have been entered incorrectly or the remote server may be down. Do you want to re-enter the server URL?
: Check the connection between the Citrix Bridge Server and Citrix Store. You can try using the IP address instead of the store's hostname. For example: 

---
### Remote Desktop Server encountered an error

: The Remote Desktop server encountered an error and closed the connection. Please try again or contact your system administrator.
: Check if the Docker container is running: . If not, start it using the following command: .

---
### Can’t transfer files

: the option to transfer files is not working.
: check if you have installed Fuse module on Bridge Server Linux. If you have installed the Fuse module, make sure it’s running, type:  or start it by typing: .

---
Do you still have questions? Reach out to the .