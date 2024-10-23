## Metadata_Start 
## code: en
## title: Certificate Manager 
## slug: a2a-api-certificate-manager 
## seoTitle: A2A Certificate Management 
## description:  
## contentType: Markdown 
## Metadata_End
:::(warning) (Caution)
To use these methods the  resource must be selected in the application authorization.
:::

## Introduction

The senhasegura  provide centralized management of the digital certificate lifecycle within the organization, from Discovery through automatic scanning of websites, directories and web servers, to automated Certificate renewal through external or internal Certificate Authorities.

The purpose of this document is to provide guidance for users using Certificate Manager administrator roles, and to discuss details about their use, benefits, concepts, and procedures.

### How the Certificate Manager works

senhasegura Certificate Manager manages the entire digital Certificate lifecycle, working with Certificate through request generation, manual importation of existing Certificates, or Discovery of Certificates across Devices, Domains or Containers. In addition to monitoring certificate validity and facilitating renewal, Certificate Manager also allows you to view logs and reports on all operations performed through the solution.

### Definitions

The senhasegura uses specific terminology for its functions and features. Thus, some terms must be understood before starting to use the solution:

-    Own employees, interns or third parties who use or may need access to company systems;

-    Digital certificates are files that contain public and private key information that is used for secure communication over the Internet, as well as to certify the sender's authenticity

-    Certification Authority is an entity duly registered with the responsible bodies and which has the function of issuing digital certificates.

### Activities

In this section, the following senhasegura functions will be covered: make requests, receive answers and senhasegura Certificate Manager method.

## Method

The senhasegura integration webservice has some methods to query, create or change information stored in the application.

### Create / Modify a Request

 
` 
POST https://vault_url/iso/certificate/request/\[request_code\] 
` 
The  method creates or modifies a certificate request in senhasegura

#### Parameters

|  |  Type |  Description |  Required |
| --- | --- | --- | --- |
|  |  Int |  Code of an already created request. If the code is not included in the parameter, a new Request will be created. |  No |
|  |  Int |  Type of certificate. The possible values are: 1 = DV SSL - Domain SSL; 2 = OV SSL - Organization SSL; 3 = EV SSL - Extended SSL |  Yes | 
|  |  String |  Type of the certificate domain. The possible values are: SING = Single domain; MULT = Multiple domains; WILD = Wildcard |  Yes |
|  |  Int |  Code of the organization. The code of an organization registered in senhasegura must be informed. |  Yes |
|  |  String |  Certificate common name |  Yes |
|  |  Array |  Subject Alternative Name. It will be filled with common_name if san is not informed. |  No |
|  |  Array |  Certificate identification tags. New tags will be registered if the reported ones do not exist |  No |
|  |  String |  encryption. The possible values are: RSA ; DSA |  Yes | 
|  |  Int |  Size of the encryption key. The possible values are: 4096; 2048; 1024 |  Yes | 
|  |  String |  Signature Algorithm. The possible values are: SHA256; SHA384; SHA512. If the encryption chosen is DSA, then only SHA256 may be used. |  Yes |  
|  |  Int |  Certificate validity time, in days. |  Yes |
|  |  String |  Password of the certificate key. |  No |
|  |  String |  Certificate revocation password. |  No |
|  |  Array |  Certificate environments. New certificate environments will be registered if the informed ones do not exist. |  No |
|  |  Array |  Certificate systems. New certificate systems will be registered if the informed ones do not exist. |  No |
|  |  String |  Certificate project in request. |  No |
|  |  String |  External IP of the certificate in the request. |  No |
|  |  String |  IP or certificate hostname in request. |  No |
|  |  String |  Request justification of up to 1024 characters. |  No |
|  |  Int |  Code of the requester and the certificate. Must be a registered username account in senhasegura . |  No |
|  |  String |  Description of the request up to 512 characters. |  No |

#### Response to certificates

If the method succeeds or fails, the response consists of a certified block with the fields:

