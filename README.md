<h1>File Permissions in Linux</h1>



<h2>Description</h2>
The research team at my organization needs to update the file permissions for certain files and directories within the projects directory. The permissions do not currently reflect the level of authorization that should be given. Checking and updating these permissions will help keep their system secure. To complete this task, I performed the following tasks: 
<br />


<h2>Check File and Directory Details</h2>

<br/>
<img src="https://imgur.com/pnG940H.png" height="80%" width="80%" alt="Check File and Directory"/>
<img src="https://imgur.com/YAqwQ5p.png" height="80%" width="80%" alt="Check File and Directory"/>
<br />

- <b>The pwd command was used to print the working directory onto the screen, then the ls command was used to display the names of files and directories in the current working directory. Lastly, the cd command was used for me to navigate between the directories. In this case I wanted to change directories to go into projects so that I can be in the file.</b>


<img src="https://imgur.com/dwQHBEu.png" height="80%" width="80%" alt="Check File and Directory"/>
- <b>I then wanted to check the file and directory details so I used the ls -l command to display the the permissions to the files and directory.</b> 

<h2>Describe the Permissions String </h2>
<img src="https://imgur.com/TLMYNnp.png" height="80%" width="80%" alt="Check File and Directory"/>

- <b>The first line of the screenshot displays the command I entered, and the other lines display the output. The code lists all contents of the projects directory. I used the ls command with the -la option to display a detailed listing of the file contents that also returned hidden files. The output of my command indicates that there is one directory named drafts, one hidden file named .project_x.txt, and five other project files. The 10-character string in the first column represents the permissions set on each file or directory.
- The 10-character string can be deconstructed to determine who is authorized to access the file and their specific permissions. The characters and what they represent are as follows:
- The 1st character indicates the file type. The d indicates it’s a directory. When this character is a hyphen (-), it's a regular file.
- The 2nd-4th characters indicate the read (r), write (w), and execute (x) permissions for the user. When one of these characters is a hyphen (-) instead, it indicates that this permission is not granted to the user.
- The 5th-7th characters indicate the read (r), write (w), and execute (x) permissions for the group. When one of these characters is a hyphen (-) instead, it indicates that this permission is not granted for the group.
- The 8th-10th characters indicate the read (r), write (w), and execute (x) permissions for the owner type of other. This owner type consists of all other users on the system apart from the user and the group. When one of these characters is a hyphen (-) instead, that indicates that this permission is not granted for other.
  
- For example, the file permissions for project_k.txt are -rw-rw-rw- . Since the first character is a hyphen (-), this indicates that project_k.txt is a file, not a directory. The second, fifth, and eight characters are all r, which indicates that user, group, and other all have read permissions. The third, sixth, sixth, and ninth characters are w, which indicates that user, group, and other all have write permissions. The fourth,seventh, and tenth characters only have a hyphen ( - ), which means no one can execute permissions for project_k.txt.</b> 

<h2>Change File Permissions</h2>

- <b>The organization determined that other shouldn't have write access to any of their files. To comply with this, I referred to the file permissions that I previously returned. I determined project_k.txt must have the write access removed for other.

The following code demonstrates how I used Linux commands to do this:
</b> 

<img src="https://imgur.com/dwQHBEu.png" height="80%" width="80%" alt="Check File and Directory"/>

- <b>To comply with this, I referred to the file permissions that I previously returned. After listing the file permissions, it appears that the owner type of other should not have writing permissions and therefore it has been removed from project_k.txt using the chmod command to update the file permissions. The first two lines display the commands I entered, and the other lines display the output of the second command. The chmod command changed the permissions on the files and directories. The first argument indicates what permissions should be changed, and the second argument specifies the file or directory. After removing write permissions from other for project_k.txt file, I used ls -la to review the updates I made.</b>

<img src="https://imgur.com/GakPn6Z.png" height="80%" width="80%" alt="Check File and Directory"/>

- <b>The read permissions for the owner type of group should be removed off of project_m.txt and therefore it has also been removed using the chmod command, which is commonly used to change permissions on files and directories to help manage authorizations.</b>

<img src="https://imgur.com/g0o89zn.png" height="80%" width="80%" alt="Check File and Directory"/>

<h2>Environments Used </h2>

- <b>Windows 10</b> (21H2)

- <h2>Environments Used </h2>

- <b>Windows 10</b> (21H2)

- <h2>Environments Used </h2>

- <b>Windows 10</b> (21H2)

- <h2>Environments Used </h2>

- <b>Windows 10</b> (21H2)

<p align="center">
Launch the utility: <br/>
<img src="https://i.imgur.com/62TgaWL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Select the disk:  <br/>
<img src="https://i.imgur.com/tcTyMUE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Enter the number of passes: <br/>
<img src="https://i.imgur.com/nCIbXbg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Confirm your selection:  <br/>
<img src="https://i.imgur.com/cdFHBiU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Wait for process to complete (may take some time):  <br/>
<img src="https://i.imgur.com/JL945Ga.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Sanitization complete:  <br/>
<img src="https://i.imgur.com/K71yaM2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Observe the wiped disk:  <br/>
<img src="https://i.imgur.com/AeZkvFQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
