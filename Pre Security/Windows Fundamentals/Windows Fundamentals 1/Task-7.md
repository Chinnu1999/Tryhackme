![image](https://user-images.githubusercontent.com/94435318/161913340-9792786d-7221-486a-93de-a3e203761565.png)

# 🟥 Task-7 User Account Control

The large majority of home users are logged into their Windows systems as local administrators. Remember from the previous task that any user with administrator as the account type can make changes to the system.

A user doesn't need to run with high (elevated) privileges on the system to run tasks that don't require such privileges, such as surfing the Internet, working on a Word document, etc. This elevated privilege increases the risk of system compromise because it makes it easier for malware to infect the system. Consequently, since the user account can make changes to the system, the malware would run in the context of the logged-in user.

To protect the local user with such privileges, Microsoft introduced User Account Control (UAC). This concept was first introduced with the short-lived Windows Vista and continued with versions of Windows that followed.

Note: UAC (by default) doesn't apply for the built-in local administrator account. 

How does UAC work? When a user with an account type of administrator logs into a system, the current session doesn't run with elevated permissions. When an operation requiring higher-level privileges needs to execute, the user will be prompted to confirm if they permit the operation to run. 

Let's look at the program on the account you're currently logged into, the built-in administrator account—Right-click to view its Properties.

In the Security tab, we can see the users/groups and their permissions to this file. Notice that the standard user is not listed. 

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161941336-1a6a3429-4704-4f6f-be2b-7ef47fd90436.png">
</p>

Log in as the standard user and try to install this program. To do this, you can remote desktop into the machine as the standard user account. 

*Note: You have the username and password for the standard user. It's visible in lusrmgr.msc.*

Before installing the program, notice the icon. Do you see the difference? When you're logged in as the standard user, the shield icon is on the program's default icon. See below.

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161941545-a1e917c7-7ae6-4f93-a795-a9d4620128cf.png">
</p>

This shield icon is an indicator that UAC will prompt to allow higher-level privileges to install the program.

![image](https://user-images.githubusercontent.com/94435318/161941684-4a884424-c695-454f-a4e3-956b702270af.png)

Double-click the program, and you'll see the UAC prompt. Notice that the built-in administrator account is already set as the user name and prompts the account's password. See below.

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161941847-31f71859-8975-4a9b-85a0-f688ea45d0a5.png">
</p>

After some time, if a password is not entered, the UAC prompt disappears, and the program does not install. 

This feature reduces the likelihood of malware successfully compromising your system. You can read more about UAC here.

------------------------------------------------------------------------------------------------

Answer the questions below--------------------------------------------------------------------
--

### What does UAC mean?

-Answer: User Account Control

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161942311-7b1cd62e-8bce-416e-ace3-fa259d1137a8.png">
</p>
  
-----------------------------------------------------------------------------------------------
