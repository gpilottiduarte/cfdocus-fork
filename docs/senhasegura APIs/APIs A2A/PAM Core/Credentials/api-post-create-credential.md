## Metadata_Start 
## code: en
## title: POST | Create credential 
## slug: api-post-create-credential 
## seoTitle: POST | Create credential 
## description:  
## contentType: Markdown 
## Metadata_End
Create a credential in .

## Requirements
* Authorization with  and  permission to  granted by the administrator in . 
Access the document on  for more information.
* Device created in . 
Access the document  for more information.

## Request

  POST 
 
 ## Request parameters
Send the parameters below in the request body.

* identifier - string - Unique string defined by the user or by senhasegura for identifying the credential.
Note: although users aren’t required to fill out this field, for security reasons and to enable future updates of the credential, the system will automatically generate an identifier based on UUID if left blank. This value can be updated in future calls.
Example: 018fe9a6-541d-7380-99b6-56051b71a475



* username - string -  required - Name of the user assigned to the credential.

Note: it's not necessary to send a value for the parameter, but it's necessary to send the parameter. 
New credential default value: usr


* hostname - string -  required - Hostname of the device associated with the credential.


* ip - string -  required - IP address of the device associated with the credential.


* content - string -  Password assigned to the credential.
New credential default value: -


* additional - string - Additional credential information.
New credential default value: -


* tags - string - Keywords associated with the credential.
New credential default value: -



* credential_type - string - Type of credential.
New credential default value: Local User


* domain - string - Name or abbreviation of the domain.
New credential default value: -


* parent_password - int - ID of the parent credential.
New credential default value: -


* type- string - Type of device.
Note: a new type is created if the value sent is unique.
New credential default value: -
  
  
* vendor - string - Device manufacturer.
Note: a new vendor is created if the value sent is unique.
New credential default value: -


* model - string - Device model.
 Note: a new model is created if the value sent is unique.
New credential default value: -


* site - string - Device location.
Note: a new site is created if the value sent is unique.
New credential default value: -


* device_domain - string - Device domain name or abbreviation.
Note: only previously registered domains are accepted.
New credential default value: -

:::(Warning) (Attention)
When listing more than one , add commas without spaces between them, as in the following example: 

:::


* device_tags - string - Keywords associated with the device.
New credential default value: -


* connectivities - string - Device connectivity.
New credential default value: -


* session_remote_config - string - Login expression.
New credential default value: -



* execution_settings - object - Administrative settings for credential automatic password change and reconciliation.
Example:  refer to the Execution settings section.
New credential default value: -


* session_settings  - object - Settings for session privilege management for remote applications, connectivity protocols, among others.
Example: refer to the Session settings section.
New credential default value: -
 
 
* additional_settings - object - Settings for implementing credential authentication mechanisms such as TOTP, and designation of the credential's owner user, among others.
Example: refer to the Additional settings section.
New credential default value: -


* jit_settings  - object - Settings to manage the service usage time.
Example: refer to the  JIT settings section.
New credential default value: -


## Credential creation options
You can choose one of the following options to create a credential in :
- Providing a value for the parameter .
- Providing a value for the parameter .

In both cases, you must provide existing values for the  and  parameters of the device associated with the credential.


:::(Info) (Info)
Before continuing, please note that the terms  and  in the context of this document mean: 
*  - a value that already belongs to a credential. 
*  - a value that doesn’t belong to a credential yet.
:::

### Send the  parameter
* Send existing  and  .
* Send a new .
* Send a new .



    
        
            Condition
            ->
            Result
        
        
            Existing identifier 
            
            The credential will be updated with the other parameters.
        
        
            New identifier
            The system will search for the credential by their hostname, ip and username
            Credential found
            The credential will be updated with the other parameters.
        
        
            Credential not found
            A new credential will be created.
.
        
    



#### Example request - new  


The following example shows the creation of a credential with a new .

  POST 
 
`json
{
    "identifier": "dyaihdppaj78a547",
    "username" : "username",
    "hostname": "w2016",   
    "ip": "10.66.33.15",
    "content": "blfjahbnaihdaa",
    "tags": "social"
}
`
#### Response 

 `json
HTTP/1.1 201 CREATED
`
 `json
{
    "code": 201,
    "response": {
        "status": 201,
        "message": "Credential successfully registered!",
        "error": false,
        "error_code": 0,
        "detail": "",
        "mensagem": "Credential successfully registered!",
        "erro": false,
        "cod_erro": 0
    },
    "tenant": "senhasegura",
    "credential": {
        "id": "152",
        "identifier": "dyaihdppaj78a547"
    }
}

`

