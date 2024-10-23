## Metadata_Start 
## code: en
## title: POST | Enable note 
## slug: api-post-enable-note 
## seoTitle: POST | Enable note 
## description:  
## contentType: Markdown 
## Metadata_End
Enable a note in .

## Requirements
* Permission to edit the note.
* Inactive note in .

## Request

  POST 

### Request parameters

Send the parameter below in the path of the URL.

identifier - int - required - Note unique identification code.
Note: this value is automatically assigned by senhasegura in POST | Create note and is obtained in the response to the GET |List all notes request.

 ### Example request

 POST 

### Response



 
`json
{
    "code": 200,
    "response": {
        "status": 200,
        "message": "Note successfully activated",
        "error": false,
        "error_code": 0,
        "detail": "",
        "mensagem": "Note successfully activated",
        "erro": false,
        "cod_erro": 0
    }
}
`


:::(Info) (Info)
If the note is already active, the call will return a  response code with the message .
:::



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

     
     