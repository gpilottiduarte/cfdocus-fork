## Metadata_Start 
## code: en
## title: About senhasegura's ITSM integration 
## slug: about-senhaseguras-itsm-integration 
## seoTitle: About senhasegura's ITSM integration 
## description:  
## contentType: Markdown 
## Metadata_End
The ITSM (IT Service Management) integration in senhasegura is a powerful feature that allows for a direct connection between privileged access management and IT service management systems.

## What is the Governance Code? 

The  is a central element in ITSM integration. It’s a unique identifier that:

* Can be inserted by users in the justification and authorization form.  
* Serves as a link between the request in senhasegura and a corresponding ticket in the ITSM system.

## How does the integration work?

Below, you can visualize a summary of the workflow for a ITSM integration process on senhasegura.

### Main components

* : initiates the request process.  
* : interface for entering the ITSM code.  
* : verifies credentials and the ITSM code.  
* : the final system to which access is requested.

### Request and Verification Process

1. The administrator user initiates the process through a request form.  
2. The administrator enters the ITSM code in the form.

### Security Verification

1. The ITSM code is sent to the senhasegura system.  
2. senhasegura requests additional credentials for authentication.

### Authentication in the ITSM Solution

1. senhasegura communicates with the ITSM Solution.  
2. senhasegura verifies if the provided ITSM code exists and is valid in the ITSM Solution.

### Confirmation and Authorization

1. If the code is valid, senhasegura receives a confirmation.  
2. The system then authorizes the user to proceed.

### Access Granted

After a successful verification, the user is granted access to the ITSM Solution.

### Security Aspects

* : the process involves both the ITSM code and additional credentials.  
* : senhasegura acts as a central point for verification and access control.  
* : the request form, security system, and ITSM solution are distinct components, increasing security.

### Benefits of ITSM Integration

* : ensures that privileged accesses are always associated with approved service tickets.  
* : facilitates tracking privileged accesses to corresponding service tickets.  
* : helps maintain compliance with security policies and regulations.  
* : automates the authorization verification process, reducing manual errors.

## How to make the Governance Code mandatory 

To ensure that all privileged access requests are linked to an ITSM ticket, you can make the Governance Code mandatory:

1. Go to:   
2. Create a new group or edit an existing one.  
3. In the  tab, in the  section, select  in the  field.

## Conclusion 

The ITSM integration in senhasegura offers an additional layer of security and control over privileged access. By linking access requests to valid ITSM tickets, organizations can ensure that all privileged accesses are properly authorized, documented, and auditable. This not only improves security but also helps maintain compliance with various regulations and security policies.