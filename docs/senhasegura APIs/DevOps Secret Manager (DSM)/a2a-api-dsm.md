## Metadata_Start 
## code: en
## title: DevOps Secret Manager 
## slug: a2a-api-dsm 
## seoTitle: a2a DSM 
## description:  
## contentType: Markdown 
## Metadata_End
The senhasegura DevOps Secret Management (DSM) offers a rapid and secure way for tools and applications to request confidential information such as secrets, credentials and other sensitive data that are used on DevOps lifecycle.

The purpose of this section is to provide guidance for DevOps teams that need integration with senhasegura to manage all secrets used on their pipeline.

In this section, the following DevOps functions will be covered:

-   Request a secret to be used on an application
-   Provision a new credential to be used on an applications
-   Deprovision a credential

For information about DSM's API for automations, access the  document.


### Method

The senhasegura web integration service has a method for query secrets stored in the application.

### Query secret

` 
GET https://vault_url/iso/dapp/application 
` 
The application method queries all secrets linked to an application authorization.

#### Response

|  |  Type |  Description |
| --- | --- | --- |
|  |  String |  Application name |
|  |  String |  Application description |
|  |  String |  Tags that identify the application |
|  |  String |  Secret system |
|  |  String |  Secret environment |
|  |  Integer |  Secret ID |
|  |  String |  Secret Name |
|  |  String |  Secret identifier |
|  |  String |  Secret version |
|  |  Date/Time |  Secret expiration date |
|  |  String |  Secret engine |
|  |  String |  Secret values |

`json
{
    "response": {
        "status": 200,
        "mensagem": "Application 5",
        "erro": false,
        "message": "Application 5",
        "error": false
    },
    "application": {
        "name": "postman",
        "description": null,
        "tags": [
            ""
        ],
        "system": "back",
        "environment": "test",
        "secrets": [
            {
                "secret_id": "106",
                "secret_name": "application5",
                "identity": "application5",
                "version": "",
                "expiration_date": "",
                "engine": "Kubernetes",
                "data": [
                    {
                        "hostname": "application5_v_test",
                        "username": "ADMIN_V_USR",
                        "password": "ADMIN_V_PW",
                        "additional_information": "ADMIN_V_SCHEMA",
                        "ip": "app.application.com"
                    },
                    {
                        "access_key_id": "LKU5YC6QWAT487S4KEK",
                        "secret_access_key": "sack10821du07f9sacfsdaasdf",
                        "TTL": null
                    },
                    {
                        "my_key_name": "my_key_value",
                        "my_key_name_2": "my_key_value_2"
                    }
                ]
            }
        ]
    }
}
`

#### Response with SSH as secret

`json
{
    "response": {
        "status": 201,
        "mensagem": "Secret created successfully.",
        "erro": false,
        "cod_erro": 0,
        "message": "Secret created successfully.",
        "error": false,
        "error_code": 0
    },
    "application": {
        "name": "postman",
        "description": "teste",
        "tags": [
            "abc",
            "def",
            "teste"
        ],
        "system": "inetconfig",
        "environment": "stage",
        "secrets": [
            {
                "secret_id": "3",
                "secret_name": "state_secret",
                "identity": "cart/americanas/npf/cassandra",
                "version": "205",
                "description": "Chamada de API",
                "expiration_date": "2022-08-18 11:10:00",
                "engine": "GitLab",
                "data": [
                    {
                        "HOSTNAME": "AWS Gateway",
                        "USERNAME": "user",
                        "CONNECTION_STRING": "mongodb://api-server/auth",
                        "private_key": "An error occurred while encrypting the text",
                        "public_key": "ssh-rsa dsafffasdfads+FoCrHU0ZZSeIK4rkoB+O55qz0Ns527ROxwslDwn0TsLMwGTr3L4QCmnihmBOF7PlX7027DtldO0gFswdwPDKynAK2Crn6bcBQg8PAw6tUAM7/QWFosW13JzrbDz6gUV+DXMilQPUIJ7CsdfmubE/jFzJ/aBN2f+5mK6Xf3ghvGLo4+PriAUZO/x1XEm4+destdfsadfasafsd+GwwgFYVvTMOUYjjHYcqKjjqah8F8ltN5aN+9P3cwWlbnO/RoORHgpavBcOMDBXOHHtWwT4qSWNZJ4/BIeBr3ACTjqoUrDdAsgr2u+i46l user\n",
                        "PASSWORD": "sbgiXZU+5qmejm/kYqb+asdffsdaafsd/PPjcBxvr9S0jS1+F7Qc2HZ0N0PqQFw4I0p2X943+Y4wYR8RXSgFqtxuEbYBMv7TJijqIA0fVWkVNdCaqRVIpIbdtGjpUuf+asdffdsa/maPt0T9KfkKJSPh9WY2O8oRkCpRays8Lihp3ZP+asdffsd==",
                        "ip": "aws.amazon.com"
                    }
                ]
            }
        ]
    }
}
` 

