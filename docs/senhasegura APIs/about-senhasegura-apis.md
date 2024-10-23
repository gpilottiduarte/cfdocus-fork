## Metadata_Start 
## code: en
## title: About senhasegura APIs 
## slug: about-senhasegura-apis 
## seoTitle: About senhasegura APIs 
## description:  
## contentType: Markdown 
## Metadata_End
The  were developed to provide an interface that allows other applications and tools to integrate with senhasegura, enabling secure access to vault functionalities and information. These APIs ensure programmatic access and management of data stored in senhasegura, maintaining the integrity, confidentiality, and auditability of information.

Operating under REST architecture, the senhasegura APIs:
- Are based on HTTP.
- Enable stateless communication between client and server.
- Use  GET,  POST,  PUT,  DEL methods to make requests.
- Support authentication via , , and .
- Accept URL *form-encoded* requests.
- Return JSON responses.
- Offer integration capabilities with third-party applications for actions such as querying, creating, updating, activating, and deactivating sensitive information, including credentials, devices, access keys, remote sessions, related users, digital certificates, dashboards, DevOps secrets, and corporate personal and team sensitive information.

## Features

The  include:
- :  senhasegura web service operates under a REST architecture, ensuring standardized and efficient communication.
- : the API supports AWS, OAuth v1.0, and OAuth v2.0, ensuring robust authentication and secure access to privileged data.
- : each API request generates detailed logs with essential information such as the date, time, IP address of the origin device, and the client application involved. In order to maintain data security, sensitive information such as passwords and keys remain hidden.
- : in addition to OAuth authentication, access control also considers the IP address of the origin device, further enhancing security.
- : client applications can access only the credentials they created or those specifically assigned to them in the senhasegura settings.
- : the API allows the management of various types of credentials, such as passwords used to access devices, servers, or routers, and RSA keys for SSH connections. Passwords and RSA keys are subject to automatic rotation according to each environment's security policy.
- : the API allows the editing of various entities, including credentials, devices and personal information, ensuring comprehensive management of privileged data.

## Applicabilites and use cases

 can be applied in various scenarios, such as:

### Credential management 
With the  API, organizations can efficiently register and manage credentials, ensuring secure access to devices and critical resources registered in PAM Core. This is particularly valuable when integrated with third-party applications, such as inventory management tools or automation platforms.



A FINTECH needs to ensure that the use of its credentials is secure and audited. Using the senhasegura API, it can integrate its vulnerability scanning system with the  security platform. With this integration, the tool can consume the credentials already registered in senhasegura to perform its procedures, ensuring that only authorized employees have secure and controlled access to critical resources.


-  



### Device management

 The  API facilitates the administration and maintenance of devices registered in , ensuring they remain accessible only to authorized users.



A HEALTHTECH needs to manage various network-connected devices already registered in its CMDB. Using the API, the company can automate these devices' registration and initial configuration, ensuring they are ready for immediate use and in compliance with security standards and industry regulations.

 
 - 



### Remote session management

The  API allows organizations to control and monitor the use of proxy sessions registered in  in an automated and centralized manner. This API facilitates the creation, monitoring, and termination of proxy sessions, offering resources for identity management, access control, and activity auditing.



A payment technology company that processes online financial transactions must ensure communications security between internal systems and business partners. The client has an internally developed system used by employees to perform necessary maintenance accesses. To monitor these accesses without changing how employees work, the company decided to use PAM, maintaining access through the custom application.

By using the senhasegura  API to create an authenticated URL for a web proxy session, the company can seamlessly integrate PAM into its platform. This allows users to be redirected to authenticated sessions, ensuring the security and integrity of financial transactions performed without employees needing to log in directly to senhasegura. Thus, the company can control and monitor the use of proxy sessions in an automated and centralized manner.


- 



### SSH key management
Through the  API, organizations can manage SSH keys registered in  in a simple and centralized way, allowing process automation, strengthening security, and ensuring compliance with access policies.



