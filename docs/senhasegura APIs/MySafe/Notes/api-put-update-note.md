## Metadata_Start 
## code: en
## title: PUT | Update note 
## slug: api-put-update-note 
## seoTitle: PUT | Update note 
## description:  
## contentType: Markdown 
## Metadata_End
Update a note in .

## Requirements
* Permission to edit the note in .

## Request

  PUT 



## Request parameters
Send the parameter below in the path of the URL.


identifier - int - required - Unique identification of the note.

Nota: this value is automatically assigned by senhasegura in POST | Create note and is obtained in the response to the GET | List all notes.


    
Send the parameters you want to update in the request body.

* name - string - Name assigned to the note.



* note - string  - The content of the note, limited to 900 characters. 
    
:::(Error) (Important!)
Notes whose content exceeds 900 characters will result in error.
:::



* tags - string - Keywords associated with the note.



* users_allowed - array of objects - Data of users allowed to access the note.



&nbsp;&emsp;&emsp;&nbsp;→username - string - Name of the user allowed to access the note.



&nbsp;&emsp;&emsp;&nbsp;→can_edit - boolean - Edit permission. 

&nbsp;&emsp;&emsp;&nbsp;Note: if left empty, users will have view-only permission.

:::(Warning) (Attention)
Users with can_edit = true permission can deactivate the note.
:::



* groups_allowed - array of objects - Data of groups allowed to access the note.



&nbsp;&emsp;&emsp;&nbsp;→name - string - Name of the group allowed to access the note.



&nbsp;&emsp;&emsp;&nbsp;→can_edit - boolean - Edit permission. 

&nbsp;&emsp;&emsp;&nbsp;Note: if left empty, group members will have view-only permission.

:::(Warning) (Attention)
Group members with can_edit = true permission can deactivate the note.
:::
### Example request

 PUT 

`json
{
   
    "users_allowed": [
        {
            "username" : "pduarte",
            "can_edit" : false
        }
    ]
}

`

## Response

`json
HTTP/1.1 200 OK
`
`json
{
    "code": 200,
    "response": {
        "status": 200,
        "message": "Note successfully update",
        "error": false,
        "error_code": 0,
        "detail": "",
        "mensagem": "Note successfully update",
        "erro": false,
        "cod_erro": 0
    },
    "note_entity": {
        "identifier": "2",
        "name": "Secret note",
        "tags": "secret",
        "users_allowed": [
            {
                "username": "pduarte",
                "can_edit": false
            }
        ],
        "groups_allowed": [],
        "shared_error": []
    }
}

`

## Errors


400 - Bad Request


* * *
Message: "1001: Parameter note limited to 900 characters"
Possible cause: the content sent in note exceeded the limit of 900 characters.
Solution: reduce the content of the note and resend the request.

* * *    



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
