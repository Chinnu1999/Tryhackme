![image](https://user-images.githubusercontent.com/94435318/162122757-c0dfdb99-8f42-4044-95c1-4bd8e1775fa2.png)

# 🟥 Task-4 Computer Management

We're continuing with Tools that are available through the System Configuration panel.

The Computer Management (compmgmt) utility has three primary sections: System Tools, Storage, and Services and Applications.

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/162130678-dd684a62-792c-487b-981f-4cf3ec58ec88.png">
</p>

## System Tools

Let's start with Task Scheduler. Per Microsoft, with Task Scheduler, we can create and manage common tasks that our computer will carry out automatically at the times we specify.

A task can run an application, a script, etc., and tasks can be configured to run at any point. A task can run at log in or at log off. Tasks can also be configured to run on a specific schedule, for example, every five mins.

To create a basic task, click on Create Basic Task under Actions (right pane).

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/162130792-b109f684-e2db-47b0-9f80-7850f5697185.png">
</p>

Next is Event Viewer.

Event Viewer allows us to view events that have occurred on the computer. These records of events can be seen as an audit trail that can be used to understand the activity of the computer system. This information is often used to diagnose problems and investigate actions executed on the system. 

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/162130856-0038053a-ef7d-4040-ba10-deb4e956ae27.png">
</p>

Event Viewer has three panes.

1. The pane on the left provides a hierarchical tree listing of the event log providers. (as shown in the image above)
2. The pane in the middle will display a general overview and summary of the events specific to a selected provider.
3. The pane on the right is the actions pane.

There are five types of events that can be logged. Below is a table from docs.microsoft.com providing a brief description for each.

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/162130967-0d3c178b-e0ea-42d3-ac36-361868f086c6.png">
</p>

The standard logs are visible under Windows Logs. Below is a table from docs.microsoft.com providing a brief description for each.

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/162131054-81577d25-ae15-4d20-9dec-239a28370e8b.png">
</p>

For more information about Event Viewer and Event Logs, please refer to the Windows Event Log room. 

Shared Folders is where you will see a complete list of shares and folders shared that others can connect to. 

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/162131149-bfeef0b6-da18-483d-8dbc-11a0889981c2.png">
</p>

In the above image, under Shares, are the default share of Windows, C$, and default remote administration shares created by Windows, such as ADMIN$. 

As with any object in Windows, you can right-click on a folder to view its properties, such as Permissions (who can access the shared resource). 

Under Sessions, you will see a list of users who are currently connected to the shares. In this VM, you won't see anybody connected to the shares.

All the folders and/or files that the connected users access will list under Open Files.

The Local Users and Groups section you should be familiar with from Windows Fundamentals 1 because it's lusrmgr.msc.

In Performance, you'll see a utility called Performance Monitor (perfmon).

Perfmon is used to view performance data either in real-time or from a log file. This utility is useful for troubleshooting performance issues on a computer system, whether local or remote. 

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/162131257-1c0d8d8c-469a-4024-9d8a-714dd12a6088.png">
</p>

Device Manager allows us to view and configure the hardware, such as disabling any hardware attached to the computer.

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/162131312-c5801db7-8f03-4be5-a543-e6336d65f843.png">
</p>

Storage  

Under Storage is Windows Server Backup and Disk Management. We'll only look at Disk Management in this room.

Note: Since the virtual machine is a Windows Server operating system, there are utilities available that you will typically not see in Windows 10.  

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/162131398-0b9ac1ca-f142-46a1-924e-ff0f8f96d86b.png">
</p>

Disk Management is a system utility in Windows that enables you to perform advanced storage tasks.  Some tasks are:

- Set up a new drive
- Extend a partition
- Shrink a partition
- Assign or change a drive letter (ex. E:) 

## Services and Applications

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/162131650-602ee8c2-5b40-43f2-9e12-25d8f9f140c4.png">
</p>

Recall from the previous task; a service is a special type of application that runs in the background. Here you can do more than enable and disable a service, such as view the Properties for the service. 

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/162131732-6cc4ea0e-bc1e-4402-abb2-3b49f74e15f3.png">
</p>

WMI Control configures and controls the Windows Management Instrumentation (WMI) service.

Per Wikipedia, "WMI allows scripting languages (such as VBScript or Windows PowerShell) to manage Microsoft Windows personal computers and servers, both locally and remotely. Microsoft also provides a command-line interface to WMI called Windows Management Instrumentation Command-line (WMIC)."

*Note: The WMIC tool is deprecated in Windows 10, version 21H1. Windows PowerShell supersedes this tool for WMI.* 

---------------------------------------------------------------------------------------------

Answer the questions below---------------------------------------------------------
--

### 1. What is the command to open Computer Management? (The answer is the name of the .msc file, not the full path)

- Answer: compmgmt.msc

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/162127081-aba7baf7-83f5-45ea-9abe-b87fe10b493f.png">
</p>

### 2. At what time every day is the GoogleUpdateTaskMachineUA task configured to run?

- Answer: 6:15 AM

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/162126983-ed9238d5-f958-4be8-af13-726434f7c467.png">
</p>

### 3. What is the name of the hidden share?

- Answer: sh4r3dF0Ld3r

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/162127552-4685ec95-fad4-4225-88bc-5a9f6ba8aa9e.png">
</p>  

----------------------------------------------------------------------------------------------