### Create or update a secret

`
POST https://vault_url/iso/sctm/secret
`

#### Parameters
|  | Type | Description |
| --- | --- | --- |
|  | String | Secret Name |
|  | String | Secret's Identity |
|  | Date/time | Secret's deactivation date |
|  | String | Secret Description |
|  | String | Secret's Engine must be a valid engine registered in senhasegura |
|  | Int | Sets the time to renew cloud access keys in minutes. If omitted is ignored, but with empty array, will disable auto-renew |
|  | Int | Set the time to renew credentials in minutes. If omitted is ignored, but with empty array, will disable auto-renew |
|  | Int | Sets the time to renew ephemeral credentials in minutes. If omitted is ignored, but with empty array, will disable auto-renewal |
|  | String | Must be valid base64 encoded json as in Data Example|

#### Data Example

`json
{
    access_keys:
    [
        {
            access_key:
            {
                type: "aws",
                fields:
                {
                    access_key_id: "AKIAREVEFYNPPAOT3PF6",
                    access_key_id_label: "AWS_ACCESS_KEY_ID",
                    secret_access_key: "AStrongPass",
                    secret_access_key_label: "AWS_SECRET_ACCESS_KEY",
                }
            }
        },
    ],
    credentials:
    [
        {
            credential:
            {
                fields:
                {
                    user: "cred_a",
                    user_label: "USERNAME",
                    host: "aws.amazon.com",
                    host_label: "HOSTNAME",
                    password: "StrongPass",
                    password_label: "PASSWORD",
                    additional_information: "mongodb://api-server/auth",
                    additional_information_label: "CONNECTION_STRING",
                }
            }
        },
        {
            credential:
            {
                fields:
                {
                    user: "an_username",
                    user_label: "USERNAME",
                    host: "an_ip",
                    host_label: "HOSTNAME",
                    password: "StrongPass",
                    password_label: "PASSWORD",
                    additional_information: "the_additional_info",
                }
            }
        },
    ]
}
`

#### Response

|  |  Type |  Description |
| --- | --- | --- |
|  |  String | Application Name |
|  |  String | Application Description |
|  |  String | Application tag |
|  |  String | Secret System |
|  |  String |  Secret Environment |
|  |  Integer |  Secret ID |
|  |  String |  Secret Name |
|  |  String |  Secret Identifier |
|  |  String |  Secret version |
|  |  Date/Time | Secret Expiration Date |
|  |  String |  Secret Engine |
|  |  String |  Secret Values |

`json
{
    "response": {
        "status": 201,
        "mensagem": "Secret created successfully.",
        "erro": false,
        "cod_erro": 0,
        "message": "Secret created successfully.",
        "error": false,
        "error_code": 0
    },
    "application": {
        "name": "postman",
        "description": "teste",
        "tags": [
            "abc",
            "def",
            "teste"
        ],
        "system": "inetconfig",
        "environment": "stage",
        "secrets": [
            {
                "secret_id": "7",
                "secret_name": "state_secret",
                "identity": "example_2",
                "version": "2",
                "description": "Chamada de API",
                "expiration_date": "2022-08-18 11:10:00",
                "engine": "GitLab",
                "data": [
                    {
                        "AWS_ACCESS_KEY_ID": "AKIAREVEFYNPPAOT3PF6",
                        "AWS_SECRET_ACCESS_KEY": "fd/ZmmciA4d8CqkXIzK8l2oWrUY7+fds/aasdf+WwP5cTAQW5mpr9XAHiGS1zkRQEUvJ7pta3ABrAeRt3QH6UuuGwPunATFdhFvAG/lTlrby6z+dfdfas/cKUzQpHpQE0UNxNwzCauRpbPDOUzMnpRopbyGQDzdkN0uXSXJLh3kraX+/qQ/v3riN1pB+Wuzd4zvxLfeH6oA==",
                        "TTL": ""
                    },
                    {
                        "APP": "Postman",
                        "CONNECTION_STRING": "mongodb://api-server/auth",
                        "DATE": "date",
                        "HOSTNAME": "an_ip",
                        "PASSWORD": "StrongPass",
                        "USERNAME": "an_username"
                    }
                ]
            }
        ]
    }
}
`

### Create or update an application

` 
POST https://vault_url/iso/dapp/application 
`

#### Parameters

