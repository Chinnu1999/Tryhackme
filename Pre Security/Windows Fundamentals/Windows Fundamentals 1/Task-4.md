![image](https://user-images.githubusercontent.com/94435318/161913340-9792786d-7221-486a-93de-a3e203761565.png)

# 🟥 Task-4 The File System

The file system used in modern versions of Windows is the New Technology File System or simply NTFS.

Before NTFS, there was FAT16/FAT32 (File Allocation Table) and HPFS (High Performance File System). 

You still see FAT partitions in use today. For example, you typically see FAT partitions in USB devices, MicroSD cards, etc. but traditionally not on personal Windows computers/laptops or Windows servers.

NTFS is known as a journaling file system. In case of a failure, the file system can automatically repair the folders/files on disk using information stored in a log file. This function is not possible with FAT.   

NTFS addresses many of the limitations of the previous file systems; such as: 

- Supports files larger than 4GB
- Set specific permissions on folders and files
- Folder and file compression
- Encryption (Encryption File System or EFS)

If you're running Windows, what is the file system your Windows installation is using? You can check the Properties (right-click) of the drive your operating system is installed on, typically the C drive (C:\).

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161931210-69d1b8ec-7a96-4db3-88c8-4d8b1661f945.png">
</p>

You can read Microsoft's official documentation on FAT, HPFS, and NTFS here. 

Let's speak briefly on some features that are specific to NTFS. 

On NTFS volumes, you can set permissions that grant or deny access to files and folders.

The permissions are:

- Full control
- Modify
- Read & Execute
- List folder contents
- Read
- Write

The below image lists the meaning of each permission on how it applies to a file and a folder. (credit Microsoft)

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161931581-d62afb76-07e9-4913-ac9a-753e96ddc2cb.png">
</p>            

How can you view the permissions for a file or folder?

- Right-click the file or folder you want to check for permissions.
- From the context menu, select Properties.
- Within Properties, click on the Security tab.
- In the Group or user names list, select the user, computer, or group whose permissions you want to view.

In the below image, you can see the permissions for the Users group for the Windows folder. 

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161931822-87b42d6c-83b7-43ce-9973-ee4936ae0458.png">
</p>

Refer to the Microsoft documentation to get a better understanding of the NTFS permissions for Special Permissions.

Another feature of NTFS is Alternate Data Streams (ADS).

### Alternate Data Streams (ADS) is a file attribute specific to Windows NTFS (New Technology File System).

Every file has at least one data stream ($DATA), and ADS allows files to contain more than one stream of data. Natively Window Explorer doesn't display ADS to the user. There are 3rd party executables that can be used to view this data, but Powershell gives you the ability to view ADS for files.

From a security perspective, malware writers have used ADS to hide data.

Not all its uses are malicious. For example, when you download a file from the Internet, there are identifiers written to ADS to identify that the file was downloaded from the Internet.

To learn more about ADS, refer to the following link from MalwareBytes here. 

### Bonus: If you wish to interact hands-on with ADS, I suggest exploring Day 21 of Advent of Cyber 2.

----------------------------------------------------------------------------------------------

Answer the questions below----------------------------------------------------------------
--

### What is the meaning of NTFS?

- Answer: New Technology File System

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161932289-a1ce4ffc-1440-4447-afba-9e1e4c1b4913.png">
</p>  

----------------------------------------------------------------------------------------------
