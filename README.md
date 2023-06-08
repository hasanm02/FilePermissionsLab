# File Permissions in Linux


<h2>Project Description</h2>
My company's research team needs to change the file permissions for a few specific files and folders in the projects directory. The degree of permission that should be granted is not yet reflected in the permissions. Their system will remain safe if these permissions are checked and updated. I did the following things to finish this task:
<br />



<h2>Check file and directory details</h2>

<p align="center">
The following code demonstrates how I used Linux commands to determine the existing
permissions set for a specific directory in the file system: 
  <br/>
  
  
<img src="https://i.imgur.com/i30Xw0H.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
 
  The code contains a list of every item in the projects directory. To display a comprehensive listing of the file contents, I used the ls program with the -l option. My command's output shows that there is one directory named drafts and four other project files. The permissions assigned to each file or directory are represented by the 10-character string in the first column. <br/>
  
  
  <h2>Change file permissions</h2>

<p align="center">
The company decided that other should not be able to have write access to any of their files. I referenced back to the file permissions that I had previously returned in order to comply with this. I came to the conclusion that other should not have write access to project_k.txt.

The code below shows how I accomplished this using Linux commands:
<br/>
  
  
<img src="https://i.imgur.com/2mqcfED.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
 
 The chmod command modifies files and directories permissions. The second argument provides the file or directory, while the first argument specifies which permissions should be altered. In this case, I disabled other ability to write to the project_k.txt file. I then ran ls -l to look over the adjustments I had made. I repeated this process with the project_m.txt file but removed the read permissions from group instead. <br/>
 
  
 <h2>Check file permissions on a hidden file</h2>

<p align="center">
Project_x.txt was recently archived by my organization's research team. The user and group should only be able to have read access, they do not want anyone to have write access.

The code below shows how I changed the permissions using Linux commands:
<br/>
  
  
<img src="https://i.imgur.com/8NmE1Cu.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
 
  Because it begins with a period (.), .project_x.txt is a secret file. In this illustration, I gave the group read capabilities while removing write permissions from the user and group. I used u-w to take the user's write permissions away. I then added read permissions to the group with g+r and deleted write permissions with g-w. <br/>
  
  
   <h2>Check directory permissions</h2>

<p align="center">
Only the researcher2 user should have access to the drafts directory and its contents, according to my organization. This indicates that only researcher2 should be granted execute permissions.

The code below shows how I changed the permissions using Linux commands:
<br/>
  
<img src="https://i.imgur.com/LThdieY.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
 
 I used the chmod command to remove the execute rights after previously verifying that the group possessed them. It was not necessary to add execute rights because the researcher2 user already had them. <br/>
  
 
<h2>Summary</h2>
I altered a number of permissions to make sure that the projects directory's files and directories had the amount of access that my business required. The directory's permissions were checked using ls -la as the initial step in this process. This influenced my choices in the subsequent steps. Then, to modify the permissions on files and directories, I repeatedly used the chmod program.
<br />
  
  
  
  

  
  
  
