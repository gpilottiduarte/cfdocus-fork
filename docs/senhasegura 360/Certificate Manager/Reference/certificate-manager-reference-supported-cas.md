# Certificate Authorities plugins 

Currently, senhasegura integrates with the following authorities listed below. 
This article describes the specific configuration fields for each CA plugin.
Info
For further registration information, refer to the article 
How to configure Authorities
.
External authority
Option to manage certificates from authorities not integrated with senhasegura.
Item
Description
Name
External CA identification.
Enabled
It enables the authority to use. Use the 
Yes
 and 
No
 options to confirm the activation or deactivation of the authority.
GlobalSign
Item
Description
Username
GlobalSign username.
Password
GlobalSign password.
Let's Encrypt
Item
Description
Emails (comma separated)
E-mails used to register the Let’s Encrypt account.
Private key password
Let’s Encrypt password.
Use existing account
Checkbox to add the information below.
Private key
Private key value.
Public key
Public key value.
Info
If you don't have a Let’s Encrypt account, you can fill in only the 
Email
 field with a valid account and save the record. Once the record is saved, simply click on 
Edit
 to view the public and private keys generated by senhasegura.
Site Blindado
Item
Description
Username
Site Blindado username.
Password
Site Blindado password.
Use testing API?
Checkbox to test the integration functionality. Use the 
Yes
 and 
No
options
 to confirm the execution. This action will test the integration but doesn't guarantee the certificate's validity.
DigiCert
Item
Description
Username
DigiCert username.
Account ID
DigiCert ID.
API key
DigiCert API key.
GoDaddy
Item
Description
Key
Secret
Requirements for Microsoft CA
Active Directory Certificate Services (AD CS) should be operational on the Windows Server.
WinRM protocol enabled with HTTP or HTTPS. The selected port must match the chosen protocol.
Enable NTLM or NTLMv2 authentication on the Windows Server hosting the certificate authority (CA).
A Windows user account to use as the access credential with:
Administrative privileges on the Windows Server.
Enrollment permissions for certificates on others' behalf in the CA security settings.
Microsoft CA
Item
Description
IP for connection with CA
IP of the Windows Server used as the Certificate Authority.
CA hostname
CA hostname.
Plugin for connection
WinRM plugin.
Port
Port 5985 (HTTP), or 5986 (HTTPS).
Access credential
The access credential registered in PAM to access the Windows machine.
Info
If a Certificate Template hasn’t been defined, senhasegura will utilize the default Certificate Template created by Windows, which is named 'webserver'.
Info
If you use Network Connector to connect to Microsoft, set the default one in 
Settings ➞ System Parameters ➞ System Parameters ➞ Application ➞ Network Connector
. With this setting, you guarantee that it'll be used for the connection at the signing.
Requirements for Entrust 
Integration with PKI Entrust enables the complete management of the certificate lifecycle and operational management across all your Certificate Authorities (CAs).
You must obtain API access keys for your existing PKI CA to access the API. Contact our Entrust operations team through your regular channels.
Info
Currently, RSA-type certificates are supported for signing and the following profiles can be used: 
Web Server Certificate - CSR
SMIME Certificate - CSR
PIV 1-Key Pair - PIV Digital Signature - CSR
Person Network Authentication Certificate - CSR No Directory
ACME Public
PIV 1-Key Pair - PIV Authentication - CSR
PIV 1-Key Pair - PIV Key Management - CSR
PIV 1-Key Pair - Card Authentication  - CSR
Network Authentication Certificate - CSR
People Network Authentication Certificate - CSR
People SMIME Certificate - CSR
Devices Network Authentication Certificate - CSR.
Entrust
Item
Description
Name
External CA identification.
Enabled
It enables the authority for use. Use the 
Yes
 and 
No
 options to confirm the activation or deactivation of the authority. By default, this parameter is set as Yes.
Certificate file
The 
Choose file
 button searches for the certificate file and uploads it.
Key password
Certificate’s password.
Do you still have questions? Reach out to the 
senhasegura Community
.