|  |  Type |  Success |  Error |
| --- | --- | --- | --- |
|  | Int | OK | 4xx |
|  | Text | Created | Could not create request | 
|  |  boolean |  false |  true |
|  |  Int |  Request code. |  The request code entered is invalid |
|  | Int |  Type of the entered certificate. |  The certificate type you entered is invalid. |
|  |  String |  Type of certificate domain entered. |  The certificate domain type you entered is invalid. |
|  |  Int |  Organization code entered. |  The organization code you entered is invalid |
|  |  String |  Common name entered. |  Certificate common name not entered |
|  |  Array |  SAN informed. |  |
|  |  Array |  Tags informed. |  |
|  |  String |  Encryption Algorithm entered. |  Encryption algorithm entered is invalid |
|  |  Int |  Size of encryption key entered. |  The encryption key length entered is invalid. |
|  |  String |  Signature Algorithm entered. |  The signature algorithm entered is invalid. |
|  |  Int |  Expiry time of the entered certificate. |  Invalid certificate expiration time. |
|  |  String |  Sensitive Information. |  Password for certificate key entered is invalid. |
|  |  String |  Sensitive Information. |  The certificate revocation password you entered is invalid. |
|  |  Array |  Informed Environments. |  |
|  |  Array |  Informed Systems. |  |
|  |  String |  Design informed. |  |
|  |  String |  IP entered. |  |
|  |  String |  IP or hostname entered. |  |
|  |  String |  Informed Justification. |  Justification must be a maximum of 1024 characters. |
|  |  Int |  Responsible Code informed. |  The parental code you entered is invalid. |
|  |  String |  Description entered. |  Description must be a maximum of 512 characters. |

### Query / List Request

 
` 
GET https://vault_url/iso/certificate/request/list\[request_code\] 
` 
The  method queries one or more certificate requests in senhasegura.

#### Parameters

|  |  Type |  Description |  Required |
| --- | --- | --- | --- |
|  |  Int |  Code of an already created Request. |  No |
|  |  Int |  Code of a status of a request. |  No |
|  |  Int |  Type of certificate. The possible values are: 1 = DV SSL - Domain SSL; 2 = OV SSL - Organization SSL; 3 = EV SSL - Extended SSL** |  No | 
|  |  String |  Type of certificate domain. The possible values are: SING = Single domain; MULT = Multiple domains; WILD = Wildcard |  No | 
|  |  Int |  Code of the organization registered in senhasegura. |  No |
|  |  String |  Common name of certificate. |  No |
|  |  String |  Subject Alternative Names, separated by comma |  No |
|  |  String |  Certificate ID tags, comma separated |  No |
|  |  String |  Encryption algorithm. The possible values are: RSA, DSA |  No |
|  |  Int |  Size of encryption key. The possible values are: 4096, 2048, 1024 |  No | 
|  |  String |  Signature algorithm. The possible values are:SHA256, SHA384, SHA512 |  No |  
|  |  Int |  Certificate validity time in days. |  No |
|  |  String |  Certificate key password. |  No |
|  |  String |  Certificate revocation password. |  No |
|  |  String |  Certificate Environments, Comma Separated |  No |
|  |  String |  Certificate Systems, Comma Separated |  No |
|  |  String |  Certificate Design on request. |  No |
|  |  String |  external certificate IP on request. |  No |
|  |  String |  IP or certificate hostname on request. |  No |
|  |  Int |  Code of the responsible for the request and the certificate. |  No |
|  |  Int |  Base number of record count by pagination. |  No |
|  |  Int |  Number of records in pagination. |  No |

#### Response to certificate

If the method succeeds or fails, the response consists of a certified block with the fields:

