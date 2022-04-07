

![image](https://user-images.githubusercontent.com/94435318/162122757-c0dfdb99-8f42-4044-95c1-4bd8e1775fa2.png)

# 🟥 Task-5 System Information

We're continuing with Tools that are available through the System Configuration panel.

What is the System Information (msinfo32) tool?

Per Microsoft, "Windows includes a tool called Microsoft System Information (Msinfo32.exe).  This tool gathers information about your computer and displays a comprehensive view of your hardware, system components, and software environment, which you can use to diagnose computer issues."

The  information in System Summary is divided into three sections:

- Hardware Resources
- Components
- Software Environment

System Summary will display general technical specifications for the computer, such as processor brand and model.

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/162132705-c0a3b275-144a-4fd2-8dcd-784ec2968ae9.png">
</p>

The information displayed in Hardware Resources is not for the average computer user. If you want to learn more about this section, refer to the official Microsoft page.

<p align="left">
  <img src="https://user-images.githubusercontent.com/94435318/162132799-5d6586bc-be78-4c6c-bdf4-0f993a2f6eb4.png">
</p>

Under Components, you can see specific information about the hardware devices installed on the computer. Some sections don't show any information, but some sections do, such as Display and Input.

<p align="left">
  <img src="https://user-images.githubusercontent.com/94435318/162132894-c06431b1-f220-442d-85e1-d8ca82ed934f.png">
</p>  

In the Software Environment section, you can see information about software baked into the operating system and software you have installed. Other details are visible in this section as well, such as the Environment Variables and Network Connections. 

<p align="left">
  <img src="https://user-images.githubusercontent.com/94435318/162133050-1c01d6d7-6d5e-4fc5-b94e-c666eae10384.png">
</p>

Recall from the Windows Fundamentals 1 room (The Windows\System32 Folder task) where Environment Variables was briefly touched on. 

Per Microsoft, "Environment variables store information about the operating system environment. This information includes details such as the operating system path, the number of processors used by the operating system, and the location of temporary folders.

The environment variables store data that is used by the operating system and other programs. For example, the WINDIR environment variable contains the location of the Windows installation directory. Programs can query the value of this variable to determine where Windows operating system files are located".

Click on Environment Variables to see the assigned values for the virtual machine.

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/162133186-aa60c6ae-03bd-4752-9345-aa4f5ec897a6.png">
</p>

Another method to view environment variables is
*Control Panel > System and Security > System > Advanced system settings > Environment Variables OR Settings > System > About > system info > Advanced system settings > Environment Variables.*

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/162133404-90851f36-a905-4dc4-a184-727b91236453.png">
</p>

The detour is over. Let's redirect our attention back to msinfo32 and pick up where we left off.

Towards the very bottom of this utility, there is a search bar. Please give it a go. Select Components and search for IP address.

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/162133488-2f6be6f5-a3fe-437b-bd0e-bf00eac8a6ec.png">
</p>

--------------------------------------------------------------------------------------------

Answer the questions below----------------------------------------------------------------
--

### 1. What is the command to open System Information? (The answer is the name of the .exe file, not the full path) 

- Answer: msinfo32.exe

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/162127870-228456d0-2528-472d-957e-803c9a223cb1.png">
</p>

### 2. What is listed under System Name?

- Answer: THM-WINFUN2

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/162128126-01e3edb5-177f-4041-bd09-e7aae735fb5c.png">
</p>

### 3. Under Environment Variables, what is the value for ComSpec?

- Answer: %SystemRoot%\system32\cmd.exe

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/162128301-6dd9af93-690f-40be-941d-f66be4c14d94.png">
</p>  

------------------------------------------------------------------------------------------------
