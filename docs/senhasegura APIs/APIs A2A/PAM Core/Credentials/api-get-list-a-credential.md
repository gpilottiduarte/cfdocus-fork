## Metadata_Start 
## code: en
## title: GET | List a credential 
## slug: api-get-list-a-credential 
## seoTitle: GET | List a credential 
## description:  
## contentType: Markdown 
## Metadata_End
Access information of a credential registered in .

## Requirements

* Authorization with  permission to  granted by the administator in . 
Access the document on  for more information.
* Credential created in . 
Access the document  for more information.

## List credential by  - Request

 GET 

### Request parameters

Send the parameter below in the  of the URL.

* id - int -  required - Unique identification code of the credential.Note: this value is automatically assigned by senhasegura in POST | Create credential and is obtained in the response to the  GET | List all credentials request. 

### Example request
 GET 

## Response 

`json 
HTTP/1.1 200 OK
`

` json
{
    "response": {
        "status": 200,
        "mensagem": "Credential 5",
        "erro": false,
	 "detail": "",
        "message": "Credential 5",
        "error": false,
	 "error_code": 0
    },
    "credential": {
        "id": "5",
        "identifier": "robot-test-5",
        "username": "credential_5",
        "password": "secret@2504",
        "content": "secret@2504",
        "hostname": "destktop-91.com",
        "parent_credential_cod": null,
        "parent_credential": null,
        "additional": "CREDADD01",
        "domain": "",
        "ip": "172.10.10.90",
        "port": "22",
        "model": "Ubuntu",
        "expiration_time": "2021-01-16T17:31:39"
    }
`

## List credential by  - Request

 GET 

### Request parameters

Send the parameter below in the  of the URL.

* username@hostname - int -  required - username and  hostname associated with the credential separated by an @ symbol. Note: these values are provided by the user in POST | Create credential  and are obtained in the response to the  GET | List all credentials request. Example: credential_5@destktop-91.com

### Example request
 GET 

:::(Warning) (Attention)
If the  provided has an @ in it, as in , the endpoint won’t work as expected due to the conflict caused by the presence of two @ symbols. 
:::

`json 
HTTP/1.1 200 OK
`

` json
{
    "response": {
        "status": 200,
        "mensagem": "Credential 5",
        "erro": false,
	 "detail": "",
        "message": "Credential 5",
        "error": false,
	 "error_code": 0
    },
    "credential": {
        "id": "5",
        "identifier": "robot-test-5",
        "username": "credential_5",
        "password": "secret@2504",
        "content": "secret@2504",
        "hostname": "destktop-91.com",
        "parent_credential_cod": null,
        "parent_credential": null,
        "additional": "CREDADD01",
        "domain": "",
        "ip": "172.10.10.90",
        "port": "22",
        "model": "Ubuntu",
        "expiration_time": "2021-01-16T17:31:39"
    }
`
## Response body fields

* credential - object - Credential data.

&nbsp;&emsp;&emsp;&nbsp;→ id - int - Unique identification code of the credential.


&nbsp;&emsp;&emsp;&nbsp;→identifier - string - Unique string defined by the user or senhasegura for identifying the credential.
&nbsp;&emsp;&emsp; Note: this value can be updated through the  POST api/pam/credential endpoint.


&nbsp;&emsp;&emsp;&nbsp;→username - string - Username assigned to the credential.


&nbsp;&emsp;&emsp;&nbsp;→expiration - string - Expiration date and time of the credential based on ISO 8601.


&nbsp;&emsp;&emsp;&nbsp;→password - string - Password assigned to the credential.
    
        
&nbsp;&emsp;&emsp;&nbsp;→content - string - Password assigned to the credential.
    
        
&nbsp;&emsp;&emsp;&nbsp;→hostname - string - Hostname of the device associated with the credential.
    
        
&nbsp;&emsp;&emsp;&nbsp;→parent_credential_cod - string - Parent credential’s identifier.
    
 
&nbsp;&emsp;&emsp;&nbsp;→parent_credential - string - Parent credential.
&nbsp;&emsp;&emsp;&nbsp;Note: when you select a parent credential, the child credential will assume the same password as the parent credential. Whenever there is a manual or automated password change on the parent credential, the child credential will also be modified and assume the same password as the parent credential.
  

&nbsp;&emsp;&emsp;&nbsp;→additional - string - Additional information about the credential.
    

 
&nbsp;&emsp;&emsp;&nbsp;→domain - string - Domain’s name or abbreviation.    

 
&nbsp;&emsp;&emsp;&nbsp;→ip - string - IP address of the device associated with the credential.


 &nbsp;&emsp;&emsp;&nbsp;→port - string - Port of the device associated with the credential.


&nbsp;&emsp;&emsp;&nbsp;→port - string - Port of the device associated with the credential.


 &nbsp;&emsp;&emsp;&nbsp;→model - string - Device model. 


&nbsp;&emsp;&emsp;&nbsp;→expiration_time - string - Date and time of credential expiration based on ISO 8601.&nbsp;&emsp;&emsp;&nbsp;Example: 2024-05-16T17:31:31-03:00
    
 

## Errors
    

400 - Bad Request

***
    
Message: "1007: Credential not found"

Possible cause: the credential wasn’t found.
        
Solution: check if the values for the parameters used to search for the credential were correct and resend the request.
    
 ***
    
Message: "1009: No access to credential"

Possible cause: you’re not authorized to access the credential.
        
Solution: ask the administrator to check your permission to access the credential.
    
***
    
Message: "1010: The item is not a credential"

Possible cause: the value for the id parameter doesn’t belong to a credential.
        
Solution: check the id and resend the request.
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
