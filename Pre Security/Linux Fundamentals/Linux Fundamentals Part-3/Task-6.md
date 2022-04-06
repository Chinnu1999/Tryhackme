![image](https://user-images.githubusercontent.com/94435318/161897073-d4156a5b-bf4b-4240-8265-05fab54f6b6f.png)

# 🟥 Task-6 Maintaining Your System: Automation

Users may want to schedule a certain action or task to take place after the system has booted. Take, for example, running commands, backing up files, or launching your favourite programs on, such as Spotify or Google Chrome.

We're going to be talking about the cron process, but more specifically, how we can interact with it via the use of crontabs . Crontab is one of the processes that is started during boot, which is responsible for facilitating and managing cron jobs.

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161906097-74738c8c-72f1-4d6b-bfbf-148956913466.png">
</p>
   
A crontab is simply a special file with formatting that is recognised by the cron process to execute each line step-by-step. Crontabs require 6 specific values:

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161906183-53e429b4-b53c-466c-852c-b9411ee44778.png">
</p>

Let's use the example of backing up files. You may wish to backup "cmnatic"'s  "Documents" every 12 hours. We would use the following formatting: 

0 *12 * * * cp -R /home/cmnatic/Documents /var/backups/

An interesting feature of crontabs is that these also support the wildcard or asterisk (*). If we do not wish to provide a value for that specific field, i.e. we don't care what month, day, or year it is executed -- only that it is executed every 12 hours, we simply just place an asterisk.

This can be confusing to begin with, which is why there are some great resources such as the online "Crontab Generator" that allows you to use a friendly application to generate your formatting for you! As well as the site "Cron Guru"!

Crontabs can be edited by using crontab -e, where you can select an editor (such as Nano) to edit your crontab.

<p align="center">
  <img src="![image](https://user-images.githubusercontent.com/94435318/161906285-fb590c15-7335-4786-a4f7-f104f2a1651e.png">
</p>

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161906345-69f4cf40-5938-427a-a51f-e0d06a25d50a.png">
</p>

-------------------------------------------------------------------------------------------

Answer the questions below-----------------------------------------------------------------
--

### 1. Ensure you are connected to the deployed instance and look at the running crontabs.

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161687394-218a79b1-ce0d-49f2-8dfb-53600bdbed33.png">
</p>

### 2. When will the crontab on the deployed instance (10.10.214.32) run?

- ANswer: reboot

----------------------------------------------------------------------------------------------