|  |  Type |  Success |  Error |
| --- | --- | --- | --- |
|  | Int | OK |  4xx |
|  | Text | Created |  Could not find requests with the information provided |
|  |  |  false |  true |
|  |  Int |  Request Code. |  There is no request with the given code. The request code you entered is invalid. |
|  |  String|  Request status code and name. |  There are no requests with the status entered. The status code you entered is invalid. |
|  |  Int |  Type of certificate entered. |  There are no requests with the type of certificate entered. The certificate type you entered is invalid. |
|  |  String |  Type of certificate domain entered. |  There are no requests with the domain type you entered. The certificate type domain you entered is invalid. |
|  |  Int |  Organization code entered. |  There are no requests with the organization code entered. The organization code you entered is invalid. |
|  |  String |  Common name entered. |  There are no requests with the given common name. |
|  |  Array |  SAN informed. |  There are no requests with the informed SAN. |
|  |  Array |  Tags entered. |  There are no requests with the given Tag. |
|  |  String |  Encryption algorithm entered. |  There are no requests with the encryption algorithm entered. The encryption algorithm entered is invalid. |
|  |  Int |  Encryption key size entered. |  There are no requests with the encryption key size entered. The encryption key length you entered is invalid. |
|  |  String |  Signature Algorithm entered. |  There are no requests with the signature algorithm entered. The signature algorithm you entered is invalid. |
|  |  Int |  Certificate expiration time entered. |  There are no requests with the expiration date entered. Invalid certificate expiration time is invalid. |
|  |  String |  Sensitive Information. |  There are no requests with the password of the entered key. The certificate key password you entered is invalid. |
|  |  String |  Sensitive Information. |  There are no requests with the revocation password entered. The certificate revocation password you entered is invalid. |
|  |  Array |  Informed environments. |  There are no requests with the informed environments. |
|  |  Array |  Informed systems. |  There are no requests with the informed systems. |
|  |  String |  Project entered. |  There are no requests with the project entered. |
|  |  String |  IP entered. |  No requests with external IP entered. |
|  |  String |  IP or hostname entered. |  No requests with IP or hostname entered |
|  |  String |  Informed Justification. |  |
|  |  Int |  Code and name of the informed responsible. |  There are no requests with the informed responsible’s code.The responsable’s code you entered is invalid. |
|  |  String |  Description entered. |  |

### Sign Request

 
` 
GET https://vault_url/iso/certificate/request/sign\[request_code\] 
` 
The  method signs an existing request in senhasegura .

#### Parameters

|  |  Type |  Description |  Required |
| --- | --- | --- | --- |
|  |  Int |  Code of request to be signed. |  Yes |
|  |  Int |  Indicates whether it is self-signed. The options will be: 1 = true, 0 = false |  Yes |  
|  |  Int |  CA Code responsible for signing request. Required if self_signed is false. |  Conditional |
|  |  String |  Text up to 1024 characters for justification. |  No |
|  |  Int |  Subscription Reason Code. You should enter a reason code for a reason entered in senhasegura. |  Yes |
|  |  String |  characters to determine ITSM code. Required if in the certificate access group the parameter "Governance code required when justifying" is enabled. Perform ITSM validations in the same way as the web interface. | Conditional |

#### Response to certificate

If the method succeeds or fails, the response consists of a certified block with the fields:

|  |  Type |  Success |  Error |
| --- | --- | --- | --- |
|  | Int | OK |  4xx |
|  | Text | Created |  Could not sign request. |
|  |  |  false |  true |
|  |  Int |  Request Code. |  Enter a request code.The request code you entered is invalid |
|  |  Int |  Value entered. |  There are no requests for this entered self-signed value.The value for self-signed entered is invalid. |
|  |  Int |  CA code and CA name entered. |  There are no requests with the CA code entered. The CA code you entered is invalid. |
|  |  String |  Informed Justification. |  Justification must be a maximum of 1024 characters |
|  |  Int |  Reason code and name entered. |  Reason code entered is invalid. |
|  |  String |  ITSM code entered. |  Enter the ITSM code. |

### Query / List Certificates

 
` 
GET https://vault_url/iso/certificate/list/\[request_code\] 
` 
The  method queries one or more certificates in senhasegura.

#### Parameters

