# Execution template tags 

Tags are pre-defined variables that can be used in senhasegura templates instead of hard-coded information, allowing the use of the same template for operations on multiple devices.
PAM Core tags
Tag
Description
[#USERNAME#]
Username of the credential that will have its password changed
[#NEW_PASSWORD#]
The new password you want the credential to use
[#CURRENT_PASSWORD#]
The password in use for the credential
[#AUTH_USER#]
Username of the credential that will be authenticated on the station/system/server to perform the change
[#AUTH_PASSWORD#]
Password of the credential that will authenticate itself to execute the change
[#AUTH_DOMAIN#]
Domain of the credential that will authenticate itself to execute the change
[#ADD_INFO#]
Additional credential information
[#IP#]
The credential's device IP that will have the password changed
[#HOSTNAME#]
The credential's device hostname that will have the password changed
[#DOMAIN#]
The credential's device domain that will have the password changed
[#SERVER_PATH#]
The path of the credential server that will have the password changed
DevOps Secret Manager tags
Application and authorization tags
Tag
Description
[#APP_NAME#]
Application name
[#APP_AUTH_UNIQUE_KEY#]
Authorization unique key
[#APP_AUTH_TYPE#]
Authorization authentication type
[#APP_AUTH_CLIENT_ID#]
OAuth2 client ID
[#APP_AUTH_CLIENT_SECRET#]
OAuth2 client secret
[#APP_AUTH_CONSUMER_KEY#]
OAuth1 consumer key
[#APP_AUTH_CONSUMER_SECRET#]
OAuth1 consumer secret
[#APP_AUTH_TOKEN#]
OAuth1 Auth token
[#APP_AUTH_TOKEN_SECRET#]
OAuth1 token secret
Secrets tags
Tag
Description
[#SECRET_NAME#]
Secret name
[#SECRET_IDENTIFIER#]
Secret identifier
[#SECRET_VERSION#]
Secret version
[#SECRET_ENGINE#]
Secret engine name
[#SECRET_EXPIRATION_DATE#]
Secret expiration date
[#SECRET_DATA#]
All secret data
Secret data tags
Tag
Description
[#ACCESS_KEY_ID#]
Access key ID
[#SECRET_ACCESS_KEY#]
Secret access key
[#ACCESS_KEY_TTL#]
Access key TTL
[#CREDENTIAL_HOSTNAME#]
Credential hostname
[#CREDENTIAL_USERNAME#]
Credential username
[#CREDENTIAL_PASSWORD#]
Credential password
[#CREDENTIAL_ADDITIONAL_INFORMATION#]
Credential additional information
[#CREDENTIAL_TTL#]
Credential TTL