### Send the  parameter

* Send existing  and .
* Send a new . 
* Don’t send a value for the .

Condition| Result|
------|------|
 | .|
existing |The credential will be updated with the other parameters.|
 


#### Example request - new  
The following example shows the creation of a credential with a new .

 POST 
`json
{
    "username" : "newusername",
    "hostname": "w2016",   
    "ip": "10.66.33.15",
    "content": "blfjahbnaihdaa",
    "identifier": "",
    "tags": "social"
}
`

#### Response 

`json
HTTP/1.1 201 CREATED
`

`json
{
    "code": 201,
    "response": {
        "status": 201,
        "message": "Credential successfully registered!",
        "error": false,
        "error_code": 0,
        "detail": "",
        "mensagem": "Credential successfully registered!",
        "erro": false,
        "cod_erro": 0
    },
    "tenant": "senhasegura",
    "credential": {
        "id": "149",
        "identifier": "018fea0c-6fe6-726c-87fd-8e595037e8a2"
    }
}
`

## Other credential parameters
You can also configure a credential by adding other parameters, which include:

* .
* .
* .
* .

### Execution Settings
Administrative settings of the credential in which you can define automatic password rotation and credential reconciliation.

#### Request parameters
Send the parameters below in the  of the request.


&#8226; execution_settings - object - Execution settings data.


&nbsp;&emsp;&emsp;&nbsp;→parent_credential - string - Parent credential selected for the edited credential.


&nbsp;&emsp;&emsp;&nbsp;→parent_hostname - string - Hostname of the selected parent credential.

    
 &nbsp;&emsp;&emsp;&nbsp;→parent_ip - string - Endereço IP address of the parent credential's device.

  

 &nbsp;&emsp;&emsp;&nbsp;→automatic_change - boolean - Enables or disables automatic changes.
&nbsp;&emsp;&emsp;&nbsp;New credential default value: false

  
&nbsp;&emsp;&emsp;&nbsp;→agent_based_password_change - boolean - Enables or disables automated password change via software agent.
&nbsp;&emsp;&emsp;&nbsp;New credential default value: false    


 
&nbsp;&emsp;&emsp;&nbsp;→change_plugin - string - Change plugin used when rotating the credential on the device.

 
&nbsp;&emsp;&emsp;&nbsp;→change_template - string - Change template used when rotating the credential on the device.

 
&nbsp;&emsp;&emsp;&nbsp;→use_own_credential_to_connect - boolean - Enables or disables the use of the credential itself to connect to the device and change the password.
&nbsp;&emsp;&emsp;&nbsp;New credential default value: false

 
&nbsp;&emsp;&emsp;&nbsp;→authentication_credential - string -  required (if the value for the use_own_credential_to_connect parameter is false) - Credential used for authentication during the credential rotation process.


&nbsp;&emsp;&emsp;&nbsp;→authentication_hostname - string -  required (if the value for the use_own_credential_to_connect parameter is false) - Hostname of the authentication device.


&nbsp;&emsp;&emsp;&nbsp;→authentication_ip - string -  required (if the value for the use_own_credential_to_connect parameter is false) - IP address of the authentication device.


&nbsp;&emsp;&emsp;&nbsp;→status - boolean - Enables or disables credential reconciliation after rotation failure.
&nbsp;&emsp;&emsp;&nbsp;New credential default value: false



&nbsp;&emsp;&emsp;&nbsp;→reconciliation_credential - string - Credential to be used in the reconciliation process.


&nbsp;&emsp;&emsp;&nbsp;→reconciliation_hostname - string - Hostname of the reconciliation device.


&nbsp;&emsp;&emsp;&nbsp;→reconciliation_ip - string - IP address of the reconciliation device.


&nbsp;&emsp;&emsp;&nbsp;→reconciliation_plugin - string - Execution plugin for the reconciliation process.


&nbsp;&emsp;&emsp;&nbsp;→reconciliation_template - string - Execution template for the reconciliation process.

 
#### Example request

 POST 
