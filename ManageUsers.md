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

 <h2>Adding users and group</h2>

The organization would like to add researcher9 to the system and add him to the
research_team group as his primary group. Here’s the command:
1. Sudo useradd researcher9
Ketmanto Wangsa - Cybersecurity Portfolio
2. Sudo usermod -g research_team researcher9
Alternatively, we can perform both steps at once:
1. Sudo useradd researcher9 -g research_team
   
<h2>Assign file ownership </h2>

Researcher9 will take over project_r and the owner has to be him (project_r.txt).
The project_r.txt is located in the /home/researcher2/projects and is currently
owned by researcher2.
The command to make it happen is:
sudo chown researcher9 /home/researcher2/projects/project_r.txt

<h2>Add the user to a secondary group</h2>

A few months later, researcher9 is now working in both the research and sales
departments. My task is to add resesarcher9 to the sales department as a secondary
group without removing him from research department. Sales team is sales_team.
Sudo usermod -a -G sales_team researcher9

<h2>Delete a user</h2>

A year later, researcher9 decided to leave the company. In this task, I have to remove him from
the system. The command to make it happen is:
1. sudo userdel researcher9 (Will not remove it. Please refer to “describe the
command” section)
2. sudo groupdel researcher9
