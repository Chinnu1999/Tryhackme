![image](https://user-images.githubusercontent.com/94435318/162138207-3af8650f-0685-4602-b1c5-785412c5225c.png)

# 🟥 Task-9 Volume Shadow Copy Service

Per Microsoft, the Volume Shadow Copy Service (VSS) coordinates the required actions to create a consistent shadow copy (also known as a snapshot or a point-in-time copy) of the data that is to be backed up. 

Volume Shadow Copies are stored on the System Volume Information folder on each drive that has protection enabled.

If VSS is enabled (System Protection turned on), you can perform the following tasks from within advanced system settings. 

- Create a restore point
- Perform system restore
- Configure restore settings
- Delete restore points

From a security perspective, malware writers know of this Windows feature and write code in their malware to look for these files and delete them. Doing so makes it impossible to recover from a ransomware attack unless you have an offline/off-site backup.

If you wish to configure Shadow Copies within the attached VM, see below.

![vss1](https://user-images.githubusercontent.com/94435318/162146606-d6afe45e-f265-47fd-a341-1518693dc6ef.png)

![vss2](https://user-images.githubusercontent.com/94435318/162146636-980c6dce-c32f-4c87-b71b-9e83cb8aa7f9.png)

Bonus: If you wish to interact hands-on with VSS, I suggest exploring Day 23 of Advent of Cyber 2.

------------------------------------------------------------------------------------------------

Answer the questions below-----------------------------------------------------------
--

### What is VSS?

- Answer: Volume Shadow Copy Service 

-----------------------------------------------------------------------------------------------
