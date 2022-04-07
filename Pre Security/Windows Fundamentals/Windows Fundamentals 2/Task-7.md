

![image](https://user-images.githubusercontent.com/94435318/162122757-c0dfdb99-8f42-4044-95c1-4bd8e1775fa2.png)

# 🟥 Task-7 Command Prompt

We're continuing with Tools that are available through the System Configuration panel.

The command prompt (cmd) can seem daunting at first, but it's really not that bad once you understand how to interact with it. 

In early operating systems, the command line was the sole way to interact with the operating system.

When the GUI (graphical user interface) was introduced, it allowed users to perform complex tasks with a few clicks of a button instead of entering commands in the command prompt. 

Even though the GUI is the primary way to interact with the operating system, a computer user can still interact via the command prompt. 

In this task, we'll only cover a few commands that a computer user can run in the command prompt to obtain information about the computer system.

Let's start with a few simple commands, such as hostname and whoami.

The command hostname will output the computer name.

![hostname](https://user-images.githubusercontent.com/94435318/162135214-65dc7403-48d7-4de8-9d28-6910139632f3.png)

The command whoami will output the name of the logged-in user.

![whoami](https://user-images.githubusercontent.com/94435318/162135254-e171086d-3eb6-46f5-8996-30330612ac52.png)

Next, let's look at some commands that are useful when troubleshooting.

A command used often is ipconfig. This command will show the network address settings for the computer.

![ipconfig](https://user-images.githubusercontent.com/94435318/162135290-c0a5dc50-ca7b-40e4-a3d3-6c7af83aed63.png)

Each command will have a help manual to explain the expected syntax to execute the command properly, along with any additional parameters that can be added to the command to expand its execution.

A  command to retrieve the help manual for a command is /?.

For example, to see the help manual for ipconfig, you can use the following command: ipconfig /?

![ipconfig-help](https://user-images.githubusercontent.com/94435318/162135443-0c0fb8d0-29f1-43c4-bd60-44d216f60426.png)

Note: To clear the command prompt screen, the command is cls. 

The next command is netstat. Per the help manual, this command will display protocol statistics and current TCP/IP network connections. 

![netstat](https://user-images.githubusercontent.com/94435318/162135461-703a17bf-af9b-4b6e-8c65-1a5f8e1f564d.png)

In the above image, the line within the red box shows us an example syntax for the command. 

The structure tells us the netstat command can be run alone or with parameters, such as -a,  -b,  -e, etc. 

When any of the parameters are appended to the root command, netstat in this case, the output changes. Play with a few to see for yourself. 

The net command is primarily used to manage network resources. This command supports sub-commands.

If you type net without a sub-command, the output will show the syntax for the root command showing a few of the sub-commands you can use.

![net](https://user-images.githubusercontent.com/94435318/162135492-5bb0da1b-6ac8-4f22-b631-d1c728cf425d.png)

For the net command, to display the help manual /? will not work. In this case, you need to use different syntax, which is net help.

![net-help](https://user-images.githubusercontent.com/94435318/162135526-df501fe3-0f01-4208-b06c-67b80461d635.png)

So, if you wish to see the help information for net user , the command is net help user. 

![net-help-user2](https://user-images.githubusercontent.com/94435318/162135546-2ccca885-2736-494d-9a8f-661af9584d75.png)

You can use the same command to view the help information for other useful net sub-commands, such as localgroup, use, share, and session. 

Refer to the following link to see a comprehensive list of commands you can execute in the command prompt here. 

--------------------------------------------------------------------------------------------

Answer the questions below-----------------------------------------------------------------
--

### 1. In System Configuration, what is the full command for Internet Protocol Configuration?

- Answer: C:\Windows\System32\cmd.exe /k %windir%\system32\ipconfig.exe

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/162128936-dbd8a21a-d43a-472e-9649-5b1781e67790.png">
 </p>
 
 ### 2. For the ipconfig command, how do you show detailed information?

- Answer: ipconfig /all

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/162129071-37dc709a-f340-4fd9-9b22-f1253df65e7d.png">
</p>  
  
-------------------------------------------------------------------------------------------------- 
