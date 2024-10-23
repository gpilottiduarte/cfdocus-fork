## Metadata_Start 
## code: en
## title: How to manage OpenID providers 
## slug: how-to-manage-openid-providers 
## seoTitle: How to manage OpenID providers 
## description:  
## contentType: Markdown 
## Metadata_End
This document provides a step-by-step guide on how to add or remove OpenID providers in senhasegura.

## Path to access

1. On senhasegura, in the upper-left corner, click the , represented by the nine squares, and select .
2. In the side menu, select .

## Add provider

1. On the OpenID Providers report page, in the top bar, click , represented by the three vertical dots icon, and select .
2. In the  window, on the  tab, fill in the fields below:
    1. : from the drop-down menu, select the type of OpenID provider to be used.
    :::(info) (Info)
    Please note that each provider will require specific information, so check the provider's settings whenever further information is required.
    :::
    3. : select the status of the OpenID provider at the time of creation. By default, it is always selected as .
    4. : select the environment that the OpenID provider will be in.
    5. : client ID for connection. This ID is provided by the OpenID provider when registering a new application.
    6. : select the secret of the OpenID authentication provider. This secret is provided by the OpenID provider when registering a new application.
    7. : insert the senhasegura's domain or public IP address. It is used by the OpenID provider to redirect the user back to their application after authentication.
    8. : specific endpoint in your application to which the OpenID provider will redirect the user after authentication.
    9. : enter adding additional notes or observations about the configuration.
3. In the  section, fill in the fields below:
    1. : insert the endpoint that configures OpenID. It is the base URL provided by the OpenID provider. This URL describes the endpoints required for OpenID interactions. This configuration automates the discovery of endpoints in general.
    :::(info) (Info)
    This field is only required if the URL fields for the endpoints aren't filled in. The user must fill in at least one of the two available fields:  or . If the URL of the other endpoints field isn't filled in, the user must fill in the  field to ensure that the services are configured correctly.

4. In the  section, fill in the fields below:
    1. : insert the URL provided by the OpenID provider, used by the application to send authorization requests.
    2. : insert the URL made available by the OpenID provider, where the application sends requests to exchange the authorization code for an access token.
    3. : URL made available by the OpenID provider, through which the application can request information on the authenticated user's profile, using the access token.
5. In the  section, fill in the fields below:
    1. : endpoint where the application can obtain the OpenID provider's public keys to validate the access token signature. This field is mandatory if these keys aren’t available on the .
    2. : a list of additional issuers that the application accepts. This is useful when the application needs to support multiple OpenID providers.
6. Click .

## Update a provider
To update the information of a previously registered provider, follow the steps below:

1. On the  report page, locate the provider you want to update.
2. In the  column, click , represented by the pencil and paper icon.
3. The  window will open in edit mode.

:::(info) (Info)
If the client's secret isn’t changed, the current information will be kept.
:::

4. Update the necessary information and click .

## Show a provider’s details
To view the provider's details, follow the steps below:

1. In the  column, click the three vertical dots icon and select , represented by the magnifying glass icon.
2. The  window will open in preview mode.
3. In this window, you can view various details of the registered provider, such as the *OpenID endpoint configuration, Authorization endpoint, Userinfo endpoint, Redirect URL, Token endpoint*, and *Comments*.
4. To view one piece of information at a time, click the eye icon next to the text field for each detail.
5. To exit, close the window.

## Delete a provider

1. In the  column, click the three vertical dots icon and select , represented by the trash can icon.
2. In the confirmation modal, click .
3. The  message will confirm the operation.

***

Do you still have questions? Reach out to the 
