## Metadata_Start 
## code: en
## title: SCIM API 
## slug: scim-api 
## seoTitle: SCIM API 
## description:  
## contentType: Markdown 
## Metadata_End
This article presents how senhasegura's System for Cross-domain Identity Management (SCIM) endpoints share information using API calls.

:::(Info) (Info)
Any tool that supports the SCIM 2.0 protocol can be integrated with senhasegura.
:::

## GET Service Provider Configuration
#### Request

To retrieve the , send a request to the following endpoint:



#### Parameters
No parameters.

#### Return
Returns the configurations supported by our SCIM connector.

#### Sample response

`json
{
    "schemas":  ["urn:ietf:params:scim:schemas:core:2.0:ServiceProviderConfig"],
    "documentationUri": "http://example.com/help/scim.html",
    "patch": {
      "supported":true
    },
    "bulk": {
      "supported":true,
      "maxOperations":1000,
      "maxPayloadSize":1048576
    },
    "filter": {
      "supported":true,
      "maxResults": 200
    },
    "changePassword": {
      "supported":false
    },
    "sort": {
      "supported":true
    },
    "etag": {
      "supported":true
    },
    "authenticationSchemes": [
      {
        "name": "OAuth Bearer Token",
        "description":
          "Authentication scheme using the OAuth Bearer Token Standard",
        "specUri": "http://www.rfc-editor.org/info/rfc6750",
        "documentationUri": "http://example.com/help/oauth.html",
        "type": "oauthbearertoken",
        "primary": true
      },
      {
        "name": "HTTP Basic",
        "description":
          "Authentication scheme using the HTTP Basic Standard",
        "specUri": "http://www.rfc-editor.org/info/rfc2617",
        "documentationUri": "http://example.com/help/httpBasic.html",
        "type": "httpbasic"
       }
    ],
    "meta": {
      "location": "https://example.com/v2/ServiceProviderConfig",
      "resourceType": "ServiceProviderConfig",
      "created": "2010-01-23T04:56:22Z",
      "lastModified": "2011-05-13T04:42:34Z",
      "version": "W\/\"3694e05e9dff594\""
    }
  }
`
:::(Info) (Info)
For more information, check the .
:::

* * *
## GET Resource Types

#### Request
To retrieve the , send a request to the following endpoint:


#### Parameters
No parameters.

#### Return
Returns the Resource Types supported by our SCIM connector.

#### Sample response
`json
{
  "schemas": [
    "urn:ietf:params:scim:api:messages:2.0:ListResponse"
  ],
  "totalResults": 1,
  "itemsPerPage": 1,
  "startIndex": 1,
  "Resources": [
    {
      "schemas": [
        "urn:ietf:params:scim:schemas:core:2.0:ResourceType"
      ],
      "id": "User",
      "name": "User",
      "endpoint": "/Users",
      "description": "https://tools.ietf.org/html/rfc7643#section-8.7.1",
      "schema": "urn:ietf:params:scim:schemas:core:2.0:User",
      "schemaExtensions": [
        {
          "schema": "urn:ietf:params:scim:schemas:extension:enterprise:2.0:User",
          "required": false
        }
      ],
      "meta": {
        "location": "https://vault.senhasegura.com/iso/scim/v2/ResourceTypes/User",
        "resourceType": "ResourceType"
      }
    }
  ]
}
`
:::(Info) (Info)
For more information, check the .
:::
***
## GET User Resource Type
#### Request
To retrieve the , add the object at the end of the URI and send a request to the following endpoint:


#### Parameters
No parameters.

#### Return
Returns the attributes associated with user objects.

#### Sample response
`json
{
  "schemas": [
    "urn:ietf:params:scim:schemas:core:2.0:ResourceType"
  ],
  "id": "User",
  "name": "User",
  "endpoint": "/Users",
  "description": "https://tools.ietf.org/html/rfc7643#section-8.7.1",
  "schema": "urn:ietf:params:scim:schemas:core:2.0:User",
  "schemaExtensions": [
    {
      "schema": "urn:ietf:params:scim:schemas:core:2.0:User",
      "required": false
    }
  ],
  "meta": {
    "location": "https://vault.senhasegura.com/iso/scim/v2/ResourceTypes/User",
    "resourceType": "ResourceType"
  }
}
`

* * *
## GET Schemas
#### Request
To retrieve the , send a request to the following endpoint:


#### Parameters
No parameters.

#### Return
Returns the Schemas supported by our SCIM connector.

#### Sample response
`json
{
  "schemas": [
    "urn:ietf:params:scim:api:messages:2.0:ListResponse"
  ],
  "totalResults": 3,
  "itemsPerPage": 3,
  "startIndex": 1,
  "Resources": [
    {
      "id": "urn:ietf:params:scim:schemas:core:2.0:User",
      "name": "User",
      "description": "User Schema",
      "attributes": [
        "..."
      ],
      "meta": {
        "resourceType": "Schema",
        "location": "https://vault.senhasegura.com/iso/scim/v2/Schemas/urn:ietf:params:scim:schemas:core:2.0:User"
      }
    }
  ]
}
`

