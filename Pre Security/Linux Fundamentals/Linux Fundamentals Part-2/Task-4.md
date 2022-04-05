![image](https://user-images.githubusercontent.com/94435318/161464318-2f53b4ec-ce25-4f2f-ad52-470231458957.png)

# 🟥 Task-4 Filesystem Interaction Continued

We covered some of the most fundamental commands when interacting with the filesystem on the Linux machine. For example, we covered how to list and find the contents of folders using ls and find and navigating the filesystem using cd. 

In this task, we're going to learn some more commands for interacting with the filesystem to allow us to:

    -> create files and folders
    -> move files and folders
    -> delete files and folders

More specifically, the following commands:

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161680507-ea6c22e2-f91f-4904-b601-409342a6af57.png">
</p>

*rotip: Similarly to using cat, we can provide full file paths, i.e. directory1/directory2/note for all of these commands

## Creating Files and Folders (touch, mkdir)

Creating files and folders on Linux is a simple process. First, we'll cover creating a file. The touch command takes exactly one argument -- the name we want to give the file we create. For example, we can create the file "note" by using touch note. It's worth noting that touch simply creates a blank file. You would need to use commands like echo or text editors such as nano to add content to the blank file.

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161680737-5dfd7fda-56b0-4eac-be48-8068b0828a5e.png">
</p>

This is a similar process for making a folder, which just involves using the mkdir command and again providing the name that we want to assign to the directory. For example, creating the directory "mydirectory" using mkdir mydirectory.

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161680799-587ac790-0102-4bfb-b560-40ba0dde2219.png">
</p>

## Removing Files and Folders (rm)

rm is extraordinary out of the commands that we've covered so far. You can simply remove files by using rm. However, you need to provide the -R switch alongside the name of the directory you wish to remove.

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161680901-d8bd1d20-0c7d-4b5a-91ca-4915b898c698.png">
</p>

## Copying and Moving Files and Folders (cp, mv)

Copying and moving files is an important functionality on a Linux machine. Starting with cp, this command takes two arguments:

1. the name of the existing file

2. the name we wish to assign to the new file when copying

cp copies the entire contents of the existing file into the new file. In the screenshot below, we are copying "note" to "note2".

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161681040-2d4a6588-f857-47ef-9d21-c9316747c03f.png">
</p>

Moving a file takes two arguments, just like the cp command. However, rather than copying and/or creating a new file, mv will merge or modify the second file that we provide as an argument. Not only can you use mv to move a file to a new folder, but you can also use mvto rename a file or folder. For example, in the screenshot below, we are renaming the file "note2" to be named "note3". "note3" will now have the contents of "note2". 
<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161681132-35690e8f-25b4-4121-b024-c18e3cbba8ec.png">
</p>

## Determiing File Type

What is often misleading and often catches people out is making presumptions from files as to what their purpose or contents may be. Files usually have what's known as an extension to make this easier. For example, text files usually have an extension of ".txt". But this is not necessary.

So far, the files we have used in our examples haven't had an extension. Without knowing the context of why the file is there -- we don't really know its purpose. Enter the file command. This command takes one argument. For example, we'll use file to confirm whether or not the "note" file in our examples is indeed a text file, like so file note.

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161681272-140bfc14-b080-45f8-bb56-65b92f7eea07.png">
</p>

------------------------------------------------------------------------------------------

Answer the questions below-------------------------------------------
--

### 1. How would you create the file named "newnote"?

### Answer: touch newnote

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161681522-dab8cf78-d73f-4df5-8afc-0d83fe8afbee.png">
</p>

### Answer: touch newnote

### 2. On the deployable machine, what is the file type of "unknown1" in "tryhackme's" home directory?

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161683466-d73ae5de-d08b-4e0c-a151-d8013bbdf1e0.png">
</p>

### Answer: ASCII text

### 3. How would we move the file "myfile" to the directory "myfolder" 

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161683552-c7bd6a81-092a-4f94-a4a3-73b57068ed23.png">
</p>

### Answer: mv myfile myfolder

### 4. What are the contents of this file?

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161683640-a4a81b56-9b3d-4751-8b55-560c34081b67.png">
</p>

### Answer: THM{FILESYSTEM}

### 5. Continue to apply your knowledge and practice the commands from this task.

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161685231-cbfdecff-bd0b-4f66-a65f-ccfdbba6147b.png">
</p>

--------------------------------------------------------------------------------------------------
