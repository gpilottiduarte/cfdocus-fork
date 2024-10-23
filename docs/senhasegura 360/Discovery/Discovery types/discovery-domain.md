## Metadata_Start 
## code: en
## title: Domain 
## slug: discovery-domain 
## seoTitle: Domain 
## description:  
## contentType: Markdown 
## Metadata_End
1. Go to 
2. Click on the icon , and choose the option 

!

1. Select 
2. Add the information:

!

-  name that will identify the search.
-  IP or domain name.
-  domain base name/domain distinguishing name.
-  indicate if you want the device activated or not.
-  select if you want an exclusive glossary with the data requested in the search.

## Connection

-  an access credential for the search. Choose an IP, a Hostname, or a Username.

:::(info) (Info)

It is recommended that you use the credentials of a user who has access to the search in question or privileged access.

:::

All credentials registered in senhasegura will be displayed.

-  password used before performing the authentication of the search process.
-  if the user needs to execute the sudo to have the permissions of these searches, the commands will be executed as a superuser.

:::(info) (Info)

The credential filled in the  field must have the info .

:::

- 
    -  the set of credentials used to perform the verification.
    -  the credential set priority.

Higher-priority credential pools take precedence over lower-priority credential pools.

## Searches
!

-  if this option is enabled, credentials will be included in the discovery process.
-  if this option is enabled, device groups will be included in the discovery process.
-  if this option is enabled, digital certificates will be included in the Discovery process.

:::(info) (info)
The Certificates tab will be visible if this field is checked.

:::

-  if this option is enabled, DevOps artifacts will be included in the Discovery process.

:::(info) (info)
The DevOps tab will be visible if this field is checked.

:::

-  if this option is enabled, unauthorized access to credentials will be monitored and logs can be viewed in Discovery.
-  if this option is enabled, credentials in application pools (IIS) will be included in Scan & Discovery.
-  if this option is enabled, device search will identify its FQDN and consider it in the discovery process.

:::(info) (Info)

The FQDN will be the unique device identifier if this option is enabled.

:::

## Search parameters
!

-  form type used for account search.
-  credential filter domain name.

:::(info) (Info)

If left blank, the base DN will be used.

:::

-  device filter domain name.

:::(info) (Info)

If left blank, the base DN will be used.

:::

-  name attribute of accounts to be fetched.
-  server name or IP.
-  domain name.
-  simplified domain name (optional).
-  indicate whether or not to use an SSL certificate when searching.
-  user connection to the domain.
-  to link the user to the domain
-  domain name of the user doing the search. If left blank, the base DN will be used.

## Filters for search
!

-  filter to identify the desired credentials.
-  filter to identify the desired devices.
-  filter to identify the desired plugins.

When choosing the Windows Plug-in option, senhasegura will attempt to connect to devices using the Windows RPC, Windows WMI, and Windows RM protocols.

## Execution
!

-  credential verification that will remain active after credential import or not.
- : days that will be allowed to perform the execution.
- : times that will be allowed for execution.
-  minimum interval, in hours, between scan runs. This criterion takes into account the values informed in the Days allowed for execution and Periods allowed for execution fields.

:::(info) (Info)

It is not recommended to add an interval of fewer than 8 hours.

:::

## Import
!

-  an exclusive glossary with the data requested in the
 search.
:::(info) (Info)
The unique glossary will be created with the information provided in * and *. By choosing this feature, all the devices found by the discovery will be related to the unique glossary.
:::
- 
    - Site
    - Type
    - Vendor
    - Product
- 
    - Type of default credential
    - Type of privileged credential
-  indicates whether the automatic importation of credentials and devices is enabled or not.
-  credential usernames that will be automatically imported (e.g. Administrator).

## Additional tabs
Additional tabs will be displayed only if selected in the Searches tab

### Certificates

If you click on Searches, and the option "Search for certificates" is checked, you will have one more tab:

!

:::(Info) (Info)
Valid extensions for performing a certificate discovery are:
.crt, .cer, .ca-bundle, .p7b, .p7c, .p7s, .pem, .p12, .pfx and .pem

It is possible to discover certificates along with keys, as long as the search takes place in directories in Linux environments.
:::

:::(Warning) (Caution)
 imports the key along with the certificate. It is not possible to import keys separately.
:::



- Apache
- Nginx
- Tomcat
- Search certificates in directories
- IIS
- Workstation Windows
- IBM Websphere
- Search certificates without login
- Issued by Microsoft CA
- Palo Alto
- Kubernetes
- NetScaler



- Import all certificates automatically
- Extra settings for F5/BigIP



When selecting the  option, this field will be displayed:
* Tomcat configuration file path



When selecting the  option, these fields will be displayed:
* Path of the directory where to fetch certificates
* File extensions to look for



When selecting the  option, these fields will be displayed:
* Search local Windows certificates
* Search Windows user certificates
* Search CA's root



When selecting the  option, these fields will be displayed:
* Path of app_server_root websphere
* Credential
* KDB Path websphere to search certificates
* Discovery using credential from vault
* Discovery using pool of credentials

:::(info) (Info)

This option allows certificates with a password and key to be imported into senhasegura.

:::



When selecting the  option, this field will be displayed:
* Ports for searching for certificates without login



When selecting the  option, this field will be displayed:

- * select a user, already registered with senhasegura, that contains the value of the API Key.
- * indicates that when finding the certificates, the keys will be imported to senhasegura as well.

:::(info) (Info)

Go to , to view the report of found certificates. Use the action button to perform a manual import.

:::



When selecting the  option, these fields will be displayed:
* API URL
* Kubernetes access token
* Kubernetes access port



When selecting the  option, these fields will be displayed:
* Import key
* API key

### DevOps

If you click on Searches, and the option "Find DevOps artifacts" is checked, you will have one more tab:
!



-  indicates whether the Ansible service is enabled.
-  indicates whether the search for playbooks is enabled.
-  indicates whether role search is enabled.
-  indicates whether host search is enabled.



-  indicates if Jenkins searches are enabled in this search.
-  if this option is enabled, Discovery will search for Jenkins Jobs.
-  if this option is enabled, Discovery will search for Jenkins nodes.
-  if this option is enabled, Discovery will search for Jenkins users.
-  a token that will be used to access Jenkins.
-  Jenkins access port.



-  indicates whether Kubernetes searches are enabled for this search.
-  if this option is enabled, Discovery will search for Kubernetes Secrets.
-  indicates whether the bearer of the token is the same as the credential.
-  credential that will be used to access Kubernetes.
-  access port to Kubernetes.

:::(info) (Info)

senhasegura has a Kubernetes plugin that allows you to use credentials registered in the vault to use the service, increasing security when using the system. To gain access to the plugin, contact the senhasegura support team.

:::