* * *
## GET User Schema
#### Request
To retrieve the , add the specifications at the end of the URI and send a request to the following endpoint:


#### Parameters
No parameters.

#### Return
Returns information about the Schema associated with the user.

#### Sample response
`json
{
  "id": "urn:ietf:params:scim:schemas:core:2.0:User",
  "name": "User",
  "description": "User Schema",
  "attributes": [
    {
      "name": "userName",
      "type": "string",
      "multiValued": false,
      "required": true,
      "caseExact": false,
      "mutability": "readWrite",
      "returned": "default",
      "uniqueness": "server",
      "description": "Unique identifier for the User, typically used by the user to directly authenticate to the service provider. Each User MUST include a non-empty userName value. This identifier MUST be unique across the service provider's entire set of Users."
    },
    {
      "name": "name",
      "type": "complex",
      "multiValued": false,
      "required": false,
      "mutability": "readWrite",
      "returned": "default",
      "uniqueness": "none",
      "description": "The components of the user's real name. Providers MAY return just the full name as a single string in the formatted sub-attribute, or they MAY return just the individual component attributes using the other sub-attributes, or they MAY return both.  If both variants are returned, they SHOULD be describing the same name, with the formatted name indicating how the component attributes should be combined.",
      "subAttributes": [
        {
          "name": "formatted",
          "type": "string",
          "multiValued": false,
          "required": false,
          "caseExact": false,
          "mutability": "readWrite",
          "returned": "default",
          "uniqueness": "none",
          "description": "The full name, including all middle names, titles, and suffixes as appropriate, formatted for display (e.g., 'Ms. Barbara J Jensen, III')."
        },
        {
          "name": "familyName",
          "type": "string",
          "multiValued": false,
          "required": false,
          "caseExact": false,
          "mutability": "readWrite",
          "returned": "default",
          "uniqueness": "none",
          "description": "The family name of the User, or last name in most Western languages (e.g., 'Jensen' given the full name 'Ms. Barbara J Jensen, III')."
        }
.
.
.
}
  ],
  "meta": {
    "resourceType": "Schema",
    "location": "https://wdc.test.host/scim/v2/Schemas/urn:ietf:params:scim:schemas:core:2.0:User"
  }
}
`
:::(Info) (Info)
For more information, check the .
:::

* * *
## GET Users
#### Request
To retrieve the , send a request to the following endpoint:


#### Parameters
No parameters.

#### Return
Returns the list of users.

#### Sample response
`json
{
  "schemas": [
    "urn:ietf:params:scim:api:messages:2.0:ListResponse"
  ],
  "totalResults": 2,
  "itemsPerPage": 25,
  "startIndex": 1,
  "Resources": [
    {
      "schemas": [
        "urn:ietf:params:scim:schemas:core:2.0:User",
      "urn:ietf:params:scim:schemas:extension:enterprise:2.0:User"
      ],
      "id": "2",
      "externalId": "SCIM1",
      "userName": "Jane Doe",
      "meta": {
        "resourceType": "User",
        "created": "2018-04-17T09:03:39-05:00",
        "lastModified": "2018-04-17T09:03:39-05:00",
        "location": "https://vault.senhasegura.com/iso/scim/v2/Users/2"
      },
      "name": {
        "familyName": "Doe",
        "givenName": "Jane",
        "honorificPrefix": "Mrs",
        "honorificSuffix": "MD",
        "formatted": "Mrs Jane Doe MD"
      },
      "displayName": "Jane Doe",
      "nickName": "Nick Jane",
      "profileUrl": "http://skimmer.com/jane",
      "title": "First Class Skimmer",
      "...": "..."
    },
    {
      "schemas": [
        "urn:ietf:params:scim:schemas:core:2.0:User",
      "urn:ietf:params:scim:schemas:extension:enterprise:2.0:User"
      ],
      "id": "1",
      "externalId": "SCIM2",
      "userName": "Card Skimmer",
      "meta": {
        "resourceType": "User",
        "created": "2018-04-17T09:03:12-05:00",
        "lastModified": "2018-04-17T09:03:12-05:00",
        "location": "https://.4me.com/scim/v2/Users/1"
      },
      "name": {
        "familyName": "Skimmer",
        "givenName": "Card",
        "honorificPrefix": "Sir",
        "honorificSuffix": "MD",
        "formatted": "Sir Card Skimmer MD"
      },
      "displayName": "Card Skimmer",
      "nickName": "Nicked Name",
      "...": "..."
    }
  ]
}
`
***
## GET User by ID
#### Request
To retrieve a , send a request to the following endpoint:


#### Parameters

| Name | Type | Required | Description | Example |
| --- | --- | --- | --- | --- |
| id | Integer | Required | Specifies the user inside the system. |  |

#### Return
Returns information about a specific user.

