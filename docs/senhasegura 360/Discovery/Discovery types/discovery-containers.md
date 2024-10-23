## Metadata_Start 
## code: en
## title: Containers 
## slug: discovery-containers 
## seoTitle: Containers 
## description:  
## contentType: Markdown 
## Metadata_End
1. Go to 
2. Click on the icon , and choose the option 

!

3. Select 
4. Add the information:

!

-  name that will identify the search.
-  IP or device name of the controller. The device where containers are hosted. All registered container hostnames will be displayed.
-  indicate if you want the device activated or not.

## Connection

-  an access credential for the search. Choose an IP, a Hostname, or a Username.

:::(info)

It is recommended that you use the credentials of a user who has access to the search in question or privileged access.

:::

All credentials registered in senhasegura will be displayed.

-  password used before performing the authentication of the search process.
-  if the user needs to execute the sudo to have the permissions of these searches, the commands will be executed as a superuser.

:::(info)

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

:::(info)
The Certificates tab will be visible if this field is checked.

:::

-  if this option is enabled, DevOps artifacts will be included in the Discovery process.

:::(info)
The DevOps tab will be visible if this field is checked.

:::

-  if this option is enabled, unauthorized access to credentials will be monitored and logs can be viewed in Discovery.
-  if this option is enabled, credentials in application pools (IIS) will be included in Scan & Discovery.
-  if this option is enabled, device search will identify its FQDN and consider it in the discovery process.

:::(info)

The FQDN will be the unique device identifier if this option is enabled.

:::
## Containers
!



- Search only running containers



- Uses Docker
- Search only running containers

## Plugins
!

Click on the icon + e fill in the plug-in field.

:::(info)

To search for Windows service accounts, you will need to select a Windows plugin under the Plugins tab.

:::
## Execution

!

-  credential verification that will remain active after credential import or not.
- : days that will be allowed to perform the execution.
- : times that will be allowed for execution.
-  minimum interval, in hours, between scan runs. This criterion takes into account the values informed in the Days allowed for execution and Periods allowed for execution fields.

:::(info)

It is not recommended to add an interval of fewer than 8 hours.

:::

## Adjacent tabs

## Certificates

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

:::(info) 

This option allows certificates with a password and key to be imported into senhasegura.

:::



When selecting the  option, this field will be displayed:
* Ports for searching for certificates without login



When selecting the  option, this field will be displayed:

- * select a user, already registered with senhasegura, that contains the value of the API Key.
- * indicates that when finding the certificates, the keys will be imported to senhasegura as well.

:::(info)

Go to , to view the report of found certificates. Use the action button to perform a manual import.

:::



When selecting the  option, these fields will be displayed:
* API URL
* Kubernetes access token
* Kubernetes access port



When selecting the  option, these fields will be displayed:
* Import key
* API key

## DevOps

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

:::(info) 

senhasegura has a Kubernetes plugin that allows you to use credentials registered in the vault to use the service, increasing security when using the system. To gain access to the plugin, contact the senhasegura support team.

:::