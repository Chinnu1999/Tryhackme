![image](https://user-images.githubusercontent.com/94435318/161464318-2f53b4ec-ce25-4f2f-ad52-470231458957.png)

# 🟥 Task-2 Acccessing Your Linux Machine Using SSH (Deploy)

The in-browser functionality was used in Linux Fundamentals Part 1 to get you directly connected to your first ever Linux machine without any hassle.

In fact, the in-browser functionality uses the exact same protocol that we are going to be using today. This protocol is called Secure Shell or SSH for short and is the common means of connecting to and interacting with the command line of a remote Linux machine.

We will be deploying two machines in this room:

    -> Your Linux machine
    -> The TryHackMe AttackBox

## What is SSH & how Does it Work?

Secure Shell or SSH simply is a protocol between devices in an encrypted form. Using cryptography, any input we send in a human-readable format is encrypted for travelling over a network -- where it is then unencrypted once it reaches the remote machine, such as in the diagram below.

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161464921-ce1c05a0-a0ff-43ba-8284-fcbc10df2181.png">
</p>

You can learn about the various types of encryption on a TryHackMe room. But for now, we only need to understand that:

    -> SSH allows us to remotely execute commands on another device remotely.
    -> Any data sent between the devices is encrypted when it is sent over a network such as the Internet

## Deploying Your Linux Machine

Press the green "Start Machine" button on the top-right of this task and then scroll to the top of the page to see the deployment information like so:

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161465107-b06bdaf1-ae17-4578-8e39-2fcc95b10ad4.png">
</p>

The IP address displayed is the address of your Linux machine that you will be logging into using SSH. Take note of this for now.

## Deploying the TryHackMe AttackBox

Looking at the top of the page, press the "Start AttackBox" button to deploy the TryHackMe AttackBox that we will be interacting with. The TryHackMe AttackBox is a Ubuntu Linux machine that is hosted online in the cloud and can be interacted with via your browser. You will be using this to interact with the machine that you deploy in this task.

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161465230-6e031ec3-1032-4985-850d-cf2487c851a2.png">
</p>

## Using SSH to Login to Your Linux Machine

The syntax to use SSH is very simple. We only need to provide two things:

1. The IP address of the remote machine
2. Correct credentials to a valid account to login with on the remote machine

For this room, we will be logging in as "tryhackme", whose password is "tryhackme" without the quotation ("") marks. Let's use the IP address of the machine displayed in the card at the top of the room as the IP address and this user, to construct a command to log in to the remote machine using SSH. The command to do so is ssh and then the username of the account, @ the IP address of the machine.

But first, we need to open a terminal on the TryHackMe AttackBox. There is an icon placed on the desktop named "Terminal". And now, we can proceed to input commands.

For example: ssh tryhackme@10.10.67.120 . Replacing the IP address with the IP address for your Linux target machine. Once executed, we will then be asked to trust the host and then provide a password for the "tryhackme" account, which is also "tryhackme".

<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161465539-c08275ac-8e82-40f5-84c0-e2174331a396.png">
</p>

Now that we are connected, any commands that we execute will now execute on the remote machine -- not our own. Please note, when typing the password in when SSH'ing into the machine, the text is invisible - type the password out and press enter (even as no text will show as you type).

----------------------------------------------------------------------------------

Answer the questions below---------------------------------------
--

### I've logged into the Linux Fundamentals Part 2 machine using SSH!            
            
<p align="center">
  <img src="https://user-images.githubusercontent.com/94435318/161465487-02f1def5-7cf0-426e-8300-4e325488af2d.png">
</p>  
            
            
