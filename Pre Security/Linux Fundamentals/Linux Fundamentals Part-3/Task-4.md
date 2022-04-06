![image](https://user-images.githubusercontent.com/94435318/161897073-d4156a5b-bf4b-4240-8265-05fab54f6b6f.png)



# 🟥 Task-4 General/USeful Utilities

## Downloading Files

A pretty fundamental feature of computing is the ability to transfer files. For example, you may want to download a program, a script, or even a picture. Thankfully for us, there are multiple ways in which we can retrieve these files.

We're going to cover the use of wget.  This command allows us to download files from the web via HTTP -- as if you were accessing the file in your browser. We simply need to provide the address of the resource that we wish to download. For example, if I wanted to download a file named "myfile.txt" onto my machine, assuming I knew the web address it -- it would look something like this:

*wget https://assets.tryhackme.com/additional/linux-fundamentals/part3/myfile.txt

## Transferring Files From Your Host - SCP (SSH)

Secure copy, or SCP, is just that -- a means of securely copying files. Unlike the regular cp command, this command allows you to transfer files between two computers using the SSH protocol to provide both authentication and encryption.

Working on a model of SOURCE and DESTINATION, SCP allows you to:

    -> Copy files & directories from your current system to a remote system
    -> Copy files & directories from a remote system to your current system

Provided that we know usernames and passwords for a user on your current system and a user on the remote system. For example, let's copy an example file from our machine to a remote machine, which I have neatly laid out in the table below:

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161901457-53321f64-7a51-4791-bf01-70c3a9205abe.png">
</p>  

With this information, let's craft our scp command (remembering that the format of SCP is just SOURCE and DESTINATION)

*scp important.txt ubuntu@192.168.1.30:/home/ubuntu/transferred.txt

And now let's reverse this and layout the syntax for using scpto copy a file from a remote computer that we're not logged into 

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161901552-daa9e61a-43a3-4245-9b13-5096e6f5ed7f.png">
</p>

The command will now look like the following: scp ubuntu@192.168.1.30:/home/ubuntu/documents.txt notes.txt 

## Serving Files From Your Host - WEB

Ubuntu machines come pre-packaged with python3. Python helpfully provides a lightweight and easy-to-use module called "HTTPServer". This module turns your computer into a quick and easy web server that you can use to serve your own files, where they can then be downloaded by another computing using commands such as curland wget. 

Python3's "HTTPServer" will serve the files in the directory that you run the command, but this can be changed by providing options that can be found in the manual pages. Simply, all we need to do is run python3 -m  http.server to start the module! In the screenshot below, we are serving from a directory called "webserver", which has a single named "file".

<p align="center">
  <img src="![image](https://user-images.githubusercontent.com/94435318/161901778-87236d7b-1440-49f6-9446-f586fa2e7b4a.png">
</p>  

Now, let's use wgetto download the file using the computer's IP address and the name of the file. One flaw with this module is that you have no way of indexing, so you must know the exact name and location of the file that you wish to use. This is why I prefer to use Updog. What's Updog? A more advanced yet lightweight webserver. But for now, let's stick to using Python's "HTTP Server".

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161901858-8cde6095-a979-429b-80fd-4c414ac6633f.png">
</p>  

In the screenshot above, we can see that wget has successfully downloaded the file named "file" to our machine. This request is logged by SimpleHTTPServer much as any web server would, which I have captured in the screenshot below.

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161901922-effc4e89-44b6-464c-a048-c0933a7bcf5c.png">
</p>

-------------------

Answer the questions below--------------------------------------------------------------
--

### 1. Ensure you are connected to the deployed instance (10.10.214.32)

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161687394-218a79b1-ce0d-49f2-8dfb-53600bdbed33.png">
</p>

### 2. Now, use Python 3's "HTTPServer" module to start a web server in the home directory of the "tryhackme" user on the deployed instance.

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161687394-218a79b1-ce0d-49f2-8dfb-53600bdbed33.png">
</p>

## Download the file http://10.10.214.32:8000/.flag.txt onto the TryHackMe AttackBox

### 3. What are the contents?

- Answer: THM{WGET_WEBSERVER}
  
<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161902613-ac516d57-68f0-4768-a464-618d14b6751c.png">
</p>

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161902777-67733bfb-7fc5-43b5-830e-0d30239b30d8.png">
</p>

## Create and download files to further apply your learning -- see how you can read the documentation on Python3's "HTTPServer" module. 

### 4. Use Ctrl + C to stop the Python3 HTTPServer module once you are finished.

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161687394-218a79b1-ce0d-49f2-8dfb-53600bdbed33.png">
</p>

--------------------------------------------------------------------------------