`json
{
    "username": "Example caderno 3.32",
    "hostname": "API-Testing",
    "ip": "128.0.0.1",
    "execution_settings": 
    {
        "parent_credential": "cred2",
        "parent_hostname": "gmail",
        "parent_ip": "https://www.gmail.com",
        "automatic_change": true,
        "agent_based_password_change": true,
        "change_plugin": "SSH",
        "change_template": "3COM",
        "use_own_credential_to_connect": false,
        "authentication_credential": "cred2",
        "authentication_hostname": "gmail",
        "authentication_ip": "https://www.gmail.com",
        "status": true,
        "reconciliation_credential": "cred2",
        "reconciliation_hostname": "gmail",
        "reconciliation_ip": "https://www.gmail.com",
        "reconciliation_plugin": "SSH",
        "reconciliation_template": "3COM"
    }
}
`

### Session Settings
Settings implemented to manage session privileges, where you can restrict remote applications, connectivity protocols, among others.

#### Request parameters
Send the parameters below in the  of the request.

 
&#8226; session_settings - object - Session settings data.





&nbsp;&emsp;&emsp;&nbsp;→SSH - boolean - Enables or disables the SSH protocol.
&nbsp;&emsp;&emsp;&nbsp;New credential default value: false


&nbsp;&emsp;&emsp;&nbsp;→Telnet - boolean - Enables or disables the Telnet protocol.
&nbsp;&emsp;&emsp;&nbsp;New credential default value: false


&nbsp;&emsp;&emsp;&nbsp;→MySQL - boolean - Enables or disables MySQL connection.
&nbsp;&emsp;&emsp;&nbsp;New credential default value: false


&nbsp;&emsp;&emsp;&nbsp;→SQL Server - boolean - Enables or disables SQL Server connection.
    &nbsp;&emsp;&emsp;&nbsp;New credential default value: false


&nbsp;&emsp;&emsp;&nbsp;→HTTP - boolean - Enables or disables the HTTP protocol.
&nbsp;&emsp;&emsp;&nbsp;New credential default value: false
    


&nbsp;&emsp;&emsp;&nbsp;→HTTPS - boolean - Enables or disables HTTPS connection.
&nbsp;&emsp;&emsp;&nbsp;New credential default value: false


&nbsp;&emsp;&emsp;&nbsp;→RDP - boolean - Enables or disables RDP connection.
&nbsp;&emsp;&emsp;&nbsp;New credential default value: false


&nbsp;&emsp;&emsp;&nbsp;→X11 Forward - boolean - Enables or disables X11 Forward.   
&nbsp;&emsp;&emsp;&nbsp;New credential default value: false


&nbsp;&emsp;&emsp;&nbsp;→VNC - boolean - Enables or disables VNC connection.
&nbsp;&emsp;&emsp;&nbsp;New credential default value: false



&nbsp;&emsp;&emsp;&nbsp;→restrict_access_to_remote_application - boolean - Enables or disables the use of the credential only in RemoteApp proxy sessions.
&nbsp;&emsp;&emsp;&nbsp;New credential default value: false


&nbsp;&emsp;&emsp;&nbsp;→macros - array of objects  - Macro automation data containing remote_app and  connectivity.


&nbsp;&nbsp;&nbsp;&nbsp;&emsp;&emsp;&emsp;&emsp;&nbsp;&nbsp;→remote_app - string - RemoteApp automation associated with the credential.


&nbsp;&nbsp;&nbsp;&nbsp;&emsp;&emsp;&emsp;&emsp;&nbsp;&nbsp;→connectivity - string - Connectivity for RemoteApp automation associated with the credential.



&nbsp;&emsp;&emsp;&nbsp;→use_own_credential_to_connect - boolean - Enables or disables the use of the credential itself for connection.
&nbsp;&emsp;&emsp;&nbsp;New credential default value: false


