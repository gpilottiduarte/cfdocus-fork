## Metadata_Start 
## code: en
## title: GET | List all API secrets 
## slug: api-get-list-all-api-secrets 
## seoTitle: GET | List all API secrets 
## description:  
## contentType: Markdown 
## Metadata_End
Access information of API secrets stored .


## Request

  GET 



## Request parameters
Send the parameters below as  in the URL.

* tag - string - Filters API secrets by the tag registered.
* identifier_code - string - Filters API secrets by their identifier.




  ### Example request
 GET  - Lists all API secrets.

 GET  - Lists API secret(s) registered with the = .

 GET  - Lists API secret(s) registered with the = .
  
  
  ## Response
 `json
HTTP/1.1 200 OK
` 
 
`json
{
    "code": 200,
    "response": {
        "status": 200,
        "message": "",
        "error": false,
        "error_code": 0,
        "detail": "",
        "mensagem": "",
        "erro": false,
        "cod_erro": 0
    },
    "api_secret_on_list": [
        {
            "identifier": "3",
            "name": "GCP1",
            "need_justify": "0",
            "need_approval": "0",
            "can_view": true,
            "can_write": true
        },
        {
            "identifier": "4",
            "name": "GCP",
            "need_justify": "1",
            "need_approval": "1",
            "can_view": true,
            "can_write": true
        },
        {
            "identifier": "5",
            "name": "GCP1",
            "need_justify": "0",
            "need_approval": "0",
            "can_view": true,
            "can_write": true
        }
    ]
}
`
### Reponse body fields

&#8226; api_secret_on_list - array of objects - Data of the stored API secrets.


&nbsp;&emsp;&emsp;&nbsp;→ identifier - int - API secret unique identification code.
    

&nbsp;&emsp;&emsp;&nbsp;→ name - string - Name assigned to the API secret.


 &nbsp;&emsp;&emsp;&nbsp;→ can_view - string - Permission to view the API secret.
 
   
&nbsp;&emsp;&emsp;&nbsp;→ can_write - string - Permission to edit the API secret.

## Errors
 
    

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


     