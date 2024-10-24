## Metadata_Start 
## code: en
## title: Hot to use DevOps Secret Manager CLI 
## slug: devops-secret-manager-cli 
## seoTitle: DevOps Secret Manager CLI 
## description:  
## contentType: Markdown 
## Metadata_End
The DSM CLI is a consolidated tool for managing the services offered by senhasegura. This utility allows the services to be used using command lines, allowing automation via scripts. The main purpose of this tool is to be an agnostic plugin capable of intercepting environment variables and inserting secrets into CI/CD systems and pipelines.

The agnostic nature of the DSM CLI means that it can be used in any CI/CD environment or tool. However, the DSM CLI already has some additional settings, simplifying integration with various tools.

This plug-in allows DevOps teams to centralize secret and application data effectively through DSM senhasegura, establishing a secure approach to consuming sensitive variables during the build and deployment phases.

Download the tool from our repository at .

## DSM CLI as Running Belt

:::(info) (Info)
If you don't have the  and  files, ask the senhasegura support team for them.
:::

So far, the senhasegura DSM CLI can only run as a Running Belt. In other words, the DSM CLI will read the secrets of the senhasegura DSM module and inject them as environment variables.

To implement the DSM CLI plugin, you must set up an application with OAuth 2.0 and authorization in senhasegura DSM.

After configuring the application, upload the executable to a directory in your environment or CI/CD tool. Also, ensure that a configuration file for authentication in senhasegura DSM is included. The DSM CLI needs information about the configured application, such as its name, system, and environment, to retrieve the secrets.

The configuration file must be in  format and contain the following details about senhasegura DSM:

* : URL of your senhasegura where DSM is enabled.
* : Client ID for authentication authorization.
* : client secret for authentication authorization.

Example of a  file:

`
SENHASEGURA_URL: ""
SENHASEGURA_CLIENT_ID: ""
SENHASEGURA_CLIENT_SECRET: ""
SENHASEGURA_MAPPING_FILE: ""
SENHASEGURA_SECRETS_FILE: ""
SENHASEGURA_DISABLE_RUNB: 0
`

:::(info) (Info)
Instead of a configuration file, the DSM CLI can obtain authentication information via environment variables, making the file optional.
:::

To use the binary, you can run the following command line providing the necessary information:

`bash
dsm runb \
    --application  \
    --system  \
    --environment  \
    --config 
`

After executing the binary with the essential information, all the environment variables available during the execution of the pipeline are collected and forwarded to the senhasegura DSM.

Subsequently, all the secrets recorded by the application are consulted and integrated into a file called .runb.vars. This file can be sent to the system to update the environment variables with the new values using the following command: 

This allows developers to not worry about injecting secrets during pipelines, since they can be managed directly through the API or the DSM interface, which is accessible to any member of the development or security team.

:::(warning) (Important)
Ensure that you have deleted the environment variables file to avoid data leakage.
:::

:::(info) (Info)
By default, the DSM CLI can discover secrets and inject them into tools such as GitHub, Azure DevOps, Bamboo, BitBucket, CircleCI, TeamCity, and Linux (default option). You can change the default option with the  argument during execution.
:::

## DSM CLI to record secrets

The DSM CLI also allows creating or updating secret values directly from the pipeline. To do this, use a mapping file called senhasegura-mapping.json. This file simplifies the identification of sensitive variables by their names, automatically registering them as secrets in the DSM.

The only additional configuration required consists of providing the mapping file, the executable, and the configuration file. Below is an example of the contents of the mapping file:

`json
{
  "access_keys": [
    {
      "name": "AWS_VARIABLES",
      "type": "aws",
      "fields": {
        "access_key_id": "AWS_ACCESS_KEY_ID_VARIABLE",
        "secret_access_key": "AWS_SECRET_ACCESS_KEY_VARIABLE"
      }
    }
  ],
  "credentials": [
    {
      "name": "CREDENCIAL_VARIABLES",
      "fields": {
        "user": "USER_VARIABLE",
        "password": "PASSWORD_VARIABLE",
        "host": "HOST_VARIABLE"
      }
    }
  ],
  "key_value": [
    {
      "name": "SECRET_VARIABLES",
      "fields": ["KEY_VALUE_VARIABLE"]
    }
  ]
}

`

This file can be divided into three main blocks:

1. : an array of objects comprising the attributes name, type, and subobject called fields. The last one is composed of the  and  attributes. The values of these attributes must be the names of the variables that contain the values, allowing senhasegura DSM to validate the existence of this data in the Cloud IAM module. If the data exists, it will be recorded as a secret for the authorization provided. It will be recorded as a key/value if it doesn't.
2. : an array of objects comprising the name attribute and a sub-object called fields. The last one includes the , , and  attributes. The values of these attributes must be the names of the variables containing this information, allowing senhasegura DSM to validate the existence of this data in the PAM module. If the data exists, it will be recorded as a secret for the authorization provided. It will be recorded as a key/value if it doesn't.
3. : is an array of objects composed of the name attribute and a fields subobject. The values of the array must be the names of the variables to be registered as secrets of the key/value type in senhasegura DSM.

:::(warning) (Important)

* This file must be named  and be at the same directory level as the executable.
* Currently, the senhasegura DSM only supports access keys via integration with AWS, Azure, or GCP, which means that the type attribute provided must be one of the supported ones.
  :::

---

Do you still have questions? Reach out to the .