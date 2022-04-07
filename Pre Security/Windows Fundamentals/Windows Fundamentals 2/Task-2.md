![image](https://user-images.githubusercontent.com/94435318/162122757-c0dfdb99-8f42-4044-95c1-4bd8e1775fa2.png)

# 🟥 Task-2 System Configuration

The System Configuration utility (MSConfig) is for advanced troubleshooting, and its main purpose is to help diagnose startup issues. 

Reference the following document here for more information on the System Configuration utility. 

There are several methods to launch System Configuration. One method is from the Start Menu.

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/162123353-94bcb240-2b03-43c0-bd8c-094a5a6070d6.png">
</p>  

*Note: You need local administrator rights to open this utility.*

The utility has five tabs across the top. Below are the names for each tab. We will briefly cover each tab in this task. 

- General
- Boot
- Services
- Startup
- Tools

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/162123531-6e5f2b05-7be9-4a77-9ea9-264d5589e76a.png">
</p>

In the General tab, we can select what devices and services for Windows to load upon boot. The options are: Normal, Diagnostic, or Selective. 

In the Boot tab, we can define various boot options for the Operating System. 

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/162123652-535edd1c-69c9-4640-b874-aa29e3168d79.png">
</p>  

The Services tab lists all services configured for the system regardless of their state (running or stopped). A service is a special type of application that runs in the background.  

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/162123760-78917dee-edce-494f-a95e-7882006966ce.png">
</p>  

In the Startup tab, you won't see anything interesting in the attached VM.  Below is a screenshot of the Startup tab for MSConfig from my local machine. 

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/162123898-1029614e-1794-449a-a29f-851bddc60872.png">
</p>

As you can see, Microsoft advises using Task Manager (taskmgr) to manage (enable/disable) startup items. The System Configuration utility is NOT a startup management program. 

Note: If you open Task Manager for the attached VM, you will notice that Task Manager doesn't show a Startup tab. 

There is a list of various utilities (tools) in the Tools tab that we can run to configure the operating system further. There is a brief description of each tool to provide some insight into what the tool is for. 

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/162123962-7d1f2af3-7f51-46b5-b2f8-bdd64d65de91.png">
</p>

Notice the Selected command section. The information in this textbox will change per tool.

To run a tool, we can use the command to launch the tool via the run prompt, command prompt, or by clicking the Launch button. 

------------------------------------------------------------------------------------------

Answer the questions below------------------------------------------------------------
--

### 1. What is the name of the service that lists Systems Internals as the manufacturer?

- Answer: PsShutdown

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/162125324-18de7477-85c3-4ffe-97af-e4e121dd6c60.png">
</p>

### 2. Whom is the Windows license registered to?

- Answer: windows user

### 3. What is the command for Windows Troubleshooting?

- Answer: C:\Windows\System32\control.exe /name Micrrosoft.Troubleshooting

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/162125832-fd51f4a8-0f42-4809-b778-84520eb42d74.png">
</p>  

### 4. What command will open the Control Panel? (The answer is  the name of .exe, not the full path)

- Answer: control.exe

--------------------------------------------------------------------------------------------------
