<h1>Use Linux Commands to Manage File Permissions</h1>

<h3>Project Description</h3>
<p>&emsp;For this scenario, the research team at my organization needs updated file permissions for certain files and directories within the project directory. The current permissions do not reflect the required authorizations. Checking and updating these permissions will increase the overall security of the system.</p>

<h3>Checking File and Directory Details</h3>
<img src="https://github.com/BradRoff/write-up/blob/d0f969f64097b5339e301c24a5732c6055d39e88/coursera/Google%20Cybersecurity%20Professional%20Certificate/Tools%20of%20the%20Trade%3A%20Linux%20and%20SQL/activities/manage%20file%20permissions/img/1.png">
<p>&emsp;The screenshot above shows the command I entered and its result. The command "ls -la" shows detailed information on each file and directory in the current directory, even if they are hidden. Currently, we are looking at a detailed list of the project directory, which includes all hidden files and their respective permissions. There are six projects, one of which is hidden, indicated by the filename starting with a dot (e.g., '.project_x.txt'). The first ten-character string is what we will be changing, as it determines the permissions for each file. The ten-character string can be broken into four sections:</p>

<table>
  <tr>
    <th>Character/s</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>1st character</td>
    <td>Will be a 'd' for a directory or a '-' for a file.</td>
  </tr>
  <tr>
    <td>2nd-4th characters</td>
    <td>Determine the read, write, and execute permissions of the user (also known as rwx). If one is '-', permission is not granted.</td>
  </tr>
  <tr>
    <td>5th-7th characters</td>
    <td>Determine the read, write, and execute permissions of the group.</td>
  </tr>
  <tr>
    <td>8th-10th characters</td>
    <td>Determine the read, write, and execute permissions of others (anyone outside the user or group).</td>
  </tr>
</table>

<h3>Changing File Permissions</h3>
<p>&emsp;The organization decided that others should never have write access to any of their files. Looking at the previous image, we can see that the file "project.k.txt" needs its permissions changed. The current permissions '-rw--w--rw-' give others permission to write, which violates the policy.</p>
<p>&emsp;The following is the command I used to change the file permissions for "project.k.txt":</p>
<img src="https://github.com/BradRoff/write-up/blob/697d218242410127417cc50d5b8a9001e93c4801/coursera/Google%20Cybersecurity%20Professional%20Certificate/Tools%20of%20the%20Trade%3A%20Linux%20and%20SQL/activities/manage%20file%20permissions/img/2.png">
<p>&emsp;The first line shows the command I used: 'chmod o-w project_k.txt'. This removes write permissions from others for "project_k.txt". The second line shows the detailed information for the result, but this time I only show the single file by using 'ls project_k.txt -la' instead of showing the entire directory.</p>

<p>&emsp;Since the research team archived "project_x.txt" and does not want anyone to have write access to this project, but the user and group should have read access, we can see that the hidden file ".project_x.txt" has the permissions '-rw--w----'. Fortunately, we can chain file permission changes in the same command.</p>
<img src="https://github.com/BradRoff/write-up/blob/27f2dd28d2e81340361b30918fe50ed96d958193/coursera/Google%20Cybersecurity%20Professional%20Certificate/Tools%20of%20the%20Trade%3A%20Linux%20and%20SQL/activities/manage%20file%20permissions/img/3.png">
<p>&emsp;The second line shows the command I entered to remove the group and user's write permissions with 'g-w,u-w' and to remove the group's read permission with 'g-r'. By chaining them with commas (no spaces), we can execute them in one command.</p>

<h3>Changing the Directory Permissions</h3>
<p>&emsp;The organization only wants "researcher2" to have access to the "drafts" directory and its contents. Currently, the "others" group has execute permission on the "drafts" directory, so I need to remove that permission.</p>
<img src="https://github.com/BradRoff/write-up/blob/a5e35a9eab4079a12299cad3ab4c01321cdc53a6/coursera/Google%20Cybersecurity%20Professional%20Certificate/Tools%20of%20the%20Trade%3A%20Linux%20and%20SQL/activities/manage%20file%20permissions/img/4.png">
<img src="https://github.com/BradRoff/write-up/blob/a5e35a9eab4079a12299cad3ab4c01321cdc53a6/coursera/Google%20Cybersecurity%20Professional%20Certificate/Tools%20of%20the%20Trade%3A%20Linux%20and%20SQL/activities/manage%20file%20permissions/img/5.png">
<p>&emsp;The first command 'chmod g-x drafts' removes the execute permission from others for the "drafts" directory. The resulting permissions 'drwx------' show that no further modifications are needed.</p>

<h3>Summary</h3>
<p>&emsp;Through this exercise, I changed multiple file and directory permissions to align with the authorization standards set by my company. Using 'ls -la' provided the necessary details to proceed with the task, allowing me to make informed decisions about which permissions to change. The resulting structure is now more secure.</p>
