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

- <b> The file permissions displayed the file and directory to make sure the read permissions were removed from the owner type of group. The ls -la command was used to display permissions to files and directories including the hidden files.</b>

<h2>Change file permissions on a hidden file</h2>

- <b>The research team at my organization recently archived the project_x.txt file. They do not want anyone to have write access to this project, however, the user and group should have read access.

The following code demonstrates how I used Linux commands to change the permissions:
</b>

<img src="https://imgur.com/rRi2lls.png" height="80%" width="80%" alt="Check File and Directory"/>

- <b>The file permissions on the hidden file .project_x.txt was changed so that both the user and the group can read, but not write to the file. The first two lines of the screenshot display the commands I entered, and the other lines display the output of the second command. I know .project_x.txt  is a hidden file because it starts with a period (.). In this example, I removed write permissions from the user and group, and added read permissions to the group. I removed write permissions from the user with u-w. Then, I removed write permissions from the group with g-w, and added read permissions to the group with g+r.</b>

- <h2>Change Directory Permissions </h2>

- <b>My organization only wants the researcher2 user to have access to the drafts directory and its contents. So no users other than researcher2 should have execute permissions.

The following code demonstrates how I used Linux commands to change the permissions:
</b> 

<img src="https://imgur.com/rRi2lls.png" height="80%" width="80%" alt="Check File and Directory"/>

- <b>When listed it is seen that the file permissions have been updated so both the user and group are able to read and not write the file. The output displays the permission listing for several files and directories. Line 1 indicates the current directory (projects), and line 2 indicates the parent directory (home). Line 3 indicates a regular file titled <em>.project_x.txt.</em> Line 4 is the directory (drafts) with restricted permissions. You are able to see that only researcher2 has execute permissions. It was previously listed that the group had execute permissions, so I used the <em>chmod</em> command to remove them. The <em>researcher2</em> user already had execute permissions, so they did not need to be added.</b>

- <h2>Summary </h2>

- <b>I changed and updated multiple permissions to match the level of authorization my organization wanted for files and directories in the <em>projects</em> directory. The first step in this was using <em>ls -la</em> to check the permissions for the directory. This helped me to make the proper decisions in following the steps. I used the <em>chmod</em> command several times to change the permissions on files and directories.</b>




<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
