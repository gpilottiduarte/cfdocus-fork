## Metadata_Start 
## code: en
## title: How to authenticate an application 
## slug: a2a-how-to-authenticate-an-application 
## seoTitle: How to authenticate an application 
## description:  
## contentType: Markdown 
## Metadata_End
This tutorial will guide you through a step-by-step on how to authenticate an application created in the  module in a REST or HTTP client of your choice.

senhasegura’s  APIs support ,  , and  authentication methods. 

:::(Info) (Info)
senhasegura recommends the use of  authentication for enhanced security.
:::

## OAuth v1.0 authentication

 is an authentication method that uses a set of , , , and  to identify and authorize application access.

## Requirements

A previously registered application using  as the authentication method and a previously registered authorization for this application. For more information, access the documentation on  and .


### Obtain OAuth v1.0 request parameters

In order to initiate requests using , you must provide the following information:

* 

* 

* 

* 

To find the values for the parameters mentioned above, follow the steps below:

1. On the senhasegura platform, in the upper left corner, click the , identified by the nine squares, and select .

1. In the side menu, select .

1. From the list, select the desired application and, in the  column, click the three vertical dots to open a drop-down menu.

1. In the drop-down menu, click .

1. In the  window, select the desired authorization, and in the  column, click , identified by the key icon.

1. In the  window, click the eye icons to view the , ,  and the .

### Make a request using OAuth v1.0

There are numerous ways to make an authentication request using . 
In the following example, Python is being used to demonstrate it. 

Use the following script:

`
import requests
import urllib3
from requests_oauthlib import OAuth1


def make_oauth1_request():
    url = "https:///"
    consumer_key = "CONSUMER_KEY"
    consumer_secret = "CONSUMER_SECRET"
    token_key = "TOKEN_KEY"
    token_secret = "TOKEN_SECRET"


    oauth = OAuth1(consumer_key, consumer_secret, token_key, token_secret)


    try:
        response = requests.get(url, auth=oauth, verify=False)
        if response.status_code == 200:
            print("Request was successful!")
            print("Response:")
            print(response.text)
        else:
            print("Request failed with status code:", response.status_code)
    except requests.exceptions.RequestException as e:
        print("An error occurred:", e)


if  == "":
    urllib3.disable_warnings()
    make_oauth1_request()
`
:::(Info) (Info)
When executing a request, replace the  field with the desired senhasegura endpoint. E.g., 
`
/iso/pam/credential
`
or 
`
/iso/pam/device
`

The parameters - , , , and  - previously obtained must be inserted in the header of the request, and not in the body.
:::
    

  
The following table presents a list with the mandatory and optional authentication parameters.
    
    

| Field | Description |
| --- | --- |
| * | A string of unique characters that act as a signature for a request. For more information, go to the documentation for . |
| * | Make sure to set the version value to 1.0. |
| * | The name of the signature method used by the client to sign the request. Set the signature method to . |
| * | The  value previously obtained. |
| * | The  value previously obtained. |
| * | The  value previously obtained. |
| * | The  value previously obtained. |
|   | A unique and random value generated by the client for each request. |
|  | The number of seconds since January 1, 1970, 00:00:00 GMT, responsible for generating a date signature. |

    
:::(Info) (Info)
The parameters marked with an asterisk are mandatory.
For more information on the parameters above, access T.
:::

##     OAuth v2.0 authentication
    
  is an authentication method that uses a  and a  to request a time-limited token and access senhasegura resources. 
    
## Requirements
 
A previously registered application using  as the authentication method and a previously registered authorization for this application. For more information, access the documentation on  and .

    
### Obtain an OAuth v2.0 authorization token
    
To obtain an  authorization token, follow the steps below.
    
:::(Info) (Info)
The process may vary depending on the scenario.
:::

1. On the senhasegura platform, click the , identified by the nine squares, and select .

1.  In the side menu, select .

1.  From the list, select the desired application and, in the  column, click the three vertical dots.

1. Click  to open a new window with the list of authorizations for the selected application.

