## Metadata_Start 
## code: en
## title: GET | List all passwords 
## slug: api-get-list-all-passwords 
## seoTitle: GET | List all passwords 
## description:  
## contentType: Markdown 
## Metadata_End
Access information of passwords stored in .


## Request


  GET 

## Query parameters
Send the parameters below as URL .

* tag - string - Filters passwords by the tag registered.
* name - string - Filters passwords by their name.
* username - string - Filters passwords by the username registered.
* url - string - Filters passwords by the URL registered.


### Example request

 GET   -  Lists all passwords.

 GET  - Lists password(s) registered with the = .

 GET  - Lists password(s) registered with the = .

 GET  Lists password(s) registered with the = .

 GET - Lists password(s) registered with the = .
  
  
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
    "password_on_list": [
        {
            "identifier": "3",
            "name": "Github",
            "url": "https://github.com",
            "username": "deboraleitef@gmail.com",
            "tags": "",
            "need_justify": "0",
            "need_approval": "0",
            "can_view": true,
            "can_write": true
        },
        {
            "identifier": "4",
            "name": "gmail personal",
            "url": "www.gmail.com",
            "username": "user@gmail.com",
            "tags": "gmail",
            "need_justify": "0",
            "need_approval": "0",
            "can_view": true,
            "can_write": true
        },
        {
            "identifier": "5",
            "name": "gmail corporate",
            "url": "www.gmail.com",
            "username": "corporateuser@gmail.com",
            "tags": "gmail",
            "need_justify": "0",
            "need_approval": "0",
            "can_view": true,
            "can_write": true
        },
        {
            "identifier": "6",
            "name": "senhasegura",
            "url": "www.senhasegura.com",
            "username": "dleite",
            "tags": "senhasegura",
            "need_justify": "0",
            "need_approval": "0",
            "can_view": true,
            "can_write": true
        }
    ]
}
`
 
 ### Response body fields

    
&#8226; passwords_on_list - array of objects - Data of the saved passwords.


&nbsp;&emsp;&emsp;&nbsp;→ identifier - string - Numeric unique identification code of the password.
    

&nbsp;&emsp;&emsp;&nbsp;→ name - string - Name of the password.


&nbsp;&emsp;&emsp;&nbsp;→ url - string - URL of the website where the password is being used.


&nbsp;&emsp;&emsp;&nbsp;→ username - string Username used to access the account.



&nbsp;&emsp;&emsp;&nbsp;→ password - string - The password that's being added.



&nbsp;&emsp;&emsp;&nbsp;→ secret_key - string - The secret key provided for multi-factor authentication.


&nbsp;&emsp;&emsp;&nbsp;→ token - string - The TOTP code generated by senhasegura for multi-factor authentication based on the secret key provided in POST | Create password.


 &nbsp;&emsp;&emsp;&nbsp;→ tags - string - Keywords associated with the password.


 &nbsp;&emsp;&emsp;&nbsp;→ users_allowed - string - array of objects - Data of the users with password access.
 
   
&nbsp;&nbsp;&nbsp;&nbsp;&emsp;&emsp;&nbsp;&nbsp;&nbsp;&nbsp;→ username - string - Name of the user with password access permission.
    
     
&nbsp;&nbsp;&nbsp;&nbsp;&emsp;&emsp;&nbsp;&nbsp;&nbsp;&nbsp;→ can_write - boolean - Editing permission.


:::(Warning) (Attention)
Users with can_write = true permission can disable the password.
:::
    
 
 &nbsp;&emsp;&emsp;&nbsp;→ groups_allowed - string - array of objects - Data of the groups with password access.
 
   
&nbsp;&nbsp;&nbsp;&nbsp;&emsp;&emsp;&nbsp;&nbsp;&nbsp;&nbsp;→ name - string - Name of the group with password access permission.
    
     
&nbsp;&nbsp;&nbsp;&nbsp;&emsp;&emsp;&nbsp;&nbsp;&nbsp;&nbsp;→ can_write - boolean - Editing permission.


:::(Warning) (Attention)
Group members with can_write = true permission can disable the password.
:::
    

 ## Errors
 
    

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



     