#### Sample response
`json
{
  "schemas": [
    "urn:ietf:params:scim:schemas:core:2.0:User",
    "urn:ietf:params:scim:schemas:extension:enterprise:2.0:User"
  ],
  "id": "2",
  "externalId": "SCIM1",
  "userName": "Jane Doe",
  "meta": {
    "resourceType": "User",
    "created": "2018-04-17T09:03:39-05:00",
    "lastModified": "2018-04-17T09:03:39-05:00",
    "location": "https://vault.senhasegura.com/iso/scim/v2/Users/2"
  },
  "name": {
    "familyName": "Doe",
    "givenName": "Jane",
    "honorificPrefix": "Mrs",
    "honorificSuffix": "MD",
    "formatted": "Mrs Jane Doe MD"
  },
  "displayName": "Jane Doe",
  "nickName": "Nick Jane",
  "profileUrl": "http://skimmer.com/jane",
  "title": "First Class Skimmer",
  "userType": "Skimmer",
  "preferredLanguage": "Dutch",
  "locale": "nl",
  "timezone": "Amsterdam",
  "active": true,
  "emails": [
    {
      "type": "work",
      "value": "jane.doe@scim.com",
      "primary": true
    }
  ],
  "phoneNumbers": [
    {
      "type": "work",
      "value": "+31 65 7777777",
      "primary": true
    },
    {
      "type": "personal",
      "value": "+31 20 4444444"
    }
  ],
  "photos": [
    {
      "value": "photo1"
    }
  ],
  "entitlements": [
    {
      "value": "specialist"
    },
    {
      "value": "change_manager"
    },
    {
      "value": "service_manager"
    }
  ],
  "groups": [
    {
      "value": "Full access"
    },
    {
      "value": "With approval"
    }
  ]
}
`

* * *
## POST Users
#### Request
To create , send a request to the following endpoint:


#### Parameters
| Name | Type | Required | Description | Example |
| --- | --- | --- | --- | --- |
userName|String|Required|The unique login identifier for the user.|
externalId|String|Required|An external identifier for the user.|
name.formatted|String|Required|The full name of the user.|
name.familyName|String|Optional|The family name or last name of the user.|
name.givenName|String|Optional|The given name or first name of the user.|
phoneNumbers.value|String|Optional|The user's phone number.|
emails.value|String|Required|The user's email address.|
emails.type|String|Optional|The category of the email address.|
emails.primary|Boolean|Optional|Indicates whether the email address is the user's primary email.|
entitlements.value|String|Optional|The user's role in the system.|
groups.value|String|Optional|The user groups associated with the user.|

#### Return
Returns the created users and the associated information when successful.

#### Sample response
`json
HTTP/1.1 201 Created

{
  "schemas":["urn:ietf:params:scim:schemas:core:2.0:User"],
  "id":"2819c223-7f76-453a-919d-413861904646",
  "externalId":"dschrute",
  "meta":{
    "resourceType":"User",
    "created":"2011-08-01T21:32:44.882Z",
    "lastModified":"2011-08-01T21:32:44.882Z",
    "location": "https://example.com/v2/Users/2819c223-7f76-453a-919d-413861904646",
    "version":"W\/\"e180ee84f0671b1\""
  },
  "name":{
    "familyName":"Schrute",
    "givenName":"Dwight"
  },
  "userName":"dschrute"
}
`
:::(Warning) (Caution)
If the user's password is included in the request, the user must use that password. Otherwise, you should generate a random password, and the administrator must log in to senhasegura to modify it and share it with the user.
:::

* * *
## PATCH Users 
#### Request
To modify information about , send a request to the following endpoint:


#### Parameters
| Name | Type | Required | Description | Example |
| --- | --- | --- | --- | --- |
userName|String|Required|The unique login identifier for the user.|
externalId|String|Required|An external identifier for the user.|
name.formatted|String|Required|The full name of the user.|
name.familyName|String|Optional|The family name or last name of the user.|
name.givenName|String|Optional|The given name or first name of the user.|
phoneNumbers.value|String|Optional|The user's phone number.|
emails.value|String|Required|The user's email address.|
emails.type|String|Optional|The category of the email address.|
emails.primary|Boolean|Optional|Indicates whether the email address is the user's primary email.|
entitlements.value|String|Optional|The user's role in the system.|
groups.value|String|Optional|The user groups associated with the user.|

#### Return
Returns the updated information associated with the users.

#### Sample response
`json
HTTP/1.1 200 OK

{
  "schemas":["urn:ietf:params:scim:schemas:core:2.0:User"],
  "id":"2819c223-7f76-453a-919d-413861904646",
  "externalId":"dschrute",
  "meta":{
    "resourceType":"User",
    "created":"2011-08-01T21:32:44.882Z",
    "lastModified":"2011-08-01T21:32:44.882Z",
    "location": "https://example.com/v2/Users/2819c223-7f76-453a-919d-413861904646",
    "version":"W\/\"e180ee84f0671b1\""
  },
  "name":{
    "familyName":"Schrute",
    "givenName":"Dwight"
  },
  "userName":"dschrute"
}
`
*** 
## DELETE Users
#### Request
To remove , send a request to the following endpoint:


#### Parameters
No parameters.

#### Return
If the user deletion was successful, it will return the 'HTTP 204 No Content' response.

#### Sample response
`json
HTTP/1.1 204 No Content
`