1. Select the desired authorization, and in the  column, click , identified by the key icon. 

1. In the  window, click the  icons to view the  and the .

### Make a request using OAuth v2.0
    

1. In the HTTP or REST client of your choice, such as , create a collection.

1. In the , select .

1. In , select .

1. In the L, make a request to the appliance endpoint. E.g., 
`
https://applianceURI/iso/oauth2/token
`

5. In , enter the value obtained in step 6 of the  section of this tutorial. 

1. In , enter the value obtained in step 6 of the  section of this tutorial. 

1. Click , at the bottom of the page.

1. Click  to open the  page and view the .

1. Use this  to make the requests in senhasegura’s  APIs.
    
:::(Warning) (Caution)
By default, senhasegura creates a token with a 1-hour validity.
:::

###     Request a new access token
    
 If needed, request a new access token to  using the following URI:
`
POST /senhasegura/iso/oauth2/token
`
 and the following mandatory parameters:



    
    

| Field | Description |
| --- | --- |
|  | The value informed must always be . |
|  | Value informed by senhasegura and obtained following the steps in the   section of this tutorial. |
|  | Value informed by senhasegura and obtained following the steps in the  section of this tutorial. |
    

    
    
`
{
	grant_type: "client_credentials"
	client_id: "765299ec425cf0255badc739c2dce1b10634973e1"
	client_secret: "f13aeddeb57f262835871dab5d839b70"
}

`
    
 
    
`
{
    "token_type": "Bearer",
    "expires_in": 3600,
    "access_token": "
        eyJ0eXAiOiJKV1QiL0IjoxNTgwNDM2NTk4LCJuYmYiOjE1ODA0MzY1OTgsImV4cCI
     6MTU4MDQ0MDE5OCwic3ViIjoiTVRNeE1qQWtTRGRPUVRWV1ozcEVSI6Ijg0OWYw
        ZmVhNDI0ZDc5NWUwYTg2MjVlMTdiZWE2YTAyNTQyMzAxNjQzYmRmYTc5ZjYzZDN
        hM2U3ZmI5ZjQzbGCJhjg0OWYwZmVhNDI0ZDc5NWUwYTg2MjVlMTdiZWE2YTAyNT
        QyMzAxNjQzYmRmYTc5ZjYzZDNhM2U3ZmI5ZjQzYmM2MjRhYzg5YmVhMzFhOGQwI
        iwiaWFciOiJSUzI1NiIsImp0ahYzg5YmVhMzFhOGQwIn0.eyJhdWQiOiIzY2E4Y
        Tk4ZDkwNzU0MzgxMjMzNGY3ZjVkYmFmY2E2NTA1ZTMzMTlmYiIsImp0aSI6IYmM
        2MjRTRzB6ZFZONlZXVXhhVWN2Y1RKdFRXNTVhM05sZGtOd1JHeHllbXR5VEV3eE
        5EMD0iLCJzY29wZXMiOltdfQ.efqHZdlij6sQcj_l9RbNNKxDbf81CbIoTFwdIk
        ooT5bK14N5iUazrT8jpB_JsgQdQ8RyD5xF_ReKSj4Al7hp1uRXIiuErlKv1FpxY
        9oNC44kldlumjyevu87GJ0qzem0RYNc3930UbT-XEYqnQijg0se8_GdzdLkxyMn
        0kxApkAkv-to9EUdbbrvvno_pmqiZGyamw6J2BL1aCqwne3S8CCG34TXRyJyqkG
        rPrDO-NPi2fj25PRbX8Ci1iIqXdYvEkefg-g-i0A_Hp9E3s585c5wqxreSBAIwi
        aGtnTkxw0D14JPzqWf48hbvVRPGMj_-KXJTnu-zXkkEPNYs8oWpA"
}

`
    
Save the  to use in the next calls for every method.
    
    
## AWS authentication



 is an authentication method that enables applications to retrieve stored data using  and  together with a unique key generated by senhasegura . This method is used mainly for integration with  applications. For more information on  authentication, access the  document. 
