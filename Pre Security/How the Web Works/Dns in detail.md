To become a better hacker it's vital to understand the underlying functions of the world wide web and what makes it work.

![image](https://user-images.githubusercontent.com/94435318/161414698-2f74ab56-fa4b-40e0-8238-2b7e5500da1d.png)

# 🟥 Task-1 What is DNS?

## What is DNS?

DNS (Domain Name System) provides a simple way for us to communicate with devices on the internet without remembering complex numbers. Much like every house has a unique address for sending mail directly to it, every computer on the internet has its own unique address to communicate with it called an IP address. An IP address looks like the following 104.26.10.229, 4 sets of digits ranging from 0 - 255 separated by a period. When you want to visit a website, it's not exactly convenient to remember this complicated set of numbers, and that's where DNS can help. So instead of remembering 104.26.10.229, you can remember tryhackme.com instead.

![image](https://user-images.githubusercontent.com/94435318/161414746-e3a12fb2-2fa0-4fc7-80ce-1447c40795a5.png)

---------------------------------------------------------------------------------------------

Answer the questions below ------------------------------------------
--
### 1. What does DNS stand for?

![image](https://user-images.githubusercontent.com/94435318/161414810-f5b26d9f-5bb6-4fb8-9d71-94c7f19ffb26.png)

### Answer: Domain Name System

# 🟥 Task-2 Domain Hierarchy

## Domain Hierarchy

![image](https://user-images.githubusercontent.com/94435318/161414838-14fcc027-b985-4b83-9df0-4dfb399612c3.png)

## TLD (Top-Level Domain)

A TLD is the most righthand part of a domain name. So, for example, the tryhackme.com TLD is .com. There are two types of TLD, gTLD (Generic Top Level) and ccTLD (Country Code Top Level Domain). Historically a gTLD was meant to tell the user the domain name's purpose; for example, a .com would be for commercial purposes, .org for an organisation, .edu for education and .gov for government. And a ccTLD was used for geographical purposes, for example, .ca for sites based in Canada, .co.uk for sites based in the United Kingdom and so on. Due to such demand, there is an influx of new gTLDs ranging from .online , .club , .website , .biz and so many more. For a full list of over 2000 TLDs click here.

## Second-Level Domain

Taking tryhackme.com as an example, the .com part is the TLD, and tryhackme is the Second Level Domain. When registering a domain name, the second-level domain is limited to 63 characters + the TLD and can only use a-z 0-9 and hyphens (cannot start or end with hyphens or have consecutive hyphens).

## Subdomain

A subdomain sits on the left-hand side of the Second-Level Domain using a period to separate it; for example, in the name admin.tryhackme.com the admin part is the subdomain. A subdomain name has the same creation restrictions as a Second-Level Domain, being limited to 63 characters and can only use a-z 0-9 and hyphens (cannot start or end with hyphens or have consecutive hyphens). You can use multiple subdomains split with periods to create longer names, such as jupiter.servers.tryhackme.com. But the length must be kept to 253 characters or less. There is no limit to the number of subdomains you can create for your domain name.

---------------------------------------------------------------------------------------------

Answer the questions below -----------------------------------------
--

### 1. What is the maximum length of a subdomain?

![image](https://user-images.githubusercontent.com/94435318/161414956-dd5de1b4-44ca-485a-afa8-f52ab03d14db.png)

### Answer: 63

### 2. Which of the following characters cannot be used in a subdomain ( 3 b _ - )?

### Answer: _

### 3. What is the maximum length of a domain name?

![image](https://user-images.githubusercontent.com/94435318/161414974-422ff2ec-fe21-495e-804c-cbf193dcfc09.png)

### Answer: 253

### 4. What type of TLD is .co.uk?

![image](https://user-images.githubusercontent.com/94435318/161415000-951ad6a0-7387-4e00-bad4-d2b2ab6405a3.png)

### Answer: ccTLD
