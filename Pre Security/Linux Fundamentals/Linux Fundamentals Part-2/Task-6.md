![image](https://user-images.githubusercontent.com/94435318/161464318-2f53b4ec-ce25-4f2f-ad52-470231458957.png)

# 🟥 Task-6 Common Directories

## /etc

This root directory is one of the most important root directories on your system. The etc folder (short for etcetera) is a commonplace location to store system files that are used by your operating system. 

For example, the sudoers file highlighted in the screenshot below contains a list of the users & groups that have permission to run sudo or a set of commands as the root user.

Also highlighted below are the "passwd" and "shadow" files. These two files are special for Linux as they show how your system stores the passwords for each user in encrypted formatting called sha512.##

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161686966-12d7fa65-5c77-4220-8a3e-3dba85823f44.png">
</p>  

## /var

The "/var" directory, with "var" being short for variable data,  is one of the main root folders found on a Linux install. This folder stores data that is frequently accessed or written by services or applications running on the system. For example, log files from running services and applications are written here (/var/log), or other data that is not necessarily associated with a specific user (i.e., databases and the like).

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161687073-31cf3e79-a37b-49cb-9085-f8182ec8113c.png">
</p>

## /root

Unlike the /home directory, the /root folder is actually the home for the "root" system user. There isn't anything more to this folder other than just understanding that this is the home directory for the "root" user. But, it is worth a mention as the logical presumption is that this user would have their data in a directory such as "/home/root" by default.  

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161687159-c4f10d87-1ee1-4ddd-9308-fbd2cd38c34b.png">
</p>

## /tmp

This is a unique root directory found on a Linux install. Short for "temporary", the /tmp directory is volatile and is used to store data that is only needed to be accessed once or twice. Similar to the memory on your computer, once the computer is restarted, the contents of this folder are cleared out.

What's useful for us in pentesting is that any user can write to this folder by default. Meaning once we have access to a machine, it serves as a good place to store things like our enumeration scripts.

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161687241-af29f59a-f2e2-4734-ae19-313e6124620e.png">
</p>

-------------------------------------------------------------------------------------

Answer the questions below------------------------------------------------
--

### 1. Read me!

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161687394-218a79b1-ce0d-49f2-8dfb-53600bdbed33.png">
</p>

### 2. What is the directory path that would we expect logs to be stored in?

### Answer: /var/log

### 3. What root directory is similar to how RAM on a computer works?

### Answer: tmp

### 4. Name the home directory of the root user 

### Answer: /root

### 5. Now apply your learning and navigate through these directories on the deployed Linux machine.

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161687394-218a79b1-ce0d-49f2-8dfb-53600bdbed33.png">
</p>

--------------------------------------------------------------------------------------------