|  |  Type |  Description |  Required |
| --- | --- | --- | --- |
|  |  Int |  Code of a certificate already created in senhasegura. |  No |
|  |  Int |  Code of a status of a certificate. The options will be: 1 = Valid; 2 = Revoked; 3 = Renewal pending; 4 = Expired |  No |  
|  |  Int |  Certificate Status on senhasegura . The options will be: 1 = Active, 0 = Inactive |  No |  
|  |  String |  Expiry start date |  No |
|  |  String |  Expiry date |  No |
|  |  Int |  Certificate origin on senhasegura . The options will be: SCAN = Scan and Discovery; REQU = Request; IMPO = Imported manually |  No | 
|  |  Int |  Type of certificate. The options will be: 1 = DV SSL - Domain SSL; 2 = OV SSL - Organization SSL; 3 = EV SSL - Extended SSL |  No | 
|  |  String |  Type of certificate domain. The options will be: SING = Single domain; MULT = Multiple domains; WILD = Wildcard |  No |  
|  |  Int |  Organization code. |  No |
|  |  String |  Common name of certificate. |  No |
|  |  String |  Subject Alternative Name. You may enter more than 1 separated by a comma. |  No |
|  |  String |  Certificate ID Tags. You may enter more than 1 separed by comma. |  No |
|  |  String |  Encryption Algorithm. The options will be: RSA, DSA |  No |  
|  |  Int |  Size of encryption key. The options will be: 4096, 2048, 1024 |  No |  
|  |  String |  Signature Algorithm The options will be: sha256, sha384, sha512 |  No |  
|  |  Int |  Certificate validity time in number of days. |  No |
|  |  String |  Password of certificate key. |  No |
|  |  String |  Certificate revocation password. |  No |
|  |  String |  Certificate Environments. You may enter more than 1 separated by commas. |  No |
|  |  String |  Certificate Systems. You may enter more than 1 separated by commas. |  No |
|  |  String |  Certificate project on request. |  No |
|  |  String |  external certificate IP on request. |  No |
|  |  String |  IP or certificate hostname on request. |  No |
|  |  Int |  Indicates whether it is self-signed. The options will be: 1 = true; 0 = false |  No | 
|  |  Int |  CA Code responsible for signing request. |  No |
|  |  Int |  Code of the responsible for the request and the certificate. |  No |
|  |  Int |  Base number of record count by pagination. |  No |
|  |  Int |  Number of records in pagination. |  No |

#### Response to certificates

If the method succeeds or fails, the response consists of a certified block with the fields:

|  |  Type |  Success |  Error |
| --- | --- | --- | --- |
|  | Int | OK  |  4xx |
|  | Text | Created |  Could not sign request. |
|  |  |  false |  true |
|  |  Int |  Request Code. |  Enter a request code.The request code you entered is invalid |
|  |  Int |  Code and name of certificate status |  There are no certificates with the entered status. The status code you entered is invalid. |
|  |  Int |  Code and name of the certificate status on senhasegura |  There is no certificate with the entered state. The state code you entered is invalid. |
|  |  String |  Expiry start date |  There are no certificates with the stated expiration date. The expiration start date you entered is invalid. |
|  |  String |  Expiry date |  There are no certificates with the stated expiration date. The expiration date entered is invalid. |
|  |  Int |  Certificate origin in senhasegura |  There are no certificates with the informed source. The source you entered is invalid. |
|  |  Int |  Type of certificate |  There are no certificates of the type entered. The certificate type you entered is invalid. |
|  |  String |  Type of certificate domain |  There are no certificates with the domain type you entered. The certificate type domain you entered is invalid. |
|  |  Int |  Code and name of the organization you entered |  There are no certificates with the organization code entered. The organization code you entered is invalid |
|  |  String |  Common name of certificate |  There are no certificates with the common name entered. |
|  |  Int |  Size of the certificate encryption key |  There are no certificates with the encryption key length entered. The encryption key length you entered is invalid. |
|  |  String |  Certificate Signing Algorithm |  There are no certificates with the signature algorithm entered.The signature algorithm you entered is invalid. |
|  |  Int |  Certificate validity time |  There are no certificates with the entered expiration time. Invalid certificate expiration time is invalid. |
|  |  String |  Certificate key password. |  There are no certificates with the entered key password. The certificate key password you entered is invalid. |
|  |  String |  Certificate revocation password. |  There are no certificates with the revocation password entered. The certificate revocation password you entered is invalid. |
|  |  String |  Certificate Environments |  There are no certificates with the environment (s) entered. |
|  |  String |  Certificate Systems |  There are no certificates with the system (s) entered. |
|  |  String |  Certificate Design. Eg project 1 |  There are no certificates with the project informed. |
|  |  String |  external certificate IP. |  No certificates with external IP entered. |
|  |  String |  IP or certificate hostname |  There are no certificates with the given IP or hostname. |
|  |  Int |  Info if the certificate is self-signed |  No certificates exist for this self-signed value entered. The value for self-signed entered is invalid. |
|  |  Int |  CA code and CA name entered |  There are no certificates with the CA code you entered. The CA code you entered is invalid. |
|  |  Int |  Code and name of responsible person informed |  There are no certificates with the responsible’s code entered. The responsible’s code you entered is invalid. |
|  |  |  Description of the certificate |  |
|  |  | Additional information for publication |  |
|  |  | Devices code attached with certificate |  |

