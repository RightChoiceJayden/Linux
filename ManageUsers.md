# Manage Users in Linux
<h2>Description</h2>

In this scenario, a new employee (researcher9) just joined the organization. As a result, I manage the user access within the organization. 
</b>

<h2>Tools</h2>

- <b>Linux OS</b>
- <b>Linux Bash Shell</b>
- <b>Linux Terminal</b>

<h2>Commands</h2>

The following are the commands when managing the user access:
1. <mark>useradd</mark> allows us to add users to the system.

<mark>sudo useradd researcher9</mark>

2.  <mark>usermod</mark>  allows us to assign the users to a specific group as well as a secondary group.

 <mark>sudo usermod -g research_team researcher9</mark>
 
3.  <mark>userdel</mark> allows us to delete the users from the system.
   
 <mark>sudo userdel researcher9</mark>
 
4.  <mark>groupdel</mark> allows us to delete the user’s group.
   
 <mark>sudo groupdel researcher9</mark> 
 
 (When a new user is created, a group with the same
name as the user is also created and that user is the only member of that group. After
removing users, it is highly recommended to clean up any such empty groups that are
left behind).

5. <mark>chown</mark> allows us to assign file ownership.

<mark>sudo chown researcher9 /home/researcher2/projects/project_r.txt </mark>

Notice that all the commands require <mark>sudo</mark>. <mark>Sudo</mark> means “super user do!”. 