A banking company that implements SSH keys to access Unix/Linux servers can easily manage the keys through the API for registration, querying, or editing, thus ensuring audited and monitored access via senhasegura.


- 



### Related user management
The  API enables the management of associations between senhasegura users and multiple credential usernames, offering a flexible and customized solution for managing access to devices.



An IT consulting firm that provides services to multiple organizations needs to efficiently manage its consultants' access to clients' systems and resources. Using the API, the company can associate multiple credential usernames with a single senhasegura user, simplifying access management and ensuring compliance with clients' security policies.


- 



### Certificate management

The  API is designed for organizations of all sizes. It aims to centralize and simplify the certificate management process, including secure certificate import, continuous monitoring, automation of the certificate lifecycle, integration with Certificate Authorities, and publication on web servers.


 
An e-commerce company operating an online shopping platform must ensure the security of customers' financial transactions. The company can automate the SSL/TLS certificate renewal and monitoring process using the API, avoiding service downtime and ensuring secure and encrypted connections between customers and the web server.


- 



### Dashboard management

The  API allows the consumption of information compiled in the senhasegura Dashboards module. Through the API, it is possible to query the information in remote sessions, suspicious actions, and credential dashboards. The queried information can be used to create customized dashboards.



A cybersecurity company providing network monitoring and protection services needs to access and visualize information compiled in dashboards to analyze privileged user activities and identify potential security threats. Using the API, the company can query and analyze data from remote sessions, suspicious actions, and credentials, then create customized dashboards that provide valuable insights for proactively protecting their clients’ IT infrastructure.


- 



### Protected information management
This API allows systems integration with senhasegura's  product, facilitating the query of corporately shared information.



A data security consulting firm serving various organizations can use the API to store and update access passwords to client systems.

  

- 



### DevOps secret management

The  API provides an agile and secure solution for tools and applications to consume the secrets and credentials used during development and operation in DevOps pipelines in an efficient and controlled manner.



A software development company adopting agile and DevSecOps practices needs to efficiently manage the secrets and credentials used in the development and continuous delivery pipelines. Through the API,  can deliver access securely to automation tools, ensuring that only authorized applications have access to the secrets needed to perform their tasks securely and efficiently without exposing credentials in their code.

  
- 



### MySafe stored item management

The  APIs enable secure management of items such as passwords, notes, files, and corporate API secrets stored in the  vault, ensuring the integrity and confidentiality of information.

 

In a consulting firm, a meeting note-taking AI is integrated with the API, allowing automatic note submission to the vault, where they are securely stored and shared with the involved participants for consultation. The API also allows another system to keep access to passwords, API secrets, and notes updated in real-time through integration. This ensures that, for example, if an employee is moved to another area, their access is automatically adjusted.



- 


### SCIM APIs
senhasegura offers APIs in the SCIM (System for Cross-domain Identity Management) standard to provide a standardized way for user identity management and provisioning in the application. These APIs are crucial for the platform as they enable senhasegura integration with IGA (Identity Governance and Administration) systems, allowing automated and centralized management of users and their access within senhasegura.



A large bank needs to ensure centralized identity management. When a new employee is hired, their IGA application automatically communicates with the senhasegura platform via the SCIM API to provision the new user's account, assigning the necessary permissions and access efficiently and quickly. This ensures the new employee has immediate access to essential resources in senhasegura, eliminating the need for manual configurations and reducing the risk of errors.


- 



## Conclusion

With a wide range of functionalities,  cover everything from credential and device management to remote session monitoring and digital certificate management. These functionalities are applicable in various use cases, from financial organizations needing to secure online transactions to technology companies seeking to automate their development and operations processes.

 represent not only a crucial tool for enhancing information security but also an opportunity for organizations to increase operational efficiency and ensure compliance with security regulations and standards. By adopting and integrating senhasegura APIs into their systems and processes, companies can achieve higher levels of data protection and customer trust in an increasingly complex and interconnected digital world.

 ## First steps

To start using senhasegura APIs, access the documents below:
- .
- .


