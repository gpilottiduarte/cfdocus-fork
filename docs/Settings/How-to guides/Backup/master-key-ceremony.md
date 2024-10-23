# Master key ceremony 

Adding guardians
Most master key ceremonies take place in person. However, when circumstances make it impossible for the people responsible for the key parts (a.k.a. guardians) to meet in person, senhasegura offers an option to perform the 
Master key
 ceremony remotely.
Important
This feature is only available in version 3.6 and higher and requires an SMTP email account set as default.
Info
The following events are logged to 
Syslog
:
Start date and time
Details of each access to a key part
Download details of the PDF file containing the key part
End date and time
Form to define a new Master Key
 
To perform the master key ceremony remotely, go to 
Settings ➔ Backup ➔ Define a new master key
.
Fill in the 
Number of parts to restore
Add the 
Guardians
Click on 
Generate New Key
Note
The minimum number of parts to restore is 
2
.
Important
For security reasons, we recommend choosing two or three times as many guardians as the number of parts needed to restore your key.
Note
The email address of each Guardian must be registered in the platform.
Only active users can serve as guardians.
Guardians must have enough privilege to 
View passwords
 to be able to access a key part during the ceremony.
No user can guard more than a single part of the key.
Make sure you trust all the guardians. This is crucial to prevent any security breaches.
Tracking progress
senhasegura provides a dashboard where you can check the status of your ceremony and which guardians have already viewed their key part. Go to 
Settings ➔ Backup ➔ Master Key Ceremony
.
Here you can keep track of:
Details of the guardian users, such as Name, Phone number, Email address, Ceremony Status, User Status in the Vault, Last Login, Last Viewed, and Last Download of their key part.
Minimum required guardians to restore the master key
Start date and time
End date and time
Shortcut to create a new master key
Note
You can find a backup log in 
Setting ➔ Backup ➔ Backup log
s
.