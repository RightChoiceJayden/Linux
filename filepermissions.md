# File Permissions in Linux
<h2>Description</h2>

In this scenario, I modify the permissions for files and
directories within the project directory. The operating system is Linux, indicating that the
tasks require a command-line interface (Linux Bash shell) approach via Linux Terminal.
</b>

<h2>Tools</h2>

- <b>Linux OS</b> 

- <b>Linux Bash Shell</b> 

- <b>Linux Terminal</b> 
</b>

## Check File and Directory Details

To begin with, I wrote the command <mark>ls</mark> to display what directories are available. As the result
goes, the <mark>project</mark> is the only directory listed. Then, the command <mark>ls</mark> with the <mark>-la</mark> displays
file contents as well as the hidden files within the <mark>project</mark> directory . The result shows
there is one hidden file within the directory. In this case, <mark>”.project_x.txt”</mark> is the hidden
file. Other findings include four project files (ends with .txt) and one <mark>drafts</mark> directory.

![FP1](https://github.com/user-attachments/assets/75e71453-f18d-4827-8766-1d69340c109a)

## Permission String Descripition

The 10-character string determines the authorization of accessing the file and their specific
permissions. The characters and what they represent are as follows:

<b>drwxr-xr-x</b> 

- <b>1st character:</b> This character is either a d or hyphen (-) and indicates the file type.
Character d shows that it is a directory and drafts is the example. A hyphen (-) shows
that it is a regular file.

- <b>2nd-4th characters:</b> These characters indicate the read (r), write (w), and execute (x)
permissions for the user. When one of these characters is a hyphen (-) instead, it
indicates that this permission is not granted to the <b>user</b>.

- <b>5th-7th characters:</b> These characters indicate the read (r), write (w), and execute (x)
permissions for the group. When one of these characters is a hyphen (-) instead, it
indicates that this permission is not granted for the <b>group</b>.

- <b>8th-10th characters:</b> These characters indicate the read (r), write (w), and execute (x)
permissions for others. It includes all other users on the system that are not users and
the group. When one of these characters is a hyphen (-) instead, that indicates that
this permission is not granted for <b>others</b>.

## Change File Permissions

The command chmod allows us to change the file permissions. To do this, there are some
important notes:
1. The command <mark>chmod u+(r/w/x) project file name</mark> allows us to add the file
permissions for the <b>users</b>.
2. The command <mark>chmod u-(r/w/x) project file name</mark> allows us to remove the
file permissions for the <b>users</b>.
3. The command <mark>chmod g+(r/w/x) project file name</mark> allows us to add the file
permissions for the <b>group</b>.
4. The command <mark>chmod g-(r/w/x) project file name </mark> allows us to remove the
file permissions for the <b>group</b>.
5. The command <mark>chmod o+(r/w/x) project file name </mark> allows us to add the file
permissions for <b>others</b>.
6. The command <mark>chmod o-(r/w/x) project file name </mark> allows us to remove the
file permissions for <b>others</b>.

<ins>Changes</ins>

1. <mark>chmod o-w project_k.txt</mark> to remove write permissions
from the file.
2. <mark>chmod g-r project_m.txt</mark> to remove read permissions from
the file.

![FP2](https://github.com/user-attachments/assets/8fbb11d7-963b-47e4-b6c8-d1e5986880ca)



