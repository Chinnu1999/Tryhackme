![image](https://user-images.githubusercontent.com/94435318/161414660-878c3870-bbda-4395-8dba-0a61b6d50be9.png)

# 🟥 Task-1 Introducing LAN Topologies

## Local Area Network (LAN) Topologies

Over the years, there has been experimentation and implementation of various network designs.  In reference to networking, when we refer to the term "topology", we are actually referring to the design or look of the network at hand. Let's discuss the advantages and disadvantages of these topologies below.

## Star Topology

The main premise of a star topology is that devices are individually connected via a central networking device such as a switch or hub. This topology is the most commonly found today because of its reliability and scalability - despite the cost.

Any information sent to a device in this topology is sent via the central device to which it connects. Let's explore some of these advantages and disadvantages of this topology below:

Because more cabling & the purchase of dedicated networking equipment is required for this topology, it is more expensive than any of the other topologies. However, despite the added cost, this does provide some significant advantages. For example, this topology is much more scalable in nature, which means that it is very easy to add more devices as the demand for the network increases.

Unfortunately, the more the network scales, the more maintenance is required to keep the network functional. This increased dependence on maintenance can also make troubleshooting faults much harder. Furthermore, the star topology is still prone to failure - albeit reduced. For example, if the centralised hardware that connects devices fails, these devices will no longer be able to send or receive data. Thankfully, these centralised hardware devices are often robust.

![image](https://user-images.githubusercontent.com/94435318/161412076-9d0ced2d-34b0-4e03-b2e7-0475fa2b88b2.png)

## Bus Topology

This type of connection relies upon a single connection which is known as a backbone cable. This type of topology is similar to the leaf off of a tree in the sense that devices (leaves) stem from where the branches are on this cable.
Because all data destined for each device travels along the same cable, it is very quickly prone to becoming slow and bottlenecked if devices within the topology are simultaneously requesting data. This bottleneck also results in very difficult troubleshooting because it quickly becomes difficult to identify which device is experiencing issues with data all travelling along the same route.

However, with this said, bus topologies are one of the easier and more cost-efficient topologies to set up because of their expenses, such as cabling or dedicated networking equipment used to connect these devices.

Lastly, another disadvantage of the bus topology is that there is little redundancy in place in case of failures. This disadvantage is because there is a single point of failure along the backbone cable. If this cable were to break, devices can no longer receive or transmit data along the bus.

![image](https://user-images.githubusercontent.com/94435318/161412092-f6b8a689-3b97-48f1-ad42-ecab1eb02d99.png)

## Ring Topology

The ring topology (also known as token topology) boasts some similarities. Devices such as computers are connected directly to each other to form a loop, meaning that there is little cabling required and less dependence on dedicated hardware such as within a star topology. 

A ring topology works by sending data across the loop until it reaches the destined device, using other devices along the loop to forward the data. Interestingly, a device will only send received data from another device in this topology if it does not have any to send itself. If the device happens to have data to send, it will send its own data first before sending data from another device.

Because there is only one direction for data to travel across this topology, it is fairly easy to troubleshoot any faults that arise. However, this is a double-edged sword because it isn't an efficient way of data travelling across a network, as it may have to visit many multiple devices first before reaching the intended device.

Lastly, ring topologies are less prone to bottlenecks, such as within a bus topology, as large amounts of traffic are not travelling across the network at any one time. The design of this topology does, however, mean that a fault such as cut cable, or broken device will result in the entire networking breaking. 

![image](https://user-images.githubusercontent.com/94435318/161412136-ddd502ee-cd72-4bb2-87cf-c2504088dd35.png)

## What is a Switch?

Switches are dedicated devices within a network that are designed to aggregate multiple other devices such as computers, printers, or any other networking-capable device using ethernet. These various devices plug into a switch's port. Switches are usually found in larger networks such as businesses, schools, or similar-sized networks, where there are many devices to connect to the network. Switches can connect a large number of devices by having ports of 4, 8, 16, 24, 32, and 64 for devices to plug into.

Switches are much more efficient than their lesser counterpart (hubs/repeaters). Switches keep track of what device is connected to which port. This way, when they receive a packet, instead of repeating that packet to every port like a hub would do, it just sends it to the intended target, thus reducing network traffic.

![image](https://user-images.githubusercontent.com/94435318/161412152-580baf8c-d7bc-4e59-907f-8c431eb50137.png)

Both Switches and Routers can be connected to one another. The ability to do this increases the redundancy (the reliability) of a network by adding multiple paths for data to take. If one path goes down, another can be used. Whilst this may reduce the overall performance of a network because packets have to take longer to travel, there is no downtime -- a small price to pay considering the alternative.

## What is a Router?

It's a router's job to connect networks and pass data between them. It does this by using routing (hence the name router!).

Routing is the label given to the process of data travelling across networks. Routing involves creating a path between networks so that this data can be successfully delivered.

Routing is useful when devices are connected by many paths, such as in the example diagram below.

![image](https://user-images.githubusercontent.com/94435318/161412182-814abc8a-3e04-4f05-a7d7-b3e3e5cbbce2.png)

## Practical
Attached to this task is an interactive practical featuring the discussed LAN topologies. Learn about the various ways in which they are vulnerable to breaking. Break the LAN topologies to retrieve the flag.

----------------------------------------------------------------------------------------------

Answer the questions below
--

#### 1. What does LAN stand for?

![image](https://user-images.githubusercontent.com/94435318/161412260-2a96e801-06b0-45e7-8031-646508acfe22.png)

### Answer: Local Area Network


### 2. What is the verb given to the job that Routers perform?

![image](https://user-images.githubusercontent.com/94435318/161412369-8e36cc60-86b4-4dcd-a1fb-23b7c80e3e47.png)

### Answer: Routing


### 3. What device is used to centrally connect multiple devices on the local network and transmit data to the correct location?

![image](https://user-images.githubusercontent.com/94435318/161412468-8b9d2e31-f09e-485d-89e8-babe79eea6f9.png)

### Answer: Switch


### 4. What topology is cost-efficient to set up?

![image](https://user-images.githubusercontent.com/94435318/161412576-105e0d2b-7426-4e40-acca-506f56645c50.png)

### Answer: Bus Topology

### 5. What topology is expensive to set up and maintain?

![image](https://user-images.githubusercontent.com/94435318/161412667-919771c1-07c5-4f0c-adfa-347c59acd9cc.png)

### Answer: Star Topology

### 6. Complete the interactive lab attached to this task. What is the flag given at the end?

![image](https://user-images.githubusercontent.com/94435318/161412831-3b626cc4-46d5-4bd2-87b9-a1e27bd67527.png)

### Answer: THM{Topology_Flaws}

-----------------------------------------------------------------------------------------------

# 🟥 Task-2 A Primer on Subnetting

As we've previously discussed throughout the module so far, Networks can be found in all shapes and sizes - ranging from small to large. Subnetting is the term given to splitting up a network into smaller, miniature networks within itself. Think of it as slicing up a cake for your friends. There's only a certain amount of cake to go around, but everybody wants a piece. Subnetting is you deciding who gets what slice & reserving such a slice of this metaphorical cake.

Take a business, for example; You will have different departments such as:

     * Accounting
     * Finance
     * Human Resources

![image](https://user-images.githubusercontent.com/94435318/161412939-94b96fee-3646-41ef-b84f-f7a304397413.png)

Whilst you know where to send information in real life to the correct department, networks need to know as well. Network administrators use subnetting to categorise and assign specific parts of a network to reflect this.

Subnetting is achieved by splitting up the number of hosts that can fit within the network, represented by a number called a subnet mask. Let's refer back to our diagram from the first room in this module:

![image](https://user-images.githubusercontent.com/94435318/161412958-0bd62a17-00c0-4fe0-9fea-b901a65147d1.png)

As we can recall, an IP address is made up of four sections called octets. The same goes for a subnet mask which is also represented as a number of four bytes (32 bits), ranging from 0 to 255 (0-255).

Subnets use IP addresses in three different ways:
    * Identify the network address
    * Identify the host address
    * Identify the default gateway

Let's split these three up to understand their purposes into the table below:

![image](https://user-images.githubusercontent.com/94435318/161412991-c22c0baa-1ae8-45bc-9457-bdebcd9f8c9b.png)

Now, in small networks such as at home, you will be on one subnet as there is an unlikely chance that you need more than 254 devices connected at one time.

However, places such as businesses and offices will have much more of these devices (PCs, printers, cameras and sensors), where subnetting takes place.

Subnetting provides a range of benefits, including:
    * Efficiency
    * Security
    * Full control
    
We'll come on to explore exactly how subnetting provides these benefits at a later date; however, for now, all we need to understand is the security element to it. Let's take the typical café on the street. This cafe will have two networks:

One for employees, cash registers, and other devices for the facility
One for the general public to use as a hotspot
Subnetting allows you to separate these two use cases from each other whilst having the benefits of a connection to larger networks such as the Internet.

-----------------------------------------------------------------------------------------------

Answer the questions below
--

### 1. What is the technical term for dividing a network up into smaller pieces?

![image](https://user-images.githubusercontent.com/94435318/161413140-bc6ad1b4-da88-4c17-a8f3-4a8dfa0d7506.png)

### Answer: Subnetting

### 2. How many bits are in a subnet mask?

![image](https://user-images.githubusercontent.com/94435318/161413172-49ac6510-0d8a-4b03-bc60-97348e447359.png)

### Answer: 32

### 3. What is the range of a section (octet) of a subnet mask?

![image](https://user-images.githubusercontent.com/94435318/161413207-724fa49d-da1c-4b70-af68-8dc2625e8f99.png)

### Answer: 0-255


### 4. What address is used to identify the start of a network?

![image](https://user-images.githubusercontent.com/94435318/161413266-cfda2a66-85b3-4fe9-9c5b-9b8b60843220.png)

### Answer: Network Address

### 5. What address is used to identify devices within a network?

![image](https://user-images.githubusercontent.com/94435318/161413324-19c1f30c-81bd-49ba-b6bb-3c6da0348418.png)

### Answer: Host Address

### 6. What is the name used to identify the device responsible for sending data to another network?

![image](https://user-images.githubusercontent.com/94435318/161413376-01e62506-4a7c-4036-8113-2def9b690ac3.png)

### Answer: Default Gateway

----------------------------------------------------------------------------------------------

# 🟥 Task-3 The ARP Protocol

Recalling from our previous tasks that devices can have two identifiers: A MAC address and an IP address, the ARP protocol or Address Resolution Protocol for short, is the technology that is responsible for allowing devices to identify themselves on a network.

Simply, the ARP protocol allows a device to associate its MAC address with an IP address on the network. Each device on a network will keep a log of the MAC addresses associated with other devices.

When devices wish to communicate with another, they will send a broadcast to the entire network searching for the specific device. Devices can use the ARP protocol to find the MAC address (and therefore the physical identifier) of a device for communication.

## How does ARP Work?

Each device within a network has a ledger to store information on, which is called a cache. In the context of the *ARP* protocol, this cache stores the identifiers of other devices on the network.

In order to map these two identifiers together (IP address and MAC address), the ARP protocol sends two types of messages:
     1. ARP Request
     2. ARP Reply
     
When an ARP request is sent, a message is broadcasted to every other device found on a network by the device, asking whether or not the device's MAC address matches the requested IP address. If the device does have the requested IP address, an ARP reply is returned to the initial device to acknowledge this. The initial device will now remember this and store it within its cache (an ARP entry). 

This process is illustrated in the diagram below:

![image](https://user-images.githubusercontent.com/94435318/161413454-763d47a1-cdba-4f4c-8bac-ded2711af127.png)

-------------------------------------------------------------------------------------------

Answer the questions below
--

### 1. What does ARP stand for?

![image](https://user-images.githubusercontent.com/94435318/161413506-e5c355dd-99f1-4c10-99bb-425256fe65c7.png)

### Answer:  Address Resolution Protocol 

### 2. What category of ARP Packet asks a device whether or not it has a specific IP address?

![image](https://user-images.githubusercontent.com/94435318/161413618-b0faa9a6-e8a4-4407-8af0-0dced2fbb267.png)

### Answer: request

### 3. What address is used as a physical identifier for a device on a network?

![image](https://user-images.githubusercontent.com/94435318/161413654-54016644-e93d-4c42-8df7-259064b9ca03.png)

### Answer: MAC Address

### 4. What address is used as a logical identifier for a device on a network?

### Answer: IP Address

--------------------------------------------------------------------------------------------

# 🟥 Task-4 The DHCP Protocol

IP addresses can be assigned either manually, by entering them physically into a device, or automatically and most commonly by using a DHCP (Dynamic Host Configuration Protocol) server. When a device connects to a network, if it has not already been manually assigned an IP address, it sends out a request (DHCP Discover) to see if any DHCP servers are on the network. The DHCP server then replies back with an IP address the device could use (DHCP Offer). The device then sends a reply confirming it wants the offered IP Address (DHCP Request), and then lastly, the DHCP server sends a reply acknowledging this has been completed, and the device can start using the IP Address (DHCP ACK).

![image](https://user-images.githubusercontent.com/94435318/161413772-55ffa527-5f59-461f-9e85-ff7eaf695fd1.png)

----------------------------------------------------------------------------------------------

Answer the questions below:
--

### 1. What type of DHCP packet is used by a device to retrieve an IP address?

![image](https://user-images.githubusercontent.com/94435318/161413935-c35a0157-df56-4a9c-b04c-ef749da86f3d.png)

### Answer: DHCP Discover

### 2. What type of DHCP packet does a device send once it has been offered an IP address by the DHCP server?

![image](https://user-images.githubusercontent.com/94435318/161413953-fc821e91-4adc-4d41-9f84-cc1c181711de.png)

### Answer: DHCP request

### 3. Finally, what is the last DHCP packet that is sent to a device from a DHCP server?

![image](https://user-images.githubusercontent.com/94435318/161413967-0ba2dddf-8699-4fb8-a5fb-f3137eef77eb.png)

### Answer: DHCP ack

------------------------------------------------------------------------------------------------

# 🟥 Task-5 Continue Your Learning: OSI Model

Continue your learning by joining the "OSI Model" room.

Answer the questions below
--

### Join the "OSI Model" room.

### Answer: Click Completed
