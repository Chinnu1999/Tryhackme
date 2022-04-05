![image](https://user-images.githubusercontent.com/94435318/161464318-2f53b4ec-ce25-4f2f-ad52-470231458957.png)

# 🟥 Task-3 Inntroduction to Flags and Switches

A majority of commands allow for arguments to be provided. These arguments are identified by a hyphen and a certain keyword known as flags or switches.

We'll later discuss how we can identify what commands allow for arguments to be provided and understanding what these do exactly.

When using a command, unless otherwise specified, it will perform its default behaviour. For example, ls lists the contents of the working directory. However, hidden files are not shown. We can use flags and switches to extend the behaviour of commands.

Using our ls example, ls informs us that there is only one folder named "folder1" as highlighted in the screenshot below. Note that the contents in the screenshots below are only examples.

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161678842-01f4f7a5-11d6-46a4-991e-43ea1d4f01c8.png">
</p>

However, after using the -a argument (short for --all), we now suddenly have an output with a few more files and folders such as ".hiddenfolder". Files and folders with "." are hidden files.

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161678943-88653109-ca1d-472c-8976-2930171a4c64.png">
</p>  

Commands that accept these will also have a--help option. This option will list the possible options that the command accepts, provide a brief description and example of how to use it.

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161679036-ae760b4f-067d-4e30-a751-9d98a27542cb.png">
</p>

This option is, in fact, a formatted output of what is called the man page (short for manual), which contains documentation for Linux commands and applications.

## The Man(ual) Page

The manual pages are a great source of information for both system commands and applications available on both a Linux machine, which is accessible on the machine itself and online.

To access this documentation, we can use the mancommand and then provide the command we want to read the documentation for. Using our ls example, we would use man ls to view the manual pages for ls like so:

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161679133-80b7c369-c4f0-44f1-9eeb-88f381355abe.png">
</p>

----------------------------------------------------------------------------------------------

Answer the questions below--------------------------------------
--

### 1. Explore the manual page of the ls command

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161679389-84396f1c-ea31-4060-a0f6-a5e1d4a92030.png">
</p>

### 2. What directional arrow key would we use to navigate down the manual page?

### Answer: down

### 3. What flag would we use to display the output in a "human-readable" way?

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161680136-7da2a918-c5c0-4dc2-93c8-eca63ea74ed1.png">
</p>

### Answer: -h
(-h is used to display the output in "human readable" way.         
            
--------------------------------------------------------------------------------------------
