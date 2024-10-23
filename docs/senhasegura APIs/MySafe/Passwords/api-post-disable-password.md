## Metadata_Start 
## code: en
## title: POST | Disable password 
## slug: api-post-disable-password 
## seoTitle: POST | Disable password 
## description:  
## contentType: Markdown 
## Metadata_End
Disabled a password in .

## Requirements
* Permission to edit the password.
* An active password in .


## Request


  POST 

## Request parameters
Send the parameter below in the  of the URL.

* identifier - int - required - Unique identification code of the password.Note: this value is automatically assigned by senhasegura in POST | Create password and is obtained in the response to the GET | List all passwords.

### Example request

 POST 
  
  ## Response

 `json
HTTP/1.1 200 OK
` 
 
`json
{
    "code": 200,
    "response": {
        "status": 200,
        "message": "Password successfully deactivated",
        "error": false,
        "error_code": 0,
        "detail": "",
        "mensagem": "Password successfully deactivated",
        "erro": false,
        "cod_erro": 0
    }
}
`
 
:::(Info) (Info)
If the password is already inactive, the call will return a  response code with the message .".
:::

 ## Errors


400 - Bad Request.

* * *
Message: "1005: Password not found"
Possible cause: the password wasn't found.
Solution: check the value for the identifier and resend the request.

    
* * *
    
Message: "1006: User does not have access"
Possible cause: user isn't allowed to access the item.

 ***
 
    

    500 - Internal Server Error.

***
    
Message: "Unexpected error."

Possible cause: the error is in the senhasegura server.
        
Solution: contact the support team for more information.
    
 ***
 
 
 
    No route matched with those values.

 ***
    
Message: "You are not authorized to access this resource."
Possíveis causas: failure in your application authentication with the senhasegura server.
        
Solution: check the authentication parameters such as Access Token URL, Client ID and  Client Secret and request a new access token or check and correct the URL. 
* * *

     

An invalid response was received from the upstream server
.

*** 
   
Message: "An invalid response was received from the a seupstream server
    
Possible cause: the upstream server may be taking too long to respond, leading to a timeout error that is interpreted as an invalid response by the proxy/gateway server.
        
Solution: check the connectivity between the source of the request and the senhasegura server.
***

     
   


The upstream server is timing out.

*** 
    
Message: "The upstream server is timing out"
    
Possible cause: the request time has expired.
        
Solution: check the connectivity between the source of the request and the senhasegura server.
* * *



     