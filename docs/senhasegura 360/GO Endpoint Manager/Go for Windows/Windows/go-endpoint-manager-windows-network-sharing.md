# Network Sharing 

This menu displays the shared network directories of the user. Credentials are used to access a directory without exposing or mapping it.
GO Endpoint Manager Core - Network Sharing
Configure file sharing 
On Windows:
Access the user's desktop.
Locate the folder you want to share, or create a new one.
Select the folder.
Right-click on it and choose 
Properties
.
Select the 
Sharing
 tab and then the 
Share
 button.
Choose the users you want to share the folder with and click 
Add.
Click the 
Share
 button.
Copy the path. Example: \WINDOWS10PRO\Shared Folder
Done
.
On the GO application:
Start 
Core
.
Click 
Network Sharing
.
In the central area of the screen, right-click and select 
Add sharing
.
Enter the path of the folder that you will share. Example: \WINDOWS10PRO\Shared Folder
OK
.
Access or remove shared folders on GO
The user can access a shared folder using the selected credential. The credential is not necessarily a domain one.
Start 
Core
.
Click 
Network Sharing
.
Select the folder you want to access or unshare.
Right-click and choose one of the following options from the context menu:
Access sharing
Delete sharing
Info
The folders accessed by Core are registered and can be reaccessed due to the cache of credentials managed by Windows. These folders won't be mapped as a drive.
Access shared folders outside of GO
Once authenticated, Windows creates a local cache with network access allowing the folder to be viewed without GO Endpoint Manager.