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

Notice that all the commands require <mark>sudo</mark>. <mark>sudo</mark> means “super user do!”. 

 <h2>Adding users and group</h2>

Add  <mark>researcher9</mark> to the system and add him to the
 <mark>research_team</mark> group as his primary group. Here’s the command:

 <mark>sudo useradd researcher9 -g research_team</mark> 
   
<h2>Assign file ownership </h2>

<mark>Researcher9</mark> will take over  <mark>project_r</mark> as the owner.
The <mark>project_r.txt</mark> is located in the /home/researcher2/projects and is currently
owned by <mark>researcher2</mark>.
The command is:

 <mark>sudo chown researcher9 /home/researcher2/projects/project_r.txt</mark> 
 
<h2>Add the user to a secondary group</h2>

Add  <mark>resesarcher9</mark> to the sales department as a secondary
group without removing him from research department. Sales team is  <mark>sales_team</mark> 

 <mark>sudo usermod -a -G sales_team researcher9</mark>

<h2>Delete a user</h2>

A year later, <mark>researcher9</mark> decided to leave the company. In this task, I remove him from
the system. The command to make it happen is:

 <mark>sudo groupdel researcher9</mark>
