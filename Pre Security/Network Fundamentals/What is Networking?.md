# Learn the core concepts of how computers communicate with each other and types of network weaknesses.

![image](https://user-images.githubusercontent.com/94435318/161387118-9f11b723-3610-4863-98ca-e47d0d23ee34.png)

# 🟥 Task-1 What is Networking?

Networks are simply things connected. For example, your friendship circle: you are all connected because of similar interests, hobbies, skills and sorts.

Networks can be found in all walks of life:

A city's public transportation system
Infrastructure such as the national power grid for electricity
Meeting and greeting your neighbours
Postal systems for sending letters and parcels
But more specifically, in computing, networking is the same idea, just dispersed to technological devices. Take your phone as an example; the reason that you have it is to access things. We'll cover how these devices communicate with each other and the rules that follow.

In computing, a network can be formed by anywhere from 2 devices to billions. These devices include everything from your laptop and phone to security cameras, traffic lights and even farming!

Networks are integrated into our everyday life. Be it gathering data for the weather, delivering electricity to homes or even determining who has the right of way at a road. Because networks are so embedded in the modern-day, networking is an essential concept to grasp in cybersecurity.

Take the diagram below as an example, Alice, Bob and Jim have formed their network! We'll come onto this a bit later on.

![image](https://user-images.githubusercontent.com/94435318/161387181-3afad0bd-3801-4fc9-9716-6c612afb8801.png)

Networks come in all shapes and sizes, which is something that we will also come on to discuss throughout this module. 

## Answer the questions below

What is the key term for devices that are connected together?

![image](https://user-images.githubusercontent.com/94435318/161387460-20d5f54e-19ad-41bb-9c71-3adaf4b31f5a.png)

### Answer: Network

-----------------------------------------------------------------------------------------

# 🟥 Task-2 What is the Internet?

Now that we've learnt what a network is and how one is defined in computing (just devices connected), let's explore the Internet.

The Internet is one giant network that consists of many, many small networks within itself. Using our example from the previous task, let's now imagine that Alice made some new friends named Zayn and Toby that she wants to introduce to Bob and Jim. The problem is that Alice is the only person who speaks the same language as Zayn and Toby. So Alice will have to be the messenger!

![image](https://user-images.githubusercontent.com/94435318/161387562-035a83dd-5d47-4bc0-a768-ae1349877fcb.png)

Because Alice can speak both languages, they can communicate to one another through Alice — forming a new network.

The first iteration of the Internet was within the ARPANET project in the late 1960s. This project was funded by the United States Defence Department and was the first documented network in action. However, it wasn't until 1989 when the Internet as we know it was invented by Tim Berners-Lee by the creation of the World Wide Web (WWW). It wasn't until this point that the Internet wasn't used as a repository for storing and sharing information (like it is today).

Let's relate Alice's network of friends to computing devices. The Internet looks like a much larger version of this sort of diagram:

![image](https://user-images.githubusercontent.com/94435318/161387590-737503c7-9f35-4e75-b2fe-5b3b1dd0407a.png)

As previously stated, the Internet is made up of many small networks all joined together.  These small networks are called private networks, where networks connecting these small networks are called public networks -- or the Internet! So, to recap, a network can be one of two types:

A private network
A public network
Devices will use a set of labels to identify themselves on a network, which we will come onto in the task below.

Answer the questions below
--

Who invented the World Wide Web?

![image](https://user-images.githubusercontent.com/94435318/161387668-2e1f50a5-8513-404a-935b-35f71f9ba42b.png)

### Answer: Tim Berners-Lee

-----------------------------------------------------------------------------------------

# 🟥 Task-3 Identifying Devices on a Network

To communicate and maintain order, devices must be both identifying and identifiable on a network. What use is it if you don't know whom you're talking to at the end of the day?

Devices on a network are very similar to humans in the fact that we have two ways of being identified:

   * Our Name
   * Our Fingerprints
Now we can change our name through deed poll, but we can't, however, change our fingerprints. Every human has an individual set of fingerprints which means that even if they change their name, there is still an identity behind it. Devices have the same thing: two means of identification, with one being permeable. These are:

   * An IP Address
   * A Media Access Control (MAC) Address -- think of this as being similar to a serial number.

## IP Addresses

Briefly, an IP address (or Internet Protocol) address can be used as a way of identifying a host on a network for a period of time, where that IP address can then be associated with another device without the IP address changing. First, let's split up precisely what an IP address is in the diagram below:

![image](https://user-images.githubusercontent.com/94435318/161387815-3d22bc3f-68e2-4d92-8ed3-0f675584e58e.png)

An IP address is a set of numbers that are divided into four octets. The value of each octet will summarise to be the IP address of the device on the network. This number is calculated through a technique known as IP addressing & subnetting, but that is for another day. What's important to understand here is that IP addresses can change from device to device but cannot be active simultaneously more than once within the same network.

IP Addresses follow a set of standards known as protocols. These protocols are the backbone of networking and force many devices to communicate in the same language, which is something that we'll come onto another time. However, we should recall that devices can be on both a private and public network. Depending on where they are will determine what type of IP address they have: a public or private IP address.

A public address is used to identify the device on the Internet, whereas a private address is used to identify a device amongst other devices. Take the table & screenshot below as an example. Here we have two devices on a private network:

![image](https://user-images.githubusercontent.com/94435318/161387856-47155529-c34d-4c06-8a69-b7c749b2ee02.png)

These two devices will be able to use their private IP addresses to communicate with each other. However, any data sent to the Internet from either of these devices will be identified by the same public IP address. Public IP addresses are given by your Internet Service Provider (or ISP) at a monthly fee (your bill!)

![image](https://user-images.githubusercontent.com/94435318/161387875-f1679988-ea7b-419d-b1ea-db5b8674c4c4.png)


As more and more devices become connected, it is becoming increasingly harder to get a public address that isn't already in use. For example, Cisco, an industry giant in the world of networking, estimated that there would be approximately 50 billion devices connected on the Internet by the end of 2021. (Cisco., 2021). Enter IP address versions. So far, we have only discussed one version of the Internet Protocol addressing scheme known as IPv4, which uses a numbering system of 2^32 IP addresses (4.29 billion) -- so you can see why there is such a shortage!

IPv6 is a new iteration of the Internet Protocol addressing scheme to help tackle this issue. Although it is seemingly more daunting, it boasts a few benefits:

   * Supports up to 2^128 of IP addresses (340 trillion-plus), resolving the issues faced with IPv4
   * More efficient due to new methodologies
The screenshot below compares both an IPv6 and IPv4 address.

![image](https://user-images.githubusercontent.com/94435318/161387911-40155341-6c77-40c8-a2ef-fd378c99512b.png)

## MAC Addresses

Devices on a network will all have a physical network interface, which is a microchip board found on the device's motherboard. This network interface is assigned a unique address at the factory it was built at, called a MAC (Media Access Control ) address. The MAC address is a twelve-character hexadecimal number (a base sixteen numbering system used in computing to represent numbers) split into two's and separated by a colon. These colons are considered separators. For example, a4:c3:f0:85:ac:2d. The first six characters represent the company that made the network interface, and the last six is a unique number.

![image](https://user-images.githubusercontent.com/94435318/161387927-c8cb5e8b-8898-4379-8834-a96bae05850c.png)

However, an interesting thing with MAC addresses is that they can be faked or "spoofed" in a process known as spoofing. This spoofing occurs when a networked device pretends to identify as another using its MAC address. When this occurs, it can often break poorly implemented security designs that assume that devices talking on a network are trustworthy. Take the following scenario: A firewall is configured to allow any communication going to and from the MAC address of the administrator. If a device were to pretend or "spoof" this MAC address, the firewall would now think that it is receiving communication from the administrator when it isn't.

Places such as cafes, coffee shops, and hotels alike often use MAC address control when using their "Guest "or "Public" Wi-Fi. This configuration could offer better services, i.e. a faster connection for a price if you are willing to pay the fee per device.  The interactive lab attached to this task has been made to replicate this scenario!

## Practical

The interactive labs simulate a hotel Wi-Fi network where you have to pay for the service. You'll note that the router is not allowing Bob's packets ( blue) to the TryHackMe website and is placing them in the bin, but Alice's packets (green) are going through fine because she has paid for Wi-Fi. Try changing Bob's MAC address to the same as Alice's to see what happens.

Deploy the interactive lab and proceed to answer the following questions below.

Answer the questions below
--

What does the term "IP" stand for?

![image](https://user-images.githubusercontent.com/94435318/161387998-4b46ed3d-bb1e-47ec-b3cd-08eab0f6c3b3.png)

### Answer: Internet Protocol

What is each section of an IP address called?

![image](https://user-images.githubusercontent.com/94435318/161388188-193f2a6a-9fa7-4dec-bd0e-d2be4555a881.png)

### Answer: Octet

How many sections (in digits) does an IP address have? 

![image](https://user-images.githubusercontent.com/94435318/161388283-63caec4b-7bd2-4bfb-ae0c-032f7a2db426.png)

### Answer: 4

What does the term "MAC" stand for?

![image](https://user-images.githubusercontent.com/94435318/161388371-a015b4a7-9b03-4679-95e0-d21ab60c03cb.png)

### Answer: Media Access Control

Deploy the interactive lab using the "View Site" button and spoof your MAC address to access the site.  What is the flag?

![image](https://user-images.githubusercontent.com/94435318/161388425-84809f23-6c09-40e7-8470-0d62c479d19c.png)

![image](https://user-images.githubusercontent.com/94435318/161388717-13215f1a-17c3-4b5a-8683-7b176934ff1a.png)

## Sppof the alice id and enter it in bob then press request site

![image](https://user-images.githubusercontent.com/94435318/161388584-f36110e7-f6ba-4697-a50a-ac1a506688f8.png)

### Answer: THM{you_got_on_tryhackme}

-----------------------------------------------------------------------------------------------

# 🟥 Task-4 Ping(ICMP)

Ping is one of the most fundamental network tools available to us. Ping uses ICMP (Internet Control Message Protocol) packets to determine the performance of a connection between devices, for example, if the connection exists or is reliable.

The time taken for ICMP packets travelling between devices is measured by ping, such as in the screenshot below. This measuring is done using ICMP's echo packet and then ICMP's echo reply from the target device.

Pings can be performed against devices on a network, such as your home network or resources like websites. This tool can be easily used and comes installed on Operating Systems (OSs) such as Linux and Windows. The syntax to do a simple ping is ping IP address or website URL. Let's see this in action in the screenshot below.

![image](https://user-images.githubusercontent.com/94435318/161388821-f6b96f15-8a8d-4fba-8d49-5b977b096249.png)

Here we are pinging a device that has the private address of 192.168.1.254. Ping informs us that we have sent six ICMP packets, all of which were received with an average time of 5.3 seconds.

Now you are going to do the same thing to ping the address of "8.8.8.8" on the deployable website in this task. Pinging the correct address will reveal a flag to answer the following question below.

Answer the questions below
--

What protocol does ping use?

![image](https://user-images.githubusercontent.com/94435318/161388872-c13ab31e-1dca-418a-ba97-f15174cc5071.png)

### Answer: ICMP

What is the syntax to ping 10.10.10.10?

### Answer: ping 10.10.10.10

What flag do you get when you ping 8.8.8.8?

![image](https://user-images.githubusercontent.com/94435318/161389029-7c9f97aa-ce01-4260-9010-0a540b688f75.png)

### Answer: THM{I_Pinged_The_Server}

-----------------------------------------------------------------------------------------------

# 🟥 Task-5 Continue Your Learning: Intro to LAN

Continue your learning by joining the "Intro to LAN" room.

Answer the questions below
--

Join the "Intro to LAN" room.

### Answer: Click Completed

-----------------------------------------------------------------------------------------------