&nbsp;&emsp;&emsp;&nbsp;→authentication_credential - string -  required (if the value for the use_own_credential_to_connect parameter is false - The authentication credential.
.


&nbsp;&emsp;&emsp;&nbsp;→authentication_hostname - string -  required (if the value for the use_own_credential_to_connect parameter is false - The IP address of the authentication device.


&nbsp;&emsp;&emsp;&nbsp;→authentication_ip -  required (if the value for the use_own_credential_to_connect parameter is false - O endereço IP do dispositivo de autenticação.


 

#### Example request

 POST 
`json
{
    "username": "Example caderno 3.32",
    "hostname": "API-Testing",
    "ip": "128.0.0.1",
    "session_settings": 
        {
            "SSH": true,
            "Telnet": true,
            "MySQL": true,
            "SQL Server": true,
            "HTTP": true,
            "HTTPS": true,
            "RDP": true,
            "X11 Forward": true,
            "VNC": true,
            "restrict_access_to_remote_application": true,
            "macros": 
            [
                {
                    "remote_app": "MySQL",
                    "connectivity": "SSH"
                },
                {
                    "remote_app": "Kaspersky",
                    "connectivity": "RDP"
                }
            ],
            "use_own_credential_to_connect": false,
            "authentication_credential": "cred2",
            "authentication_hostname": "gmail",
            "authentication_ip": "https://www.gmail.com"
        }
}
`
    
### Additional settings
Settings to implement credential authentication mechanisms, such as TOTP, and to designate the credential's owner, among others.

#### Request parameters
Send the parameters below in the  of the request.
    

&#8226; additional_settings - array of objects - Session settings data.


&nbsp;&emsp;&emsp;&nbsp;→identifier - string - Credential identifier. Used to retrieve the credential via Webservice (A2A).



&nbsp;&emsp;&emsp;&nbsp;→user_credential_owner - string - Credential owner's username.


&nbsp;&emsp;&emsp;&nbsp;→server_path - string - Path to the script or file where the credential is stored.


&nbsp;&emsp;&emsp;&nbsp;→secret_key - string - The secret key (TOTP) used to generate temporary passwords for authentication.


&nbsp;&emsp;&emsp;&nbsp;→criticality - string - The criticality level of the credential. Possible values are low, medium and high.
    

&nbsp;&emsp;&emsp;&nbsp;→additional_authentication_fields - array de objetos  - Additional information required to complete authentication steps containing name, short_name and  value.


&nbsp;&nbsp;&nbsp;&nbsp;&emsp;&emsp;&emsp;&emsp;&nbsp;&nbsp;→name - string - Name of the additional authentication.


&nbsp;&nbsp;&nbsp;&nbsp;&emsp;&emsp;&emsp;&emsp;&nbsp;&nbsp;→short_name - string - Short name of the additional authentication.


&nbsp;&nbsp;&nbsp;&nbsp;&emsp;&emsp;&emsp;&emsp;&nbsp;&nbsp;→value - string - The value to be filled in during the additional authentication process.


&nbsp;&emsp;&emsp;&nbsp;→notes - string - General notes about the credential.
    &nbsp;&emsp;&emsp;&nbsp;Example: Credential to be used only in network A.	

 
 #### Example request

 POST 
`json
{
    "username": "Example caderno 3.32",
    "hostname": "API-Testing",
    "ip": "128.0.0.1",
    "additional_settings": [
        {
            "identifier": "identifer",
            "user_credential_owner": "admin",
            "server_path": "/etc/host",
            "secret_key": "295B3LA1M6LRAHI2S7G1A36LMK6I4IWW",
            "criticality": "High",
            "additional_authentication_fields": [
                {
                    "name": "name",
                    "short_name": "short_name1",
                    "value": "Enable"
                },
                {
                    "name": "name2",
                    "short_name": "short_name2",
                    "value": "value"
                }
            ]
        }
    ],
    "notes": "Credential to be used only in network A"
}

`
### JIT Settings
JIT (Just-in-Time) settings are implemented to manage the time-limited use of services, especially in contexts where temporary access is required to perform specific actions. This is often applied in situations like account creation, service activation, or adding temporary permissions to perform certain tasks.

JIT credentials are used to initiate sessions on devices located in segregated networks. These credentials are accessible via Web Proxy, Terminal Proxy, and RDP Proxy, ensuring secure and temporary access to the necessary resources.

In senhasegura, you can implement JIT settings when creating a credential for the following scenarios:

* Create and delete a credential upon the initiation and termination of a Proxy session.

* Enable and disable a credential upon the initiation and termination of a Proxy session.

#### Create and delete a credential upon the initiation and completion of a Proxy session.

 #### Request parameters
Send the parameters below in the  of the request.


&#8226; jit_settings - object  - Just-in-Time settings data for creating and removing credentials upon the initiation and termination of a Proxy session.


&nbsp;&emsp;&emsp;&nbsp;→jit - boolean - Enables or disables JIT settings.



&nbsp;&emsp;&emsp;&nbsp;→credential_creation_and_deletion - boolean - Indicates credential creation upon Proxy session initiation and deletion after session termination.



&nbsp;&emsp;&emsp;&nbsp;→use_own_credential_to_connect - boolean - Enables or disables the use of the credential itself for connection.


&nbsp;&emsp;&emsp;&nbsp;→authentication_credential - boolean -  required (if the value for the use_own_credential_to_connect parameter is false - Authentication credential.


&nbsp;&emsp;&emsp;&nbsp;→authentication_hostname - boolean -  required (if the value for the use_own_credential_to_connect parameter is false - Hostname of the authentication device.


&nbsp;&emsp;&emsp;&nbsp;→authentication_ip - boolean -  required (if the value for the use_own_credential_to_connect parameter is false - IP address of the authentication device.


&nbsp;&emsp;&emsp;&nbsp;→credential_creation_plugin - string - Plugin for credential creation.
    &nbsp;&emsp;&emsp;&nbsp;Note: this field must be filled with an existing plugin already registered in senhasegura.
    

&nbsp;&emsp;&emsp;&nbsp;→credential_creation_template -string - Template for credential creation.
    &nbsp;&emsp;&emsp;&nbsp;Note: this field must be filled with an existing template already registered in senhasegura.
 

&nbsp;&emsp;&emsp;&nbsp;→credential_deletion_plugin - string - Plugin for credential deletion.
&nbsp;&emsp;&emsp;&nbsp;Note: this field must be filled with an existing plugin already registered in senhasegura.
    

&nbsp;&emsp;&emsp;&nbsp;→credential_deletion_template - string - Template for credential deletion.
&nbsp;&emsp;&emsp;&nbsp;Nota: this field must be filled with an existing template already registered in senhasegura.
    




#### Example request
 POST 
`json
{
  "username": "API_CREDENTIAL_3",
  "hostname": "API_DEVICE_1",
  "ip": "localhost",
  "jit_settings": {
    "jit": true,
    "credential_creation_and_deletion": true,
    "enable_disable_credential": false,
    "use_own_credential_to_connect": false,
    "authentication_credential": "API_CREDENTIAL_1",
    "authentication_hostname": "API_DEVICE_1",
    "authentication_ip": "localhost",
    "credential_creation_plugin": "SSH",
    "credential_creation_template": "Linux - Create User",
    "credential_deletion_plugin": "SSH",
    "credential_deletion_template": "Linux - Remove User"
  }
}
`
    
 #### Enable and disable credential upon Proxy session initiation and termination

 #### Request parameters
Send the parameters below in the  of the request.
    
    

&#8226; jit_settings - object  -  Just-in-Time settings for enabling and disabling a credential upon Proxy session initiation and termination.


&nbsp;&emsp;&emsp;&nbsp;→jit - boolean - Enables or disables JIT settings.



&nbsp;&emsp;&emsp;&nbsp;→enable_disable_credential - boolean - Indicates enabling the credential upon Proxy session initiation and disabling it after session termination.


&nbsp;&emsp;&emsp;&nbsp;→use_own_credential_to_connect - boolean - Enables or disables the use of the credential itself for connection.


&nbsp;&emsp;&emsp;&nbsp;→authentication_credential - string -  required (if the value for the use_own_credential_to_connect parameter is false - The authentication credential.


&nbsp;&emsp;&emsp;&nbsp;→authentication_hostname - string -  required (if the value for the use_own_credential_to_connect parameter is false - The hostname of the authentication device.


&nbsp;&emsp;&emsp;&nbsp;→authentication_ip - string -  required (if the value for the use_own_credential_to_connect parameter is false - The IP address of the authentication device.


&nbsp;&emsp;&emsp;&nbsp;→credential_enable_plugin - string - Plugin for credential enablement.
&nbsp;&emsp;&emsp;&nbsp;Note:  this field must be filled with an existing plugin already registered in senhasegura.
    
   


&nbsp;&emsp;&emsp;&nbsp;→credential_enable_template - string - Template for credential enablement.
&nbsp;&emsp;&emsp;&nbsp;Note: this field must be filled with an existing template already registered in senhasegura.
    
   

&nbsp;&emsp;&emsp;&nbsp;→credential_disable_plugin - string - Plugin for credential disablement.
    &nbsp;&emsp;&emsp;&nbsp;Note: this field must be filled with an existing plugin already registered in senhasegura.
        


&nbsp;&emsp;&emsp;&nbsp;→credential_disable_template - string - Template for credential disablement.
&nbsp;&emsp;&emsp;&nbsp;Note: this field must be filled with an existing template already registered in senhasegura.
    
      
  #### Example request

 POST 
`json
{
  "username": "API_CREDENTIAL_3",
  "hostname": "API_DEVICE_1",
  "ip": "localhost",
  "jit_settings": {
    "jit": true,
    "enable_disable_credential": true,
    "use_own_credential_to_connect": true,
    "authentication_credential": "API_CREDENTIAL_1",
    "authentication_hostname": "API_DEVICE_1",
    "authentication_ip": "localhost",
    "credential_enable_plugin": "LDAP",
    "credential_enable_template": "AD - Activate User",
    "credential_disable_plugin": "LDAP",
    "credential_disable_template": "AD - Deactivate User"
  }
}
`
    
    
## Errors
 
 
400 - Bad Request.

***
    
Message: "1004: The device's hostname was not informed"
Possible cause: the required parameter hostname of the device wasn’t informed.
Solution: provide a value for the hostname parameter of the device and resend the request. 
  
* * *

Message: "1005: The device's IP was not informed"
Possible cause: the required parameter ip of the device wasn’t informed.
    Solution: provide a value for the ip parameter of the device and resend the request.
  

* * *
    
 Message: "1011: Device not found"
 Possible cause: the device wasn’t found.
  Solution: provide a valid device and resend the request.
 
***
Message: "1029: It is not possible to enter a domain that has not been previously registered"
 Possible cause:  the device_domain sent doesn’t exist or the sent format is incorrect.
  Solution: provide a valid value for the device_domain , or, in case you’re sending more than one device_domain remember to not add space between commas. Example: qakm.lab.mt4.dev,my_device_domain.

  ***
Message: "1039: Without PAM Configuration Access permission"  
Possible cause: your authorization doesn’t have permission to create a credential. 
     
Solution: ask the administrator to check your read and write permission to PAM Core resources in A2A.

*** 
     
Message: "1042: Invalid username"  
Possible cause: the required parameter username wasn’t sent.
     
Solution: enter the username parameter and resend the request. You don’t need to provide a value for the username, but you need to send the parameter.

*** 
     
Message: "1046: Plugin not informed"  
Possible cause: the plugin wasn’t informed.
     
Solution: provide a value for the credential creation, deletion, enablement or disablement plugin. This plugin must exist and be registered in senhasegura. 

*** 
     
Message: "1047: Template plugin not informed"  
Possible cause: the template wasn’t informed.
     
Solution: provide a value for the credential creation, deletion, enablement or disablement template. This template must exist and be registered in senhasegura. 

*** 




404 - Not Found

***
Message: "Resource sub not found"

Possible cause: the URL or the requested resource isn’t correct.
        
Solution: check the URL and make sure the parameter is correct.
* * *




 
500 - Internal Server Error

***
    
Message: "Unexpected error."
 
Possible cause: the error is in the senhasegura server.
        
Solution: contact the support team for more information.

***

Message: "You are not authorized to access this resource."

Possible cause: you don’t have the authorization to access this resource.
        
Solution: ask the administrator to check your permission to access the PAM Core resources in A2A.

* * *
    

  


Client authentication failed

*** 
   
Message: "Client authentication failed."
Possible cause: failure in your application authentication with the senhasegura server. 
        
Solution: check the authentication parameters such as Access Token URL, Client ID e Client secret and request a new access token.
 
* * *   

     
  


Invalid signature

*** 
    
Message: "Invalid signature"
    
Possible cause: failure in recognizing the URL of the client application.
        
Solution: check the URL of the client application and resent the request.

* * * 

     


    No route matched with those values
    
***   
    
Message: "No route matched with those values."
   Possible cause: the authorization header is missing in the API request.
        
  Solution: request a new access token.
   
 * * *

 


     Request timed out
    
***
    
Message: "Request timed out."
Possible cause: the request time has expired.
        
Solution: check the connectivity between the source of the request and the senhasegura server.
