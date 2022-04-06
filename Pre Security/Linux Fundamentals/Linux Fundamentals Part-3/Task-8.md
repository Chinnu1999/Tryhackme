![image](https://user-images.githubusercontent.com/94435318/161897073-d4156a5b-bf4b-4240-8265-05fab54f6b6f.png)

# 🟥 Task-8 Maintaining Your System: Logs

We briefly touched upon log files and where they can be found in Linux Fundamentals Part 1. However, let's quickly recap. Located in the /var/log directory, these files and folders contain logging information for applications and services running on your system. The Operating System  (OS) has become pretty good at automatically managing these logs in a process that is known as "rotating".

I have highlighted some logs from three services running on a Ubuntu machine:

    -> An Apache2 web server
    -> Logs for the fail2ban service, which is used to monitor attempted brute forces, for example
    -> The UFW service which is used as a firewall
    
<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161908565-15bac313-899d-43a8-b24a-9a3bed92e605.png">
</p>
    
These services and logs are a great way in monitoring the health of your system and protecting it. Not only that, but the logs for services such as a web server contain information about every single request - allowing developers or administrators to diagnose performance issues or investigate an intruder's activity. For example, the two types of log files below that are of interest:

    -> access log
    -> error log   
    
<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161908655-3e8c541a-d6fc-40d4-b2f2-277a2b7a5604.png">
</p>

There are, of course, logs that store information about how the OS is running itself and actions that are performed by users, such as authentication attempts.

--------------------------------------------------------------------------------------------------

Answer the questions below---------------------------------------------------------------
-- 

### 1. Look for the apache2 logs on the deployable Linux machine

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161687394-218a79b1-ce0d-49f2-8dfb-53600bdbed33.png">
</p>


### 2. What is the IP address of the user who visited the site?

- ANswer: 10.9.232.111

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161909403-8ab006ab-d8a4-45ee-8270-e7007a291ced.png">
</p>

### 3. What file did they access?

- Answer: catsanddogs.jpg
<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161910173-696f0487-06a3-4e68-b173-c4d5165093b6.png">
</p>    

  
------------------------------------------------------------------------------------------------
