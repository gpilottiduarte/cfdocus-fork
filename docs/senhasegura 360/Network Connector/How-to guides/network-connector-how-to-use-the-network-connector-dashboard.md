## Metadata_Start 
## code: en
## title: How to use the Network Connector dashboard 
## slug: network-connector-how-to-use-the-network-connector-dashboard 
## seoTitle: How to use the Network Connector dashboard 
## description:  
## contentType: Markdown 
## Metadata_End

In this document, you’ll find a step-by-step guide on how to use the dashboard , to view data on the connection status, agents and logs.

## Requirements

It’s necessary to have the agent  installed. To do this, follow the steps in the document .

## View the Network Connector dashboard

To view data from the  dashboard, follow the steps below:

1. Access the senhasegura platform using  on port 59022 with the administrative user .
2. Run the command: .

Once the command is executed, the following screen will be displayed:

| Item 	    | Description                                                        	                    |
|-----------|-------------------------------------------------------------------------------------------|
| Name 	    | Name used for agent.                                         	                            |
| Port   	| Port used for the agent.                                                                  |
| Primary   | Main network connector agent status.                 	                                    |
| Secondary | Status of the secondary network connector agent.                 	                        |
| Offline   | The agent is offline.                                           	                        |
| Online    | The agent is connected with (number of connections) (bandwidth consumption).              |
| Tunns     | The number of devices and ports connected to the agent determines the “Tunns”. For example, a device on port 22 (192.168.0.10:22) results in Tunns equal to 1. If the same device uses another port, such as 443 (192.168.0.10:443), then Tunns equals 2. Adding another device with a new port, Tunns increases to 3.              |
| Version (P/S) | Agent version.                                                                        |

:::(Info) (Info) 
A Tunn is not added if there is already a tunnel to the same device + port. 
:::

## View logs on the Network Connector dashboard

To access the logs generated by  on the Network Connector *dashboard*, follow the steps below:

1. Access the senhasegura platform using  on port 59022 with the administrative user .
2. Enter the following command: .
3. Type  and enter.

---

Do you still have questions? Reach out to the .