## Functionalities 

The senhasegura webservice has some functionalities to perform operations on the application.

### Publish Certificate

 
` 
POST https://vault_url/iso/cert/publish 
` 
 functionality prompts you to publish a certificate on one or more devices.

#### Parameters

|  |  Type |  Description |  Required |
| --- | --- | --- | --- |
|  |  Int |  Code of a certificate to be publish. |  Yes |
|  |  Int |  Publish profile code.A publication profile previously registered on senhasegura will be used. |  Yes |
|  |  String |  Justification of publication up to 1024 characters. |  No |
|  |  Int |  Publication reason code.You must enter a code for a reason entered on senhasegura. |  Yes |
|  |  String |  characters to determine ITSM code. Required if in the certificate access group the parameter "Governance code required when justifying" is enabled. Perform ITSM validations in the same way as the web interface. |  Conditional |
|  |  Array |  Array with the codes of the devices where the certificate is to be published. Devices must exist on senhasegura. |  Yes | 

#### Response to certificates

If the functions succeeds or fails, the response consists of a certified block with the fields:

|  |  Type |  Success |  Error |
| --- | --- | --- | --- |
|  | Int  | OK |  4xx |
|  | Text |  Created |  Invalid certificate code. |
|  | Boolean |  false |  true |
|  | String |  Posting scheduling code |  |
|  | Int |  Code and name of reason for publication |  Reason code entered is invalid. |
|  |  String |  ITSM code entered |  Enter the ITSM code. ITSM code does not exist on senhasegura integrated ITSM system. The code must be a maximum of 30 characters. |
|  |  Array |  Device Codes for Publishing |  |

### Query / List Publications

 
` 
GET https://vault_url/iso/cert/publish/\[code_request\] 
` 
 feature queries one or more publications on senhasegura .

#### Parameters

|  |  Type |  Description |  Required |
| --- | --- | --- | --- |
|  |  Int |  Publication code. |  No |
|  |  Int |  Code of certificate to be published. |  No |
|  |  Int |  Publish Profile Code. |  No |
|  |  String |  Date of registration |  No |
|  |  Int |  Publication processing status.The options will be: 1 = Yes; 0 = No |  No | 
|  |  Int |  Publication Error Status.The options will be: 1 = Yes; 0 = No |  No |  
|  |  Int |  Publication reason code. |  No |
|  |  String |  ITSM code Text reported. |  No |
|  |  Int |  Device code of the publication. |  No |
|  |  Int |  Base number of record count by pagination. |  No |
|  |  Int |  Number of records in pagination. |  No |

#### Response to certificates

If the function succeeds or fails, the response consists of a certified block with the fields:

|  |  Type |  Success |  Error |
| --- | --- | --- | --- |
|  | Int | OK |  4xx |
|  | Text |  Created |  Invalid certificate code. |
|  | Boolean |  false |  true |
|  | String |  Posting scheduling code |  |
|  | Int |  Code and name of reason for publication |  Reason code entered is invalid. |
|  |  String |  ITSM code entered |  Enter the ITSM code. ITSM code does not exist on senhasegura integrated ITSM system. The code must be a maximum of 30 characters. |
|  | String |  Publishing credential code |  The credential code you entered is invalid. |
|  | Int |  Username for credential search |  |
|  | Int |  Number of devices in the publication |  |

### Create/Edit Apache Publication Profile 

 
` 
POST https://vault_url/iso/cert/profile/apache 
` 
 function creates or edits an Apache plugin publishing profile.

#### Parameters

