![image](https://user-images.githubusercontent.com/94435318/154879611-2e4d82fa-c711-4259-ab3b-470369dbc333.png)

Task-1 Connecting to our network
---
Get Connected﻿

To connect to our network, you need to download the OpenVPN GUI open-source application and import your VPN configuration file.

On TryHackMe you can deploy virtual machines that you can use to hack into and learn from. However, to access these machines you need to be connected to our network. You do this through using a VPN (similar to how you would connect to a work or school computer from home).

Firstly, go to the access page and download your VPN configuration file. Then read the task that is suited for your computer.

Answer:

Download your configuration file from the access page.

![image](https://user-images.githubusercontent.com/94435318/154877279-1df51289-0f8d-4e8f-978f-a8e5f928fb36.png)

-----------------------------------------Here I am using Linux--------------------------------------

Task-4 Connecting with Linux
---
![image](https://user-images.githubusercontent.com/94435318/154878131-212afa19-6939-482e-8a84-fdebd332f1a7.png)

1. Download OpenVPN by running the following command in your terminal: sudo apt install openvpn

2. Locate the full path to your VPN configuration file (download from the access page), normally in your Downloads folder.

3. Use your OpenVPN file with the following command: sudo openvpn /path-to-file/file-name.ovpn

And that's it! You should be successfully connected.

Answer:
Connect to our network on Linux using your OpenVPN configuration file.

![image](https://user-images.githubusercontent.com/94435318/154878243-2b7e6b8a-67d2-4da6-8565-7afdf709f5fe.png)

Task-5 Using Tryhackme without a VPN
---

If you are unable to connect to our network through the VPN, you can deploy a Kali Linux machine and control it in your browser. You can then access all TryHackMe machines through that machine. Free users can deploy the machine for 1 hour a day, subscribers have unlimited access.

Follow the steps to deploy your own machine in your browser:

    1.Subscribe to TryHackMe
    2.Go to the My Machine page
    3.Deploy a web-based machine of your choice!

A in-browser window will then appear, wait for your machine to load and you will be able to access machines through the Kali Linux machine without being connected to a VPN. If you're using the Kali Linux machine, start the machine on the "My Machine" page, and paste the machines and IP into the Kali Linux's machines web browser. 

Task-6 Check you're connected

You can check if you're connected to our network by a green tick next to connected on the Network Information table on the access page. 

Now verify that you're connected by deploying a machine and accessing its website. Deploy the machine on this task (it will take a few minutes to boot). Go to http://MACHINE_IP - can you see a website?

Answer:

Try to open the given ip in browser.

![image](https://user-images.githubusercontent.com/94435318/154878595-fec0caa2-4f73-46f7-9115-9f036cd8fb97.png)

Answer:

What is the flag displayed on the deployed machine's website?

![image](https://user-images.githubusercontent.com/94435318/154878667-09bd6c30-16ee-4e24-9b63-abb12a8fc2d5.png)


Completed:
---
![image](https://user-images.githubusercontent.com/94435318/154878887-553fd4b5-2615-4760-9299-ec6e3a33a2d3.png)

![image](https://user-images.githubusercontent.com/94435318/154879697-7a203414-bb62-459f-b7db-b0cd63a0e46f.png)
