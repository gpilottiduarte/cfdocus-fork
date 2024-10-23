## Metadata_Start 
## code: en
## title: POST | Enable API secret 
## slug: api-post-enable-api-secret 
## seoTitle: POST | Enable API secret 
## description:  
## contentType: Markdown 
## Metadata_End
Enable an API secret in .

## Requirements
* Permission to edit the API secret.
* A disabled API secret in .

## Request

 POST 



## Request parameters
Send the parameter below in the  of the URL.

identifier - int - required - API secret unique identification code.
Note: this value is automatically assigned by senhasegura in POST | Create API secret and is obtained in the response to the GET | List all API secrets.


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
        "message": "Api secret activated successfully",
        "error": false,
        "error_code": 0,
        "detail": "",
        "mensagem": "Api secret activated successfully",
        "erro": false,
        "cod_erro": 0
    }
}
`

:::(Info) (Info)
If the API secret is already active, the call will return a  response code with the message .
:::
 
## Errors
 

400 - Bad Request.

***
Message: "1005: Api secret not found"
Possible cause: Api secret wasn't found
Solution:  check the value for the identifier and resend the request.

    
* * *
    
Message: "1006: User does not have access"
Possible cause: user doesn't have access to the API secret.

 ***

    

    500 - Internal Server Error.

***
    
Message: "Unexpected error."

Possible cause: the error is on the senhasegura server.
        
Solution: contact the support team for more information.
    
 ***
 
 
 
    No route matched with those values.

 ***
    
Message: "No route matched with those values."
Possible causes: failure in your application authentication with the senhasegura server or incorrect URL.
        
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


     