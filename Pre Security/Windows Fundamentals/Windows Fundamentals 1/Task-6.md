
![image](https://user-images.githubusercontent.com/94435318/161913340-9792786d-7221-486a-93de-a3e203761565.png)

# 🟥 Task-6 User Accounts, Profiles and Permissions

User accounts can be one of two types on a typical local Windows system: Administrator & Standard User. 

The user account type will determine what actions the user can perform on that specific Windows system. 

- An Administrator can make changes to the system: add users, delete users, modify groups, modify settings on the system, etc. 
- A Standard User can only make changes to folders/files attributed to the user & can't perform system-level changes, such as install programs.

You are currently logged in as an Administrator. There are several ways to determine which user accounts exist on the system. 

One way is to click the Start Menu and type Other User. A shortcut to System Settings > Other users should appear. 

<p align="left">
  <img src="https://user-images.githubusercontent.com/94435318/161934337-94e3eab5-c2d7-4231-bcf2-49930cd8e2f1.png">
</p>

If you click on it, a Settings window should now appear. See below.

<p align="left">
  <img src="https://user-images.githubusercontent.com/94435318/161934495-3347fac2-38fe-4850-b071-29097311b47d.png">
</p>

Since you're the Administrator, you see an option to Add someone else to this PC.

*Note: A Standard User will not see this option.*

Click on the local user account. More options should appear: Change account type and Remove. 

<p align="left">
  <img src="https://user-images.githubusercontent.com/94435318/161934647-43abee5a-bb23-4776-84c4-2ba6477b7575.png">
</p>

Click on Change account type. The value in the drop-down box (or the highlighted value if you click the drop-down) is the current account type. 

<p align="left">
  <img src="https://user-images.githubusercontent.com/94435318/161934881-d830fe69-b8a2-4d86-91b3-06ed84321445.png">
</p>

When a user account is created, a profile is created for the user. The location for each user profile folder will fall under is C:\Users.

For example, the user profile folder for the user account Max will be C:\Users\Max.

The creation of the user's profile is done upon initial login. When a new user account logs in to a local system for the first time, they'll see several messages on the login screen. One of the messages, User Profile Service, sits on the login screen for a while, which is at work creating the user profile. See below.

<p align="left">
  <img src="![image](https://user-images.githubusercontent.com/94435318/161935083-72f30f96-d7d2-458b-9f0f-f24bc6c52246.png">
</p>

Once logged in, the user will see a dialog box similar to the one below (again), indicating that the profile is in creation.

<p align="left">
  <img src="https://user-images.githubusercontent.com/94435318/161935211-3c192e43-5931-460c-bf2e-f69fa2b252d5.png">
</p>

Each user profile will have the same folders; a few of them are:

- Desktop
- Documents
- Downloads
- Music
- Pictures

Another way to access this information, and then some, is using Local User and Group Management. 

Right-click on the Start Menu and click Run. Type lusrmgr.msc. See below

<p align="left">
  <img src="![image](https://user-images.githubusercontent.com/94435318/161935484-27a944e6-9d6d-4454-ba97-dbc22f012cf3.png">
</p>

Note: The Run Dialog Box allows us to open items quickly. 

Back to lusrmgr, you should see two folders: Users and Groups. 

If you click on Groups, you see all the names of the local groups along with a brief description for each group. 

Each group has permissions set to it, and users are assigned/added to groups by the Administrator. When a user is assigned to a group, the user inherits the permissions of that group. A user can be assigned to multiple groups.

Note: If you click on Add someone else to this PC from Other users, it will open Local Users and Management

--------------------------------------------------------------------------------------------

Answer the questions below-----------------------------------------------------------------
--

### 1. What is the name of the other user account?

- Answer: tryhackmebilly

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161938269-d19381db-b64f-4c35-bd56-e425a454907f.png">
</p>
  
 ### 2. What groups is this user a member of?

- Answer: remote desktop users, users
 
<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161938772-d0b92814-193f-482a-a66b-e26f4f148e4f.png">
</p>  


### 3. What built-in account is for guest access to the computer?
 
 - Answer: Guest
 
<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161939171-6af3180b-338e-497e-a52c-5a327df29eda.png">
</p>  

### 4. What is the account status?

- Answer: account is disabled

----------------------------------------------------------------------------------------  