|  |  Type |  Description |  Required |
| --- | --- | --- | --- |
|  |  Int |  Code of an already created profile.If the code is not passed, the system will interpret it as creating a profile. |  No |
|  |  String |  Name of profile to create. |  Yes |
|  |  String |  Site where the certificate is to be installed. If not entered, the certificate will be installed on the default Apache site. |  No | 
|  |  String |  Address of the configuration.Standard: /etc/apache2/sites-available/default.com.conf | No | 
|  |  Int |  Port. Default:443 |  No |  
|  |  Int |  Credential code to be used in the publication. A credential previously registered in the vault will be used. This information is required if a username is not entered. |  Conditional |
|  |  String |  Username that will be used to find credentials for the publication. This information is required if you do not enter a code_credential** |  Conditional |
|  |  Array |  Array with the codes of the devices where the certificate is to be published |  Yes |

#### Response to certificates

If the function succeeds or fails, the response consists of a certified block with the fields:

|  |  Type |  Success |  Error |
| --- | --- | --- | --- |
|  | Int |  OK | 4xx | 
|  | Text |  Created |  Invalid certificate code. |
|  | Boolean |  false |  true |
|  | String | Profile name | The code of profile informed is invalid |
|  | String | Profile name |  |
|  | String | Informed Text |  |
|  | String |  Configured Path |  |
|  | Int | Port |  |
|  | Int | Credential code to publication |  The credential code informed is invalid |
|  | String | Username to search credentials |  |
|  | Array | Devices’ code to publication |  |

### Create/Edit IIS Publication Profile

 
` 
POST https://vault_url/iso/cert/profile/iis 
` 
 function creates or edits an Apache plugin publishing profile.

#### Parameters

|  |  Type |  Description |  Required |
| --- | --- | --- | --- |
|  |  Int |  Code of an already created profile.If the code is not passed, the system will interpret it as creating a profile. |  No |
|  |  String |  Name of profile to create. |  Yes |
|  |  String |  Site where the certificate is to be installed. If not entered, the certificate will be installed on the default IIS site. | No |
|  | String |  IIS certificate management repository. Default: MY | No |
|  |  Int |  Port. Default:443 |  No | 
|  |  Int | Credential code to be used in the publication. A credential previously registered in the vault will be used. This information is required if a username is not entered. |  Conditional |
|  |  String |  Username that will be used to find credentials for the publication. This information is required if you do not enter a code_credential |  Conditional |  
|  |  Array |  Array with the codes of the devices where the certificate is to be published |  Yes |

#### Response to certificates

If the function succeeds or fails, the response consists of a certified block with the fields:

|  |  Type |  Success |  Error |
| --- | --- | --- | --- |
|  | Int | OK | 4xx |  
|  | Text |  Created |  Invalid certificate code. |
|  | Boolean |  false |  true |
|  | String | Profile name | The code of profile informed is invalid |
|  | String | Profile name |  |
|  | String | Informed Text |  |
|  | String | IIS certificate management repository |  |
|  | Int | Port |  |
|  | Int | Credential code to publication |  The credential code informed is invalid |
|  | String | Username to search credentials |  |
|  | Array | Devices’ code to publication |  |

### Create/Edit F5 Big IP Publication Profile

 
` 
POST https://vault_url/iso/cert/profile/bigip 
` 
 function creates or edits an Apache plugin publishing profile.

#### Parameters

|  |  Type |  Description |  Required |
| --- | --- | --- | --- |
|  |  Int |  Code of an already created profile.If the code is not passed, the system will interpret it as creating a profile. |  No |
|  |  String |  Name of profile to create. |  Yes |
|  | String |  Name of the partition | No |
|  | String | Name of the certificate. If a certificate with the same name is already configured, on publication it will be replaced. | No |
|  | Array |  Array of SSL Client Profiles and their VIPs | No |
|  | Array | Array of SSL Server Profiles and their VIPs | No |
|  |  Int |  Credential code to be used in the publication. A credential previously registered in the vault will be used.This information is required if a username is not entered. |  Conditional |
|  |  String |  Username that will be used to find credentials for the publication. This information is required if you do not enter a code_credential** |  Conditional |  
|  |  Array |  Array with the codes of the devices where the certificate is to be published |  Yes |

#### Response to certificates

If the function succeeds or fails, the response consists of a certified block with the fields:

