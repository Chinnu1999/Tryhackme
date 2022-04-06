![image](https://user-images.githubusercontent.com/94435318/161897073-d4156a5b-bf4b-4240-8265-05fab54f6b6f.png)

# 🟥 Task-7 Maintianing Yout System: Package Management

## Introducing Packages & Software Repos

When developers wish to submit software to the community, they will submit it to an  "apt" repository. If approved, their programs and tools will be released into the wild. Two of the most redeeming features of Linux shine to light here: User accessibility and the merit of open source tools.

When using thelscommand on a Ubuntu 20.04 Linux machine, these files serve as the gateway/registry. 

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161907756-e9f3bac1-00f8-4c7a-b786-dba8fc6665f6.png">
</p> 

Whilst Operating System vendors will maintain their own repositories, you can also add community repositories to your list! This allows you to extend the capabilities of your OS. Additional repositories can be added by using the add-apt-repositorycommand or by listing another provider! For example, some vendors will have a repository that is closer to their geographical location.

#3 Managing Your Repositories (Adding and Removing)

Normally we use the apt command to install software onto our Ubuntu system. The apt command is a part of the package management software also named apt. Apt contains a whole suite of tools that allows us to manage the packages and sources of our software, and to install or remove software at the same time.

Let's walk through adding and removing a repository using the add-apt-repository command we illustrated above. Whilst you can install software through the use of package installers such as dpkg, the benefits of apt means that whenever we update our system -- the repository that contains the pieces of software that we add also gets checked for updates. 

In this example, we're going to add the text editor Sublime Text to our Ubuntu machine as a repository as it is not a part of the default Ubuntu repositories. When adding software, the integrity of what we download is guaranteed by the use of what is called GPG (Gnu Privacy Guard) keys. These keys are essentially a safety check from the developers saying, "here's our software". If the keys do not match up to what your system trusts and what the developers used, then the software will not be downloaded.

So, to start, we need to add the GPG key for the developers of Sublime Text 3. (Note that TryHackMe instances do not have internet access and so we're not expecting you to add this to the machine that you deploy, as it would fail.)

1. Let's download the GPG key and use apt-key to trust it:  

*wget -qO - https://download.sublimetext.com/sublimehq-pub.gpg | sudo apt-key add -

2. Now that we have added this key to our trusted list, we can now add Sublime Text 3's repository to our apt sources list. A good practice is to have a separate file for every different community/3rd party repository that we add.

2.1. Let's create a file named sublime-text.list in /etc/apt/sources.list.d and enter the repository information like so:

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161907976-3b602294-f5f0-44b0-93e5-9c8d03d0cf33.png">
</p>  

2.2. And now use Nano or a text editor of your choice to add & save the Sublime Text 3 repository into this newly created file:

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161908084-9890ca70-00c7-4c16-b888-3a44de133757.png">
</p>  


2.3. After we have added this entry, we need to update apt to recognise this new entry -- this is done using the apt update command

2.4. Once successfully updated, we can now proceed to install the software that we have trusted and added to apt using apt install sublime-text

Removing packages is as easy as reversing. This process is done by using the add-apt-repository --remove ppa:PPA_Name/ppa command or by manually deleting the file that we previously fulfilled. Once removed, we can just use apt remove [software-name-here] i.e. apt remove sublime-text

--------------------------------------------------------------------------------------------

Answer the questions below------------------------------------------------------------------
--

### Since TryHackMe instances do not have an internet connection...this task only requires you to read through the material.

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161687394-218a79b1-ce0d-49f2-8dfb-53600bdbed33.png">
</p>

----------------------------------------------------------------------------------------------
