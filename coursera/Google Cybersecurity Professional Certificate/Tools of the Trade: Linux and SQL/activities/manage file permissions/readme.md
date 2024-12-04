<h1>Use Linux commands to manage file permissions</h1>
<h3>Project description</h3>
&emp;For this senario, the reaserch team at my orginization neeeds updated file permision for the reaserch team for certian files and directories within the projects directory. The current permissions do not reflect the required authrizations. Checking and updating these permisions will increase overal security of the system.

<h3>Checking File and directory details</h3>
<img src="https://github.com/BradRoff/write-up/blob/d0f969f64097b5339e301c24a5732c6055d39e88/coursera/Google%20Cybersecurity%20Professional%20Certificate/Tools%20of%20the%20Trade%3A%20Linux%20and%20SQL/activities/manage%20file%20permissions/img/1.png">
<p>
&emp;The screen shot above is the command I entered and its result. The command "ls -la" shows detailed infromation on each file and directory in the current directory even if it is hidden. Currently we are looking at a detailed list of the projects directoy which includes all hidden files and their respective permisions. Their are six projects one being hidden indicated by starting '.' being '.project_x.txt'. The first ten character string is what we will be changing as that is what determins the permissions for each file. The ten character string can be broken into four sections:
<table>
 <tr>
    <th>Character/s</th>
    <th>Description</th>
    
  </tr>
  <tr>
    <td>1st character</td>
    <td>will be a 'd' or '-' for if it a directory or a file respectively</td>
  </tr>
  <tr>
    <td>2nd-4th characters</td>
    <td>Determines the read write and exicute permisions of the user. Also known as the rwx, if one is '-' permission is not granted.</td>
  </tr>
  <tr>
    <td>5nd-7th characters</td>
    <td>Determines the read write and exicute permisions of the group. </td>
  </tr>
  <tr>
    <td>8nd-10th characters</td>
    <td>Determines the read write and exicute permisions of the other. As the name sounds, other includes anyone outside the user or the group. </td>
  </tr>
</table>
</p>
<h3>Changing File Permissions</h3>
</p>&emp;
The orginization decided that others should never have write access to any of their files. To follow this looking at the previous image we can see the project.k.txts permmissions need to be changed as '-rw--w--rw-' gives othersthe permission to write. 
</p>
The following is the code I used to change the file permissions for project.k.txt.
<img src ="https://github.com/BradRoff/write-up/blob/697d218242410127417cc50d5b8a9001e93c4801/coursera/Google%20Cybersecurity%20Professional%20Certificate/Tools%20of%20the%20Trade%3A%20Linux%20and%20SQL/activities/manage%20file%20permissions/img/2.png">
<p>&emp;
The first line shows the command I used 'chmod o-w project_k.txt'. This removes write permissions from the others for project_k.txt. The seccond line command shows the detailed information for the result, but this time I only showed the single file by using 'ls project_k.txt -la' instead of showing the current directory.</p>
<p>As the reasherch team arcived 'project_x.txt.' they don't want anyone to have write access to this project, but user and group should have read access. Looking back at file permissions we see that the hidden file '.project_x.txt' are '-rw--w----'. Luckly, we can chain file permission changes on the same prompt. </p>
<img src = "https://github.com/BradRoff/write-up/blob/27f2dd28d2e81340361b30918fe50ed96d958193/coursera/Google%20Cybersecurity%20Professional%20Certificate/Tools%20of%20the%20Trade%3A%20Linux%20and%20SQL/activities/manage%20file%20permissions/img/3.png">

[Add content here.]
Change directory permissions
[Add content here.]
Summary
[Add content here.]
