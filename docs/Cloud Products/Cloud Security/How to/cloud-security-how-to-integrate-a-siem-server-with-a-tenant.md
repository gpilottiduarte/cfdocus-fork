## Metadata_Start 
## code: en
## title: How to integrate a SIEM server with a tenant 
## slug: cloud-security-how-to-integrate-a-siem-server-with-a-tenant 
## seoTitle: How to integrate a SIEM server with a tenant 
## description: This tutorial presents a step-by-step process on how to add SIEM integrations to a tenant in Cloud Security. 
## contentType: Markdown 
## Metadata_End
This tutorial presents a step-by-step process on how to add SIEM integrations to a tenant in .

### Requirements

- Have the role .
- Have one or more SIEM sockets configured in a third-party service.

## Add a SIEM server integration

1. On , click the  icon on the top right corner of the screen.
2. In the dropdown menu, select .
3. Under , select .
4. Click .
5. Fill in the fields as follows:
    1. : type a name for the SIEM integration being created.
    2. : in the select field, choose between:
        1. : add the full hostname of the SIEM socket.
        2. : add the IP address of the SIEM socket.
    3. : add the listener port that should receive the logs.
    4. : in the select field, choose between  or .
    5. : in the select field, choose between  or .
    6. : in the select field, select  to enable the TLS handshake for communication with the SIEM socket or choose  if Cloud Security should not initiate a TLS handshake.
6. Click .