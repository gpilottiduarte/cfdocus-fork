## Metadata_Start 
## code: en
## title: Upgrade Notes 
## slug: upgrade-notes 
## seoTitle: Upgrade Notes 
## description:  
## contentType: Markdown 
## Metadata_End
:::(Warning) (Attention)
Starting from August 19, 2024, all updates will utilize the new senhasegura repository. The old repository will no longer be available after this date.

If you are using a very old version of senhasegura, you will need to update incrementally, passing through each intermediate version until you reach the latest version, as described in our documentation.
:::
:::(Warning) (Attention)
Proxy 2.0 is in Beta. We do not recommend using Beta versions in production environments.
:::
:::(Warning) (Caution)

Before executing the senhasegura update,  and perform the 

:::

:::(Warning) (Caution)

If you use the , remove it from the cluster before updating senhasegura. .

:::

:::(Warning) (Caution)

Zabbix users must reconfigure the application if it presents any problem after updating. Find instructions in the article .

:::

We are pleased to introduce version 3.33 of senhasegura, which includes a range of new features and improvements across our products. This update focuses on four main areas: , , , and . Here are the highlights:

## Framework
### Accelerated Updates with Geographically Distributed Repositories

Administrators can now configure repositories and define bucket locations directly from the command line. We've also implemented a new mirror structure, making repositories available in multiple geographic locations. This allows you to choose the closest repository, reducing latency and speeding up the download of update files.

1. We have prepared clear and simplified  to guide you through the repository update process;

1. If you are using an older version of the product, you will need to , going through intermediate versions until you reach the latest version.

### Application Component and Operating System Version Updates

Version 3.33 includes essential updates to application components and the operating system. These improvements are crucial for ensuring maximum security and performance with new security features, enhanced stability, performance improvements, and storage optimizations.

## PAM Core

### Real-Time User Analysis and Protection

senhasegura’s Behavior module analyzes active user behavior. In version 3.33, we have introduced , a feature that monitors real-time actions, identifies suspicious activities, and requests additional verification to ensure user authenticity. Continuous Identification is triggered by customizable admin-defined criteria, such as attempts to start sessions outside permitted times.
:::(Info) (Info)
Continuous Identification is disabled by default.
:::

## My Safe
### External Data Sharing with Protection and Speed

The MySafe module now features , allowing temporary sharing of notes, passwords, files, and API secrets with external users. This solution facilitates secure and controlled collaboration with external parties while ensuring the integrity of sensitive data stored in MySafe.

## Domum
### Enhanced User Classification and Management

We have made significant updates to Domum Remote Access with a  solution. This restructuring improves user classification and management on the platform, allowing for clear distinctions between different types of users (full access or minimum privilege) and their affiliations (internal employees or third-party/vendors).

## Additional Update
### Explore the Updated Help Center Menu: Increased Efficiency and Ease

We have revamped our  menu to improve usability and content organization for more efficient and intuitive navigation. We have restructured categories and options to facilitate access to relevant information, enhancing user experience and making the system more fluid and professional.
