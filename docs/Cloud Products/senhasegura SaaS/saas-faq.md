## Metadata_Start 
## code: en
## title: FAQ 
## slug: saas-faq 
## seoTitle: FAQ 
## description:  
## contentType: Markdown 
## Metadata_End
## 

### 

*   
  * senhasegura is responsible for taking these snapshots daily and before scheduled maintenance.

### 

*   
  * In the SaaS model, updates are handled by support according to the manufacturer’s schedule. In the Private SaaS model, updates are coordinated between the support team and the client.

## 

### 

*   
  * Snapshots capture a complete image of the application, allowing for restoration in the event of unavailability or an incident.

### 

*   
  * Local backups allow for “break the glass” procedures without requiring access to the cloud, ensuring device access during unavailability.

### 

*   
  * Credential backups are stored on the client's network for "break the glass" procedures.

### 

*   
  * senhasegura defines the service provider for SaaS. Clients preferring a different provider must opt for the on-premises version.

### 

*   
  * By default, no. senhasegura uses Google's contingency services for data availability. Multi-region architectures require an additional service contract.  
*   
  * DR environments aren't typically included by default in senhasegura offerings; they involve extra costs and complex arrangements.

### 

*   
  * Google's environment includes region-specific backup systems. Inter-region backup services are available separately.

### 

*   
  * Customers can back up videos and credentials on a personally managed server, be it cloud-based or physical. Daily snapshots by senhasegura are stored on GCP in the same region as the instance.

## 

### 

*   
  * GCP's multiple data centers within each region ensure transparent failovers, minimizing failure risks.

### 

*   
  * Intrusion tests coincide with each software update in the hosting environment, utilizing market-standard tools and external consultants.

### 

*   
  * senhasegura employs comprehensive operational policies certified by ISO 27001 to prevent errors.

## 

### 

*   
  * Access by the senhasegura team is limited to the client's network, with all activities logged for audit trails.

### 

*   
  * In the new SaaS model, only senhasegura can access the Orbit menu. Clients have Orbit access in the Private SaaS setup.

## 

### 

*   
  * In the SaaS model, senhasegura manages system backups, while password backups fall to the client via rsync. Private SaaS clients manage both system and password backups independently.

