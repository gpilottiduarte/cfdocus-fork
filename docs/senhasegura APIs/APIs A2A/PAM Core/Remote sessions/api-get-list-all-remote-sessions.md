## Metadata_Start 
## code: en
## title: GET | List all remote sessions 
## slug: api-get-list-all-remote-sessions 
## seoTitle: GET | List all remote sessions 
## description:  
## contentType: Markdown 
## Metadata_End
Access information of proxy sessions registered in .

## Requirements
*  Authorization with  permission to  granted by the administrator in .
Access the document on  for more information.
* Remote sessions registered in .
Access the document on  for more information.

## Request

  GET 

## Example request

  GET 



## Response

:::(Warning) (Attention)
Depending on the number of sessions registered in the environment, the returned list can be very long and the response time may take a few minutes.
:::

` json
HTTP/1.1 200 OK
`

` json
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
    "remote_sessions": [
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
    "tenant": "senhasegura",
    "remote_sessions": [
        {
            "id": "3",
            "user": "Admin",
            "origin_ip": "172.16.20.125",
            "credential": "usrdomadm01",
            "device": "10.66.33.15:3389",
            "protocol": "rdp",
            "proxy": "Web Proxy",
            "session_id": "e7acacb6aedbab70073456da5744166939b77527",
            "start": "2024-05-06 16:05:07",
            "end": "2024-05-06 16:07:59",
            "time": "00:02:52",
            "prevent_purge": "No",
            "request": null,
            "ITSM": null
        },
        {
            "id": "6",
            "user": "Admin",
            "origin_ip": "172.16.20.125",
            "credential": "usrsudonopass",
            "device": "10.66.33.17:22",
            "protocol": "ssh",
            "proxy": "Web Proxy",
            "session_id": "c819cbc5f2fad2065f1d132a22d0e2dfacccb228",
            "start": "2024-05-06 16:11:17",
            "end": "2024-05-06 16:11:30",
            "time": "00:00:13",
            "prevent_purge": "No",
            "request": null,
            "ITSM": null
        }
    ]
 }
`


### Response body fields

remote_sessions - array of objects - Data of the listed remote sessions.


&nbsp;&emsp;&emsp;&nbsp;→id - int - Unique identification code for the remote session.&nbsp;&emsp;&emsp;&nbsp;Note: this value is automatically assigned by senhasegura when the session is created and should not be confused with the session_id parameter.


&nbsp;&emsp;&emsp;&nbsp;→user - string - Username used for authentication.


&nbsp;&emsp;&emsp;&nbsp;→origin_ip - string - IP address of the session's originating device.


&nbsp;&emsp;&emsp;&nbsp;→credential - string - Credential used for the session.


&nbsp;&emsp;&emsp;&nbsp;→device - string - Hostname or IP address of the target device.
  

&nbsp;&emsp;&emsp;&nbsp;→protocol - string - Network protocol (SSH, RDP, HTTPS, among others).


&nbsp;&emsp;&emsp;&nbsp;→proxy - string - Type of proxy session.


&nbsp;&emsp;&emsp;&nbsp;→session_id - string - Unique hash generated by senhasegura to exclusively identify a specific session.&nbsp;&emsp;&emsp;&nbsp;Example: e7acacb6aedbab70073456da5744166939b77527

&nbsp;&emsp;&emsp;&nbsp;Note: this identifier is used internally by the application for operations related to the session, such as access control, activity tracking, and resource management. Each time a session is started, a new session_id is generated for that specific session.


&nbsp;&emsp;&emsp;&nbsp;→start - string - Start date and time of the session in ISO 8601 format.
&nbsp;&emsp;&emsp;&nbsp;Example: 2024-05-06 16:05:07


&nbsp;&emsp;&emsp;&nbsp;→end - string - End date and time of the session in ISO 8601 format.
&nbsp;&emsp;&emsp;&nbsp;Example: 2024-05-06 16:07:59


&nbsp;&emsp;&emsp;&nbsp;→time - string - Duration of the session.
&nbsp;&emsp;&emsp;&nbsp;Example: 00:02:52


&nbsp;&emsp;&emsp;&nbsp;→prevent_purge - string - Indicates whether the session data will be automatically deleted.
&nbsp;&emsp;&emsp;&nbsp;Example: No


&nbsp;&emsp;&emsp;&nbsp;→request - string - Request made by the user.


&nbsp;&emsp;&emsp;&nbsp;→ITSM - string - ITSM software code.


 ## Errors
 

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
        
Solution: ask the administrator to check your permission to access the Web Proxy Session resources in A2A.

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

