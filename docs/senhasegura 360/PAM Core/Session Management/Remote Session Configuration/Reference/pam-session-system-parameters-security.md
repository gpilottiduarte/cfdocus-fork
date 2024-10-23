## Metadata_Start 
## code: en
## title: System parameters - Security 
## slug: pam-session-system-parameters-security 
## seoTitle: System parameters - Security 
## description:  
## contentType: Markdown 
## Metadata_End
This document contains detailed information about the  page, where you can configure the features from .

***
## Path to access

1. On senhasegura, in the upper left corner, click , represented by the nine squares icon, and then select .
2. In the side menu, select  >  > .
***

:::(warning) ()
All fields are set with a default value, as recommended by senhasegura. However, you can customize your session according to your needs.
:::

### Security tab
|
|---|---|
*|Forces the multifactor authentication to view a password. Default option: .
|Defines the time interval in which tokens must be requested for password display. It can be 0 until 60 minutes. Default option: .
*|Indicates if the checkbox displayed when logging into the senhasegura environment should be disregarded for examining passwords. Default option: .
*|Forces the user to use the 2FA token to start proxy sessions. Default option: .
|Defines the time interval in which tokens must be requested to perform a session. Choose from 0 to 60 minutes. Default option: .
*|Indicates whether the checkbox displayed when logging into the senhasegura environment should be disregarded for examining passwords. Default option: .
*|Forces the use of a secure connection during the password change. Default option: .
*|Determines whether senhasegura will change the password right after the proxy session starts. Default option: .
*|Forces a session to be authenticated by a digital certificate when connecting through RDP Proxy. Default option: .
*|Forces a session to be authenticated by a digital certificate when connecting through SSH/Telnet Proxy. Default option: .
*|Indicates the security level of target RDP connections. Can be *Automatic*, *RDP*, *NLA*, or *TLS*. By default,  is set. With this setting, the client and server will determine the level of security. Since it functions as a bridge, the client in this scenario is the senhasegura platform. To adjust the security level of incoming connections to senhasegura, refer to the RDP Proxy documents.
*|Defines the idle session duration that will trigger an automatic disconnection. You can select a duration between Minutes, Hours, and Days. The number can be 0 to 60. Default option: .
|Enables a filter based on the IP address that controls the IP address that has permission to start proxy sessions. Default option: .
|If  is active, you can determine a list of IPs, individual or at intervals, that will be allowed to start a proxy session. Default option: .


### At Encryption section
:::(info) ()
Note that you must select an HSM device, only if you set the * to .
:::
|
|---|---|
*|Indicates if the encryption mode will be Default or HSM. Default option: .
|Selects the hardware device used to manage the encryption keys.

