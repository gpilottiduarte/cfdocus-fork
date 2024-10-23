## Metadata_Start 
## code: en
## title: GET | List an API secret by [identifier] 
## slug: api-get-list-an-api-secret 
## seoTitle: GET | List an API secret by [identifier] 
## description:  
## contentType: Markdown 
## Metadata_End
Access information of an API secret stored .

## Requirements
* API secret access in .
 
## Request

  GET 



## Request parameters
Send the parameter below in the  of the URL.

identifier - int - required - API secret unique identification code.
Note: this value is automatically assigned by senhasegura in POST | Create API secret and is obtained in the response to the GET | List all API secrets.




  ### Example request
 GET .
  
  ## Response
 `json
HTTP/1.1 200 OK
` 
 
`json
{
    "code": 200,
    "response": {
        "status": 200,
        "message": "Success",
        "error": false,
        "error_code": 0,
        "detail": "",
        "Message": "Success",
        "erro": false,
        "cod_erro": 0
    },
    "api_secret_entity": {
        "identifier": "3",
        "name": "GCP1",
        "url": "https://gcp1.com",
        "client_secret": "hy7464g5v8ghy4d858jk7fds57t4tr",
        "client_id": "hb455f7g8fg9dfg8yt845bxxku",
        "identifier_code": "12534",
        "method": "get",
        "tags": "Cloud1",
        "notes": "Access details for this API secret",
        "users_allowed": [
            {
                "name": "alices",
                "can_edit": true
            }
        ],
        "groups_allowed": []
    }
}
`
### Reponse body fields

&#8226; api_secret_entity - object - Data of the stored API secret.


&nbsp;&emsp;&emsp;&nbsp;→ identifier - int - API secret unique identification code.
    

&nbsp;&emsp;&emsp;&nbsp;→ name - string - Name assigned to the API secret.


&nbsp;&emsp;&emsp;&nbsp;→ url - string - required - URL of the website where the API secret will be used.


&nbsp;&emsp;&emsp;&nbsp;→ client_secret - string  - The secret used to the authenticate the application.



&nbsp;&emsp;&emsp;&nbsp;→ client_id - string - required - ID of the client application. 



&nbsp;&emsp;&emsp;&nbsp;→ dentifier_code - string - Unique string defined by the user to identify the API secret.

 
&nbsp;&emsp;&emsp;&nbsp;→ method - string - The HTTP method to be used in the API call. 

 
&nbsp;&emsp;&emsp;&nbsp;→ notes - string - Observations about the API secret.


&nbsp;&emsp;&emsp;&nbsp;→ tags - string - Keywords associated with the API secret.



&nbsp;&emsp;&emsp;&nbsp;→ users_allowed - array of objects - Data of the users with access to the API secret.



&nbsp;&emsp;&emsp;&nbsp;→ groups_allowed - array of objects - Data of the groups with API secret access.


    

## Errors
 

400 - Bad Request.

***
Message: "1010: Unexpected identifier type"
Possible cause: the identifier provided wasn't recognized as valid.
Solution: check the value of the identifier and resend the request.
  
* * *
Message: "1005: Api secret not found"
Possible cause: the API secret wasn't found.
Solution: check the value of the identifier and resend the request.

    
* * *
    
Message: "1006: User does not have access"
Possible cause: user doesn't have access to the API secret.

 ***
Message: "1009: Inactive Api secret"
Possible cause: inactive API secret.
 Solution: enable the API secret through the path  POST api/mysafe/password/active[identifier].

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


     