|  | Type | Description |
| --- | --- | --- |
| | String | Secret Name |
|  | String | Secret Identity |
|  | Date/Time | Secret's deactivation date |
|  | String | Secret Description |
|  | String | Secret's Engine must be a valid engine registered in senhasegura |
|  | Int | Set renewal time to cloud access keys in minutes. If omitted will disable  auto-renewal |
|  | Int | Set renewal time to credentials in minutes. If omitted will disable auto-renewal | 
|  | Int | Set renewal time to ephemeral credentials in minutes. If omitted will disable auto-renewal |
|  | String | Must be valid base64 encoded json |

#### Response

|  |  Type |  Description |
| --- | --- | --- |
|  | String | Unique identifier of an authorization, if the value is sent, the environment and system fields will be ignored for the authorization search |
|  | String | Application Name |
|  | String | System to which the authorization belongs, used for consultation, only used for writing in new authorizations |
|  | String | Environment to which the authorization belongs, used for consultation, only used for writing in new authorizations |
|  | String | Application description |
|  | String |  Application authentication and authorization method, this parameter is only used when creating the application, when updating it is ignored |
|  | String | Defines the application's line of business |
|  | String | Defines the application type |
|  | String | Define applications tags |
|  |  String | Define application ARNs |
|  | String |  Defines application cloud dynamic provisioning profiles |
|  |  Array | Defines application ephemeral credential dynamic provisioning profiles |
|  | String | Defines the authorized resources of the authorization, used only when creating the authorization |
|  | Date/Time |  Secret expiration date, used only when creating the authorization |
|  |  Boolean | Defines encryption of sensitive authorization data, used only in authorization creation |
|  | String | Defines the allowed IPs of the authorization, used only when creating the authorization |
|  | String | Defines the allowed HTTP referrers of the authorization, used only when creating the authorization |
|  | String | Defines the fingerprint of the authorization certificate, used only when creating the authorization |

#### Response 

|  | Type | Description |
| --- | --- | --- |
|  | String | Application ID | 
|  | String | Application Signature |

`json
{
    "response": {
        "status": 200,
        "mensagem": "Application updated: (4) postman | Authorization found: (6)",
        "erro": false,
        "cod_erro": 0,
        "message": "Application updated: (4) postman | Authorization found: (6)",
        "error": false,
        "error_code": 0
    },
    "id": "applicationID",
    "signature": "signature"
}
`

### Providing a credential
 
` 
POST https://vault_url/iso/coe/dapp/provision 
` 
Create a new credential secret to be used on a container.

#### Parameters

|  |  Type |  Description |  Required |
| --- | --- | --- | --- |
|  |  String |  Name of the pod that will use the credential |  Yes |
|  |  String |  Name of the deploy that will use the credential |  Yes |
|  |  String |  Namespace of the container that will use the credential |  Yes |

#### Response

|  |  Type |  Description |
| --- | --- | --- |
|  |  String | Application name |
|  |  String | Application description |
|  |  String |  Tags that identify the application |
|  |  String | Sistema da secret |
|  |  String | Ambiente de secret |
|  |  Integer | ID da secret |
|  |  String | Nome da secret |
|  |  String | Identificador da secret |
|  |  String | Versão da secret |
|  | Date/Time | Data de expiração da secret |
|  |  String | Engine da secret |
|  |  String | Valor da secret |

`json
{
    "response": {
        "status": 200,
        "mensagem": "Application 6",
        "erro": false
    },
    "application": {
        "name": "runb",
        "description": null,
        "tags": [
            ""
        ],
        "system": "senhasegura",
        "environment": "lab",
        "secrets": [
            {
                "secret_id": "3",
                "secret_name": "secure-demo",
                "identity": "secure-demo",
                "version": "",
                "expiration_date": "",
                "engine": "Kubernetes",
                "data": {
                    "APP_VAR1": "fX6v8vh7TADY",
                    "APP_VAR2": "vlln0XkBNWIk",
                    "APP_VAR3": "7qWgm1EBFnQb",
                    "APP_DB_PASSWORD": "4i8Vm0khqTWs",
                    "APP_SECRET": "GSePWjXyd91K"
                }
            }
        ]
    }
}
`

### Removing a credential
 
` 
POST https://vault_url/iso/coe/dapp/deprovision 
` 
Remove a credential secret to be used on a container.

#### Parameters

|  |  Type |  Description |  Required |
| --- | --- | --- | --- |
|  |  String |  Name of the pod that will use the credential |  Yes |
|  |  String |  Name of the deploy that will use the credential |  Yes |
|  |  String |  Namespace of the container that will use the credential |  Yes |
|  |  Integer |  Secret ID |  Yes |
