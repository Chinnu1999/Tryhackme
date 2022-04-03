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

Answer the questions below
--

#### What does LAN stand for?

![image](https://user-images.githubusercontent.com/94435318/161412260-2a96e801-06b0-45e7-8031-646508acfe22.png)

### Answer: Local Area Network


### What is the verb given to the job that Routers perform?

![image](https://user-images.githubusercontent.com/94435318/161412369-8e36cc60-86b4-4dcd-a1fb-23b7c80e3e47.png)

### Answer: Routing


### What device is used to centrally connect multiple devices on the local network and transmit data to the correct location?

![image](https://user-images.githubusercontent.com/94435318/161412468-8b9d2e31-f09e-485d-89e8-babe79eea6f9.png)

### Answer: Switch


### What topology is cost-efficient to set up?

![image](https://user-images.githubusercontent.com/94435318/161412576-105e0d2b-7426-4e40-acca-506f56645c50.png)

### Answer: Bus Topology

### What topology is expensive to set up and maintain?

![image](https://user-images.githubusercontent.com/94435318/161412667-919771c1-07c5-4f0c-adfa-347c59acd9cc.png)

### Answer: Star Topology

### Complete the interactive lab attached to this task. What is the flag given at the end?

![image](https://user-images.githubusercontent.com/94435318/161412831-3b626cc4-46d5-4bd2-87b9-a1e27bd67527.png)

### Answer: THM{Topology_Flaws}

# 🟥 Task-2 A Primer on Subnetting

As we've previously discussed throughout the module so far, Networks can be found in all shapes and sizes - ranging from small to large. Subnetting is the term given to splitting up a network into smaller, miniature networks within itself. Think of it as slicing up a cake for your friends. There's only a certain amount of cake to go around, but everybody wants a piece. Subnetting is you deciding who gets what slice & reserving such a slice of this metaphorical cake.

Take a business, for example; You will have different departments such as:

     * Accounting
     * Finance
     * Human Resources