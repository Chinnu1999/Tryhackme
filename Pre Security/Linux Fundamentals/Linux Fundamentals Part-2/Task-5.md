![image](https://user-images.githubusercontent.com/94435318/161464318-2f53b4ec-ce25-4f2f-ad52-470231458957.png)

# 🟥 Task-5 Permissions 101

As you would have already found out by now, certain users cannot access certain files or folders. We've previously explored some commands that can be used to determine what access we have and where it leads us. 

In our previous tasks, we learned how to extend the use of commands through flags and switches. Take, for example, the ls command, which lists the contents of the current directory. When using the -lswitch, we can see ten columns such as in the screenshot below. However, we're only interested in the first three columns:

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161685701-93ea4e2d-c7bc-4d6f-82c5-7b0b9dbd819f.png">
</p> 

Although intimidating, these three columns are very important in determining certain characteristics of a file or folder and whether or not we have access to it. A file or folder can have a couple of characteristics that determine both what actions are allowed and what user or group has the ability to perform the given action -- such as the following:

    -> Read
    -> Write
    -> Execute 

Using su to switch to user2

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161685852-b4fb4bef-8233-4bb1-83b5-cc59ce825663.png">
</p>

Let's use the "cmnatic.pem" file in our initial screenshot at the top of this task. It has the "-" indicator highlighting that it is a file and then "rw" followed after. This means that only the owner of the file can read and write to this"cmnatic.pem" file but cannot execute it.

## Briefly: The Differences Between Users & Groups

We briefly explored this in Linux fundamentals part 1 (namely, the differences between a regular user and a system user). The great thing about Linux is that permissions can be so granular, that whilst a user technically owns a file, if the permissions have been set, then a group of users can also have either the same or a different set of permissions to the exact same file without affecting the file owner itself.

Let's put this into a real-world context; the system user that runs a web server must have permissions to read and write files for an effective web application. However, companies such as web hosting companies will have to want to allow their customers to upload their own files for their website without being the webserver system user -- compromising the security of every other customer. 

We'll learn the commands necessary to switch between users below.

## Switching Between Users

Switching between users on a Linux install is easy work thanks to the su command. Unless you are the root user (or using root permissions through sudo), then you are required to know two things to facilitate this transition of user accounts:

     -> The user we wish to switch to
     -> The user's password

The su command takes a couple of switches that may be of relevance to you. For example, executing a command once you log in or specifying a specific shell to use. I encourage you to read the man page for su to find out more. However, I will cover the -l or --login switch.

Simply, by providing the -lswitch to su, we start a shell that is much more similar to the actual user logging into the system - we inherit a lot more properties of the new user, i.e., environment variables and the likes. 

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161685950-6739c2a6-fc1e-47c2-a477-903095c0efde.png">
</p>

For example, when using su to switch to "user2", our new session drops us into our previous user's home directory. 

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161686030-a286dc14-a386-4de9-961c-03144afae6fe.png">
</p>

Where now, after using -l, our new session has dropped us into the home directory of "user" automatically. 

---------------------------------------------------

Answer the questions below--------------------------------------------------------
--

### 1. On the deployable machine, who is the owner of "important"?

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161684069-3e514554-85f5-4644-9b6d-83b4e8d43305.png">
</p>

### Answer: user2

### 2. What would the command be to switch to the user "user2"?

### Answer: su user2

### 3. Now switch to this user "user2" using the password "user2"

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161686563-2ad0ae91-c39f-4ab5-b56e-f7f7de7d294c.png">
</p>

### 4. Output the contents of "important", what is the flag?

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161683936-5ba193b7-8c96-4b82-a134-7a395d16e5a4.png">
</p>  

### Answer" THM{SU_USER2}

--------------------------------------------------------------------------------------------
