## Metadata_Start 
## code: en
## title: GET | List all notes 
## slug: api-get-list-all-notes 
## seoTitle: GET | List all notes 
## description:  
## contentType: Markdown 
## Metadata_End
Access information of notes stored in .


## Request


  GET 


## Query parameters
Send the parameters below in the  of the URL. 

* tag - string - Filter notes by tags.
* name - string -Filters notes by name.


### Example requests

 GET   - Gets all notes.

 GET  - Gets the note(s) registered with the  = .

 GET  - Gets the note(s) registered with the  = .
  
  
  ## Response 
`
HTTP/1.1 200 OK
`

`
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
    "note_on_list": [
        {
            "identifier": "1",
            "name": "My note",
            "tags": "",
            "need_justify": "0",
            "need_approval": "0",
            "can_view": true,
            "can_write": true
        },
        {
            "identifier": "2",
            "name": "Secret note",
            "tags": "secret",
            "need_justify": "0",
            "need_approval": "0",
            "can_view": true,
            "can_write": true
        },
        {
            "identifier": "6",
            "name": "Staff meeting decisions",
            "tags": "meeting",
            "need_justify": "0",
            "need_approval": "0",
            "can_view": true,
            "can_write": true
        },
        {
            "identifier": "9",
            "name": "TC Meeting",
            "tags": "API, MySafe, TC",
            "need_justify": "0",
            "need_approval": "0",
            "can_view": true,
            "can_write": true
        }
     ]
}
`
 
 ### Response body fields

    
&#8226; notes_on_list - array of objects - Data of the stored notes.


&nbsp;&emsp;&emsp;&nbsp;→ identifier - int - Note unique identification code.
    

&nbsp;&emsp;&emsp;&nbsp;→ name - string - Note name.


&nbsp;&emsp;&emsp;&nbsp;→ tags - string - Keywords associated with the note.


 &nbsp;&emsp;&emsp;&nbsp;→ can_view - string - Permission to view the note.
 
   
&nbsp;&emsp;&emsp;&nbsp;→ can_write - string - Permission to edit the note.
 
   


 ## Errors
 
    

500 - Internal Server Error

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

     

