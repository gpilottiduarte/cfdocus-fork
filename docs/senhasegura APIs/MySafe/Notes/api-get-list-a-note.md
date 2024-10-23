## Metadata_Start 
## code: en
## title: GET | List a note by [identifier] 
## slug: api-get-list-a-note 
## seoTitle: GET | List a note by [identifier] 
## description:  
## contentType: Markdown 
## Metadata_End
Access a note information in .



## Request


  GET 


## Request parameters
Send the parameter below in the path of the URL.

identifier - int - required - Note unique identification code.
Note: this value is automatically assigned by senhasegura in POST | Create note and is obtained in the response to the GET | List all notes request.


  ### Example request

GET 
  
  
  
  ## Response

 `
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
        "mensagem": "Success",
        "erro": false,
        "cod_erro": 0
    },
    "note_entity": {
        "identifier": "2",
        "name": "Secret note",
        "note": "My top secret note",
        "tags": "secret",
        "users_allowed": [],
        "groups_allowed": []
    }
}
`

### Response body fields

    
&#8226; notes_entity - object - Data of the stored note.


&nbsp;&emsp;&emsp;&nbsp;→ identifier - int - Note unique identification code.
    

&nbsp;&emsp;&emsp;&nbsp;→ name - string - Note name.


&nbsp;&emsp;&emsp;&nbsp;→ tags - string - Keywords associated with the note.


&nbsp;&emsp;&emsp;&nbsp;→ users_allowed - array of objects - List of users' names and permissions to view and/or edit the note.
 
 
   
&nbsp;&emsp;&emsp;&nbsp;→ groups_allowed - array of objects - List of groups' names and permissions to view and/or edit the note.
 
   



 
 ## Errors
 

400 - Bad request.

***
    
Message: "1006 User does not have access"

Possible cause: user doesn't have access to this note.
    
 ***    
Message: "1010: Unexpected identifier type"

Possible cause: URL not recognized.
 Solution: check the URL and resend the request .
          
    
 ***


500 - Internal Server Error.

***
    
***
Message: "Unexpected error."
Possible cause: the error is on the senhasegura server.
Solution: contact the support team for more information.

***



No route matched with those values.

***
Message: "No route matched with those values."
Possible causes: failure in your application's authentication with the senhasegura server or incorrect URL.
Solution: check the authentication parameters such as Access Token URL, Client ID, and Client Secret and request a new access token or check and correct the URL.

***



An invalid response was received from the upstream server.

***
Message: "An invalid response was received from the upstream server."
Possible cause: the upstream server may be taking too long to respond, leading to a timeout error interpreted as an invalid response by the proxy/gateway server.
Solution: check the connectivity between the request origin and the senhasegura server.

***



The upstream server is timing out.

***
Message: "The upstream server is timing out."
Possible cause: the request timed out.
Solution: check the connectivity between the request origin and the senhasegura server.

***

     
     