## Metadata_Start 
## code: en
## title: How to configure a device 
## slug: pam-devices-management 
## seoTitle: Configure a device 
## description:  
## contentType: Markdown 
## Metadata_End
For the proper functioning of the solution, a correct registration of the devices is essential. Discrepancies can affect the behavior of the software.

You have two ways to access the  configuration area. To do so, follow the steps below:

1.  in the toolbar, ath the top of the senhasegura platform, click the icon represented by a sheet of paper with the sum sign and select . This action will load a pop-up window witht the  form.
2.  in the top left corner, click the icon represented by a box of nine squares, and select .

In case you select the , you'll need to select  on the side menu. To do this, proceed as follows:

1. Select, on the side menu,  to load the list of devices. 
2. Click on the  icon, identified by the three vertical dots, and select .

A pop-up window will show the  form with the data to be filled in to register a new device in the senhasegura platform.

## How to configure devices

Fill in the following data to configure a new device:

### Information's tab

1.  fill in the address to which the device is registered and accessible.
2.  fill in with a name for internal use.
3.  select desired type.
4.  select relevant manufacturer.
5.  select device model.
6.  select the division/local this device belong to.
7.  fill in the desired tags.

In the  session, select the desired domain. To add other domains, click on the  icon, identified by the sum symbol.

:::(Info) (Info)
The fields , , , and  can be registered directly on the device enrollment screen if the entered value doesn't exist.

All device registration, modification, and inactivation operations are sent via .
:::

:::(Warning) (Important)
Changes and deactivations may affect access to devices and credentials.
:::

### Connectivity's tab

1.  select the required network connector.
2.  select the type of connection (HTTP, Telnet, VNC, etc.).
3.  fill in the port for communication.

:::(Info) (Info)
Connectivity tests are performed via TCP socket. It's possible to configure the platform to use the device with two applications and the same protocol, but you must configure different ports.
:::

:::(Warning) (Important)
When the default port is modified, the change is reflected only on the specific device being edited.
:::

### Additional settings' tab

1.  select the degree of criticality (*High, Medium, or Low*).
2.  add regular expressions to handle custom authentications.
3. Click the  button.

:::(Info) (Info)
It's recommended to use protocols with encryption support if possible.
:::

:::(Info) (Info)
In case you need a more detailed explanation about the items of devices, you can access the  documentation.
:::

## Next
1. 
2. 
3. .
4. .
5. .
6. .

***

Do you still have questions? Reach out to the .