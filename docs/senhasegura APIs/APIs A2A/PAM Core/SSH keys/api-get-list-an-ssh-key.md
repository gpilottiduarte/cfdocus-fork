## Metadata_Start 
## code: en
## title: GET | List an SSH key by [id] 
## slug: api-get-list-an-ssh-key 
## seoTitle: GET | List an SSH key by [id] 
## description:  
## contentType: Markdown 
## Metadata_End

Access information of an SSH key registered in .

## Requirements
* Authorization with  permission to  granted by the administator in . 
Access the document on  for more information.



## Request

 GET 

## Request parameters

Send the parameter below in the path of the URL.


* id - int - required - Unique identification code of the SSH key.Note: this value is automatically assigned by senhasegura in POST | Create SSH key and is obtained in the response to  the GET | List all credentials request that lists all credentials accessible to your authorization.


  ### Example request

GET 
  
  
  
  ## Response 
 `json
HTTP/1.1 200 OK 
`
`json
{
    "code": 200,
    "response": {
        "status": 200,
        "message": "Key 39",
        "error": false,
        "error_code": 0,
        "detail": "",
        "Message": "Key 39",
        "erro": false,
        "cod_erro": 0
    },
    "tenant": "senhasegura",
    "key": {
        "id": "39",
        "username": "dleite",
        "key_name": "test2",
        "hostname": "w2016",
        "ip": "10.66.33.15",
        "private_key": "-----BEGIN OPENSSH PRIVATE KEY-----\r\cTA9Vb5aA0kXaK2HEjGUWgeCBG5vbmUAAAAEbm9uZQAAAAAAAAABAAAAMwAAAAtzc2gtZW\r\nQyNTUxOQAAACCLABE9/nb3BlbnNzaC1rZXktdjEAAAAAxtPOCkR2sGccAAAAKi5DXJnuQ1y\r\nZwAAAAtzc2gtZWQyNTUxOQAAACCLABE9/cTA9VTGVpdGVGZXJyZWlyYUBIUjFTUkb5aA0kXaK2HEjGUWgeCxtPOCkR2sGccA\r\nDgaNiGsvbkkkXhepU2NQi3iZ4sAET39xMD1VvloDSRdorYc\r\nSMZRaB4LG084KRHawZxwAAAAI0F6dXJlQUQrRGVib3JhAAAECc20zsB7FuSJQAqhLxe\r\ngzAQI=\r\n-----END OPENSSH PRIVATE KEY-----",
        "public_key": "ssh-ed25519 C1lZDI1NTE5AAawZxwAAAAAAC3NzaIIsAET39xdorYcSMZRaB4LG084MD1VvloDSRKRH AzureAD+DeboraLeiteFerreira@HR1SRH3",
        "password": null,
        "devices": [
            {
                "hostname": "API device test",
                "ip": "10.66.33.20"
            }
        ],
        "expiration_time": "2024-06-04T12:20:19"
    }
}
`

### Response body fields
 
     

* key - object  - SSH key data.


&nbsp;&emsp;&emsp;&nbsp;→id - int - Unique identification code of the SSH key.


&nbsp;&emsp;&emsp;&nbsp;→key_name - string - Username related to the key in the device.
    
 &nbsp;&emsp;&emsp;&nbsp;New SSH key default value: usr



    
  &nbsp;&emsp;&emsp;&nbsp;→hostname - string - Name of the main device associated with the SSH key.



    
&nbsp;&emsp;&emsp;&nbsp;→ip - string - IP address of the main device associated with the SSH key.



    
 &nbsp;&emsp;&emsp;&nbsp;→private_key - string - Private key necessary for user authentication.
    &nbsp;&emsp;&emsp;&nbsp;Example: -----BEGIN OPENSSH PRIVATE KEY-----\rcTA9Vb5aA0kXaK2HEjGUWgeCBG5vbmUAAAAEbm9uZQAAAAAAAAABAAAAMwAAAAtzc2gtZW\rQyNTUxOQAAACCLABE9/nb3BlbnNzaC1rZXktdjEAAAAAxtPOCkR2sGccAAAAKi5DXJnuQ1y\r\nZwAAAAtzc2gtZWQyNTUxOQAAACCLABE9/cTA9VTGVpdGVGZXJyZWlyYUBIUjFTUkb5aA0kXaK2HEjGUWgeCxtPOCkR2sGccA\rDgaNiGsvbkkkXhepU2NQi3iZ4sAET39xMD1VvloDSRdorYc\rSMZRaB4LG084KRHawZxwAAAAI0F6dXJlQUQrRGVib3JhAAAECc20zsB7FuSJQAqhLxe\rgzAQI=\r-----END OPENSSH PRIVATE KEY-----



  
  &nbsp;&emsp;&emsp;&nbsp;→public_key - string - Public key that allows servers to verify the user's identity associated with the corresponding private key.
    &nbsp;&emsp;&emsp;&nbsp;Example: ssh-ed25519 C1lZDI1NTE5AAawZxwAAAAAAC3NzaIIsAET39xdorYcSMZRaB4LG084MD1VvloDSRKRH AzureAD+DeboraLeiteFerreira@HR1SRH3



 
&nbsp;&emsp;&emsp;&nbsp;→password - string - Optional password that provides an extra layer of security to the private key.



&nbsp;&emsp;&emsp;&nbsp;→tags - string - Keywords for identifying the SSH key.



  
&nbsp;&emsp;&emsp;&nbsp;→devices - array of objects - Additional devices associated with the SSH key, containing hostname and ip.
    
&nbsp;&nbsp;&nbsp;&nbsp;&emsp;&emsp;&nbsp;&nbsp;&nbsp;&nbsp;→hostname - string - Hostname of the additional device associated with the SSH key.

 
&nbsp;&nbsp;&nbsp;&nbsp;&emsp;&emsp;&nbsp;&nbsp;&nbsp;&nbsp;→ip - string -  IP address of the additional device.


 &nbsp;&emsp;&emsp;&nbsp;→expiration_time - string - Expiration time of the SSH key based on ISO 8601.
&nbsp;&emsp;&emsp;&nbsp;Example: 2024-06-04T12:20:19



  
    
 ## Errors
 

 
400 - Bad Request

***

Message: "1015: SSH key not found"
Possible cause: the SSH key wasn’t found.
        
Solution: check the id sent to search for the SSH key and resend the request.

* * * 
 
 Message: "1016: The item is not a ssh key"
Possible cause: the value for the id parameter doesn’t correspond to an SSH key. 
        
Solution: check the id  and resend the request.

* * * 

    
Message: "1017: Key inactive"
Possible cause: the SSH key is inactive. 
        
Solution: activate the key through the endpoint PUT .

* * * 




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
        
Solution: ask the administrator to check your permission to access the PAM Core resources in A2A.

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
