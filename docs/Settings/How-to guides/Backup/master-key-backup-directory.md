# Backup directory 

Configure the encrypted data storage directory
Before creating the 
Master Key
, it is necessary to configure the export location of the encrypted data. Remember that this directory must be known to the parties' guardians.
Caution
This step is unnecessary if you are configuring a senhasegura SaaS instance. Go to step 
Generate remote ceremony from the master key
.
Within the module and menu 
Settings ➔ Backup ➔ Servers
, you will access the records of the directory where senhasegura internally forwards the backup.
Create a new record via the 
New
 report action button
Choose how the backup will be stored
Fill in your directory
Caution
If you choose 
Local Directory
, keep the default data and click 
Save
.
Fill in the 
Host
, 
Port
, and the 
Credential for authentication
Click 
Save
Backup server registration
 
This directory is the same directory where the database and session files backup was configured. The 
Master Key
 files are forwarded to this same directory and automatically directed to the remote directory configured in the backup step.