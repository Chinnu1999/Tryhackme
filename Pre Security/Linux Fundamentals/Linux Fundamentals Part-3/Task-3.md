![image](https://user-images.githubusercontent.com/94435318/161897073-d4156a5b-bf4b-4240-8265-05fab54f6b6f.png)

# 🟥 Task-3 Terminal Text Editors

Throughout the series so far, we have only stored text in files using a combination of the echo command and the pipe operators (> and >>). This isn't an efficient way to handle data when you're working with files with multiple lines and the sorts!

## Introducing terminal text editors

There are a few options that you can use, all with a variety of friendliness and utility. This task is going to introduce you to nano but also show you an alternative named VIM (which TryHackMe has a room dedicated to!)

## Nano

It is easy to get started with Nano! To create or edit a file using nano, we simply use nano filename -- replacing "filename" with the name of the file you wish to edit.

<p aalign="center">
  <img src="https://user-images.githubusercontent.com/94435318/161898148-de070f98-cd41-4fdc-8341-0be35a0b638a.png">
</p>

Once we press enter to execute the command, nano will launch! Where we can just begin to start entering or modifying our text. You can navigate each line using the "up" and "down" arrow keys or start a new line using the "Enter" key on your keyboard.

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161898219-bf30f0d5-f445-4242-96e9-d85010c1b8f1.png">
</p>

Nano has a few features that are easy to remember & covers the most general things you would want out of a text editor, including:

    -> Searching for text
    -> Copying and Pasting
    -> Jumping to a line number
    -> Finding out what line number you are on

You can use these features of nano by pressing the "Ctrl" key (which is represented as an ^ on Linux)  and a corresponding letter. For example, to exit, we would want to press "Ctrl" and "X" to exit Nano.

## VIM

VIM is a much more advanced text editor. Whilst you're not expected to know all advanced features, it's helpful to mention it for powering up your Linux skills.

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161898368-ec60fa08-749c-45fd-b5a5-088019e0ba96.png">
</p>

Some of VIM's benefits, albeit taking a much longer time to become familiar with, includes:

    -> Customisable - you can modify the keyboard shortcuts to be of your choosing
    -> Syntax Highlighting - this is useful if you are writing or maintaining code, making it a popular choice for software developers
    -> VIM works on all terminals where nano may not be installed
    -> There are a lot of resources such as cheatsheets, tutorials, and the sorts available to you use.

TryHackMe has a room showcasing VIM if you wish to learn more about this editor!

---------------------------------------------------------------------------------------------

Answer the questions below---------------------------------------
--

### 1. Create a file using Nano

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161687394-218a79b1-ce0d-49f2-8dfb-53600bdbed33.png">
</p>

### 2. Edit "task3" located in "tryhackme"'s home directory using Nano. What is the flag?

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161901131-05e3b568-61bc-4b45-86d4-437893ef2352.png">
</p>

- Answer: THM{TEXT_EDITORS}

-----------------------------------------------------------------------------------------------
