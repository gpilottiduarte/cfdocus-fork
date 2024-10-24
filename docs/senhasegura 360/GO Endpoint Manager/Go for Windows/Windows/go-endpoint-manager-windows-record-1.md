# Session recording 

The 
GO Endpoint Manager
 agent for Windows allows certain users to be monitored by video during the entire session.
Go Agent Recording Rules
The agent's recording logic for applications executed using the Go Agent is influenced by access list rules as follows:
Application Non-Recording List: If an application is on the list marked to prevent recording, it will not be recorded.
Absence of a List: The application will not be recorded if there is no list.
Permitted Recording List: An application will be recorded only if it is on a permitted recording list and there is no list denying recording for that application.
Configure parameters for recording
Record session for these application
: access the 
Go Endpoint Manager ➔ Policies ➔ Windows ➔ Access List ➔ 
⁝
  ➔ New general segregation.
Enable recording session?
: global parameter mentioned in go configuration in 
GO Endpoint Manager ➔ Settings ➔ Parameters.
Monitoring happens only when:
The global parameter and the access list are active and related to the recording. 
Applications that fit into the access list will be recorded, including those outside GO Endpoint Manager.
The global parameter is active and without an existing access list.
Any execution of GO Endpoint Manager will be recorded.
When the user starts a JIT process, all his actions will be audited by video and forwarded to the senhasegura server like a RunAs elevation.
Info
Segregated parameters apply in this scenario.
Recording report
When a user elevates an application, GO Endpoint Manager will record a video while the application is running. As soon as the execution is finished, the video is forwarded to the senhasegura server, making it available for evaluation.
Caution
Through the 
Session Video
 record action, you can watch the video. However, this functionality will only be available if the 
Enable session recording
 parameter is active.
To view a recorded session: 
Access the senhasegura platform. 
Access the menu
 PAM Core ➔ Access control ➔ Remote sessions. 
In the 
Proxy
 field, filter by 
GO Endpoint Manager
.
Click the 
Action
 play button to view the recording.
Info
Videos only appear after the service restarts and finish uploading videos. This process takes 15 minutes.
For administrators
Administrators of this process can check the recordings made in a certain period.
Access the 
Event Viewer,
 which makes it possible to monitor the sending of each video. Check the 
%programdata%\\go\\recordFiles
 folder to see the video files of the recordings in progress and already finished, as shown in the example below:
Types of recording
1. Any execution:
Core applications (execute, control panel, network adapters, uninstall).
2. Just-in-time:
The entire session is recorded until the user logs off or until the user cancels just in time.
3. Automation:
All automation is carried out in the process.
Important
Actions performed on Network Adapters and credential withdrawal is not recorded.