|  |  Type |  Success |  Error |
| --- | --- | --- | --- |
|  | Int | OK | 4xx |  
|  | Text |  Created |  Invalid certificate code |
|  | Boolean |  false |  true |
|  | Int | Publish profile code | The code of profile informed is invalid |
|  | String | Profile name |  
|  | String | Name of the profile |  
|  | String | Name of the certificate that is shown on the web application |  |
|  | Array | Complete name of the profile |  
|  | Array | Complete name of the profile |  
|  | Int | Credential code to publication |  The credential code informed is invalid |
|  | String | Username to search credentials |  
|  | Array | Device’s code to publication |  

### Create/Edit WebSphere WAS Profile Publication

 
` 
POST https://vault_url/iso/cert/profile/was 
` 
 function creates or edits an Apache plugin publishing profile.

#### Parameters

|  |  Type |  Description |  Required |
| --- | --- | --- | --- |
|  |  Int |  Code of an already created profile. If the code is not passed, the system will interpret it as creating a profile. |  No |
|  |  String |  Name of profile to create. |  Yes |
|  | String | Path of the Key database name | Yes |
|  | String | Server’s password | Yes |
|  | String | Server’s label | Yes |
|  |  Int |  Credential code to be used in the publication. A credential previously registered in the vault will be used. This information is required if a username is not entered. |  Conditional |
|  |  String |  Username that will be used to find credentials for the publication. This information is required if you do not enter a code_credential** |  Conditional |  
|  |  Array |  Array with the codes of the devices where the certificate is to be published |  Yes |

#### Response to certificates

|  |  Type |  Success |  Error |
| --- | --- | --- | --- |
|  | Int | OK |  4xx | 
|  | Text |  Created |  Invalid certificate code. |
|  | Boolean |  false |  true |
|  | Int | Publish profile code | The code of profile informed is invalid |
|  | String | Profile name |  
|  | String | Path of the Key database name |
|  | String | Server’s label |  
|  | Int | Credential code to publication |  The credential code informed is invalid |
|  | String | Username to search credentials | 
|  | Array | Devices’ code to publication |  

### Import an SSL certificate
#### Request
To import an SSL certificate, send a request to the following endpoint: 
`
PUT api/certificate/upload
`


#### Request parameters




| Field | Type | Required | Description | Example |
| --- | --- | --- | --- | --- |
|  | String | Yes | Code of a certificate already created in passwords. | Base64_encoded_certificate_file |
|    | String | No | In case this field is empty, the key won’t be available in the system, limiting the use of the certificate, its publishing, and the possibility to link it to devices.
Note: The .pfx extension already has a private key in it. Therefore, even if you don’t inform its value in the API call, you’ll still be able to view it in the response. | Base64_encoded_private_key_file |
|  | String | No | Password to retrieve the corresponding certificate | null |
|  | String | No | Password to revoke the associated SSL certificate. | null |
|  | String | Yes |  | certificate_extension |



`
{
    "certificate": "Base64_encoded_certificate_file",
    "private_key": "Base64_encoded_private_key_file",
    "password": null,
    "revoke_password": null,
    "extension": "certificate_extension",
}

`

#### Return

Imports an SSL certificate and returns a message with information about the process.





`
HTTP/1.1 200 OK
`

`
{
    "response": {
        "status": 200,
        "message": "1001: OK",
        "error": false,
        "error_code": 0,
        "status_certificate": 1,
        "detail": "",
        "mensagem": "1001: OK",
        "erro": false,
        "cod_erro": 0
}
`



`
HTTP/1.1 400 BAD REQUEST
`

`
{
    "response": {
        "status": 400,
        "message": "1049: There is no certificate with the given code",
        "error": false,
        "error_code": 0,
        "status_certificate": 1,
        "detail": "",
        "mensagem": "1049: There is no certificate with the given code",
        "erro": false,
        "cod_erro": 0
},
   
    "exception": {
        "code": 1049,
        "message": "1049: There is no certificate with the given code",
        "detail": null
}

`

#### Possible errors
Here’s a list with HTTP error codes and their reasons:


*  missing  parameter.

* : token expired.

*  no token registered for the call.

*  the certificate already exists.

*  invalid or empty certificate.

*  invalid .
.

*  empty .


:::
