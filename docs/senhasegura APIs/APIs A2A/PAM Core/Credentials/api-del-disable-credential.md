## Metadata_Start 
## code: en
## title: DEL | Disable credential 
## slug: api-del-disable-credential 
## seoTitle: DEL | Disable credential 
## description:  
## contentType: Markdown 
## Metadata_End
Disable a credential in .

## Requirements
* Authorization with  and  permission to  granted by the administrator in .
Access the document on  for more information.
* An enabled credential in . 
Access the document  for more information.

## Disable credential by  - Request

  DEL 

## Request parameters

Send the parameter below in the path of the URL.

* id - int - required - Unique identification code of the credential.
    Note: this value is automatically assigned by senhasegura in POST | Create SSH key and is obtained in the response to the  GET /api/pam/credential which lists all credentials accessible to your authorization. 
    
### Example request

 DEL 

## Response

`json
HTTP/1.1 200 OK
`

 
`json
{
    "code": 200,
    "response": {
        "status": 200,
        "message": "Credential successfully deactivated",
        "error": false,
        "error_code": 0,
        "detail": "",
        "mensagem": "Credential successfully deactivated",
        "erro": false,
        "cod_erro": 0
    }
}
`

## Disable credential by  - Request

  DEL 

## Request parameters

Send the parameter below in the path of the URL.

* username@hostname - int -  required - username and  hostname associated with the credential separated by an @ symbol. Note: these values are provided by the user in POST | Create credential  and are obtained in the response to the  GET | List all credentials request. Example: credential_5@destktop-91.com
    
### Example request

 DEL 

### Response

`json
HTTP/1.1 200 OK
`

 
`json
{
    "code": 200,
    "response": {
        "status": 200,
        "message": "Credential successfully deactivated",
        "error": false,
        "error_code": 0,
        "detail": "",
        "mensagem": "Credential successfully deactivated",
        "erro": false,
        "cod_erro": 0
    }
}
`
## Errors


400 - Bad Request
 
* * *
    
Message: "1007: Credential not found"

Possible cause: the credential wasn’t found.
        
Solution: check if the values for the parameters used to search for the credential were correct and resend the request.
    
 ***
    
 Message: "1008: Credential inactive"
Possible cause: the credential is already inactive.
    
***
    
Message: "1009: No access to credential"

Possible cause: you’re not authorized to access the credential.
        
Solution: ask the administrator to check your permission to access the credential.
    
***
    
Message: "1010: The item is not a credential"

Possible cause: the value for the id parameter doesn’t belong to a credential.
        
Solution: check the id and resend the request.
***
 
Message: "1039: Without PAM Configuration Access permission"  
Possible cause: your authorization doesn’t have permission to disable a device.

Solution: ask the administrator to check your read and write permission to PAM Core resources in A2A.


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
