## Metadata_Start 
## code: en
## title: OpenID providers 
## slug: openid-providers 
## seoTitle: OpenID providers 
## description:  
## contentType: Markdown 
## Metadata_End
On this document, you'll find the information about the OpenID providers on senhasegura.

## Path to access

1. On senhasegura, in the upper left corner, click the , represented by the nine squares, and select .  
2. In the side menu, select .

## Top bar

| Item  | Description |
| :---- | :---- |
|  | Represented by the magnifying glass icon, it displays or hides the search fields on the screen. |
|  | Represented by the counterclockwise arrow icon, it refreshes the page. |
|  | Represented by the three vertical dots icon, it shows all the possible actions for the report. |
|  | Opens the  window to register a new OpenID provider |
|  | Represented by the printer icon, it opens a new page for printing the report. |
|  | Represented by the paper sheet icon, it downloads the report. |
|  | Represented by the clock icon, it opens the  form. |

## Search fields

| Item | Descrição |
| :---- | :---- |
|  | Registration code of the OpenID provider in senhasegura. |
|  | Drop-down menu to select the type of OpenID provider. |
|  | Text field for entering the value of the client ID. |
|  | Text field for entering the value of the OpenID provider's redirect URL. |
|  | Drop-down menu to choose the status of the provider. It can be  or . |
|  | Drop-down menu to choose the environment in which the provider will be used. |

## Report fields

*   
*   
*   
*   
*   
*   
* In the  column, you have two options:  
  *  represented by the pencil and paper icon, opens the  window in edit mode.  
  *  by clicking on the three vertical dots icon, you have two options:  
    *  represented by the magnifying glass icon, opens the provider details window.  
    *  represented by the trash can icon, deletes the provider.

## Provider registration window

By clicking on  in the  column or , you can access the  window. It contains the following fields:

| Item | Description |
| :---- | :---- |
|  | Type of OpenID provider. |
|  | Radio button for selecting the provider's state. It can be  or . |
|  | Radio button for selecting the provider's environment. It can be  or . |
|  | Client ID of the client in the OpenID provider. |
|  | Secret of the client application in the OpenID provider. |
|  | Domain or public IP address of senhasegura. Used by the OpenID provider to redirect the user back to the app. |
|  | The specific endpoint in the client application to which the OpenID provider will redirect the user after auth. |
|  | Comments field, such as notes, explanations, and others. |

### Endpoint settings section

| Item | Description |
| :---- | :---- |
|  | OpenID configuration endpoint. If Google OpenID is chosen, the field will be filled in automatically with Google's information. |

### URL for other endpoints section

| Item | Description |
| :---- | :---- |
|  | URL provided by the OpenID provider where the application sends the authorization request. |
|  | URL provided by the OpenID provider where the application requests to exchange the authorization code for an access token. |
|  | URL provided by the OpenID provider where the application can request information from the authenticated user's profile using the access token. |

### Extra settings for provider section

| Item | Descrição |
| :---- | :---- |
|  | Endpoint where the application can obtain the public keys from the OpenID provider to validate the signature of the access token. It's mandatory if these keys aren't available on the OpenID configuration endpoint. |
|  | List of additional issuers that are accepted by the application. Useful when the application needs to support multiple OpenID providers. Issuers are separated by a comma. |
