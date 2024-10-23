## Metadata_Start 
## code: en
## title: GET | List all credentials 
## slug: api-get-list-all-credentials 
## seoTitle: GET | List all credentials 
## description:  
## contentType: Markdown 
## Metadata_End
Access information of the credentials associated with your authorization in .

## Requirements

* Authorization with  permission to  granted by the administator in . 
Access the document on  for more information.

## Request

 GET 

:::(Info) (Info)
SSH keys inserted as credentials will also be listed in this response. However, to list a specific SSH key, send a  GET request to the endpoint `api/pam/key.
:::

### Example request
 GET 

## Response 

`json 
HTTP/1.1 200 OK
`

` json
{
    "code": 200,
    "response": {
        "status": 200,
        "message": "2 credentials found",
        "error": false,
        "error_code": 0,
        "detail": "",
        "mensagem": "2 credentials found",
        "erro": false,
        "cod_erro": 0
    },
    "credentials": [
        {
            "id": "2",
            "identifier": "018f3fe6-10e2-724d-9229-a6e9749fa88e",
            "username": "testefelipeqasenhasegura@gmail.com",
            "expiration": "2024-05-16T17:31:31-03:00",
            "change": "2024-05-03 16:19:53",
            "view": "2024-05-24 16:26:09",
            "hostname": "gmail.com",
            "management_ip": "mail.google.com",
            "type": "Local User",
            "type_code": "1",
            "device_model": "Gmail",
            "device_type": "Web Application",
            "device_vendor": "Google",
            "automatic_change": false,
            "connectivity": "HTTPS",
            "connectivity_code": "10"
        },
        {
            "id": "39",
            "identifier": "018fcedb-fbd5-70ff-9864-b81fcd00e410",
            "username": "dleite",
            "expiration": null,
            "change": "2024-05-31 11:03:13",
            "view": null,
            "hostname": "w2016",
            "management_ip": "10.66.33.15",
            "type": "SSH Key",
            "type_code": "1",
            "device_model": "Windows Server 2016",
            "device_type": "Server",
            "device_vendor": "Microsoft",
            "automatic_change": false,
            "connectivity": "RDP",
            "connectivity_code": "13"
        }
    ]
}

`

## Response body fields

* credentials - array of objects - Data of listed credentials.

&nbsp;&emsp;&emsp;&nbsp;→ id - int - Unique identification code of the credential.
&nbsp;&emsp;&emsp;Note: this value is assigned by senhasegura in POST | Create credential.

    
  


   &nbsp;&emsp;&emsp;&nbsp;→identifier - string - Unique string defined by the user or by senhasegura for identifying the credential.
&nbsp;&emsp;&emsp;Note: this value can be updated through the  POST api/pam/credential endpoint.



    &nbsp;&emsp;&emsp;&nbsp;→username - string - Username assigned to the credential.&nbsp;&emsp;&emsp;&nbsp;New credential default value: usr



    &nbsp;&emsp;&emsp;&nbsp;→expiration - string - Expiration date and time of the credential based on ISO 8601.
    &nbsp;&emsp;&emsp;&nbsp;Example: 2024-05-16T17:31:31-03:00




    &nbsp;&emsp;&emsp;&nbsp;→change  - string - Date and time of the last modification made to the credential based on ISO 8601.
    &nbsp;&emsp;&emsp;&nbsp;Example: 2024-05-03 16:19:53



    &nbsp;&emsp;&emsp;&nbsp;→view  - string - Date and time of the last view of the credential based on ISO 8601.
&nbsp;&emsp;&emsp;&nbsp;Example: 2024-05-24 16:26:09


 &nbsp;&emsp;&emsp;&nbsp;→hostname - string - Hostname of the device associated with the credential.
    
    
&nbsp;&emsp;&emsp;&nbsp;→management_ip - string - IP address used to manage the device or system associated with the credential.


    &nbsp;&emsp;&emsp;&nbsp;→type - string - Credential type.


&nbsp;&emsp;&emsp;&nbsp;→type_code - string - Code for credential type.


    &nbsp;&emsp;&emsp;&nbsp;→device_model - string - Model of the device associated with the credential. 


    &nbsp;&emsp;&emsp;&nbsp;→device_type - string - Type of device associated with the credential.


    &nbsp;&emsp;&emsp;&nbsp;→device_vendor - string - Manufacturer of the device associated with the credential. &nbsp;&emsp;&emsp;&nbsp;Example: Microsoft


    &nbsp;&emsp;&emsp;&nbsp;→automatic_change - boolean - Indicates if the credential is automatically changed.


    &nbsp;&emsp;&emsp;&nbsp;→connectivity - string - Type of credential connectivity.
    

    &nbsp;&emsp;&emsp;&nbsp;→connectivity_code - string - Code for the type of connectivity.
    
    
:::(Info) (Info)
Access the document  for descriptions of other credential parameters such as Execution settings, Session settings, Additional settings, and JIT settings.
:::
    
## Errors
    

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
