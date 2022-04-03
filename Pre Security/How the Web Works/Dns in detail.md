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

--------------------------------------------------------------------------------------------

# 🟥 Task-3 Record Types

## DNS Record Types

DNS isn't just for websites though, and multiple types of DNS record exist. We'll go over some of the most common ones that you're likely to come across.

## A Record

These records resolve to IPv4 addresses, for example 104.26.10.229

## AAAA Record

These records resolve to IPv6 addresses, for example 2606:4700:20::681a:be5

## CNAME Record

These records resolve to another domain name, for example, TryHackMe's online shop has the subdomain name store.tryhackme.com which returns a CNAME record shops.shopify.com. Another DNS request would then be made to shops.shopify.com to work out the IP address.

## MX Record

These records resolve to the address of the servers that handle the email for the domain you are querying, for example an MX record response for tryhackme.com would look something like alt1.aspmx.l.google.com. These records also come with a priority flag. This tells the client in which order to try the servers, this is perfect for if the main server goes down and email needs to be sent to a backup server.

## TXT Record

TXT records are free text fields where any text-based data can be stored. TXT records have multiple uses, but some common ones can be to list servers that have the authority to send an email on behalf of the domain (this can help in the battle against spam and spoofed email). They can also be used to verify ownership of the domain name when signing up for third party services.

Answer the questions below ----------------------------------------------------------------
--

### 1. What type of record would be used to advise where to send email?

![image](https://user-images.githubusercontent.com/94435318/161415163-edc031fc-1225-4e10-b909-fb6442f633d2.png)

### Answer: MX

### 2. What type of record handles IPv6 addresses?

![image](https://user-images.githubusercontent.com/94435318/161415180-3d1f627a-614d-4903-8d18-9834f237a820.png)

### Answer: AAAA

---------------------------------------------------------------------------------------------

# 🟥 Task-4 Making A Request

## What happens when you make a DNS request

    1. When you request a domain name, your computer first checks its local cache to see if you've previously looked up the address recently; if not, a request to your Recursive DNS Server will be made.

    2. A Recursive DNS Server is usually provided by your ISP, but you can also choose your own. This server also has a local cache of recently looked up domain names. If a result is found locally, this is sent back to your computer, and your request ends here (this is common for popular and heavily requested services such as Google, Facebook, Twitter). If the request cannot be found locally, a journey begins to find the correct answer, starting with the internet's root DNS servers.

    3. The root servers act as the DNS backbone of the internet; their job is to redirect you to the correct Top Level Domain Server, depending on your request. If, for example, you request www.tryhackme.com, the root server will recognise the Top Level Domain of .com and refer you to the correct TLD server that deals with .com addresses.

    4. The TLD server holds records for where to find the authoritative server to answer the DNS request. The authoritative server is often also known as the nameserver for the domain. For example, the name server for tryhackme.com is kip.ns.cloudflare.com and uma.ns.cloudflare.com. You'll often find multiple nameservers for a domain name to act as a backup in case one goes down.

    5. An authoritative DNS server is the server that is responsible for storing the DNS records for a particular domain name and where any updates to your domain name DNS records would be made. Depending on the record type, the DNS record is then sent back to the Recursive DNS Server, where a local copy will be cached for future requests and then relayed back to the original client that made the request. DNS records all come with a TTL (Time To Live) value. This value is a number represented in seconds that the response should be saved for locally until you have to look it up again. Caching saves on having to make a DNS request every time you communicate with a server.

![image](https://user-images.githubusercontent.com/94435318/161415270-91d9e227-189d-4002-b111-de2b9b493a4e.png)

--------------------------------------------------------------------------------------------

Answer the questions below ------------------------------------------------------------------
--

### 1. What field specifies how long a DNS record should be cached for?

![image](https://user-images.githubusercontent.com/94435318/161415417-c79fe655-7aec-4085-8f67-dfb0a450cd2a.png)

### Answer: TTL

### 2. What type of DNS Server is usually provided by your ISP?

![image](https://user-images.githubusercontent.com/94435318/161415433-93a1e299-a64a-4ff6-a079-903492b2ab64.png)

### Answer: Recursive

### 3. What type of server holds all the records for a domain?

![image](https://user-images.githubusercontent.com/94435318/161415454-db047734-6061-4663-8dce-37656ab6de08.png)

### Answer: Authoritative

---------------------------------------------------------------------------------------------

# 🟥 Task-5 Practical

Using the website on the right, we can build requests to make DNS queries and view the results. The website will also show you the command you'd need to run on your own computer if you wished to make the requests yourself.

Answer the questions below-----------------------------------
--

### 1. What is the CNAME of shop.website.thm?

![image](https://user-images.githubusercontent.com/94435318/161415571-aa2a035a-9b3d-48b0-b28f-4669930ef4e0.png)

![image](https://user-images.githubusercontent.com/94435318/161415595-ba04b8bf-5dac-487a-90cc-9f9e9608abeb.png)

### Answer: shops.myshopify.com

### 2. What is the value of the TXT record of website.thm?

![image](https://user-images.githubusercontent.com/94435318/161415625-f10a7e24-6d79-4745-86a6-88c4c4f95b13.png)

### Answer: THM{7012BBA60997F35A9516C2E16D2944FF}

### 3. What is the numerical priority value for the MX record?

![image](https://user-images.githubusercontent.com/94435318/161415681-8417b278-e3d0-4756-ad2c-b588bb3d1833.png)

### Answer: 30

### 4. What is the IP address for the A record of www.website.thm?

![image](https://user-images.githubusercontent.com/94435318/161415744-e10aa03b-8ca7-4753-8415-e022172fa9c4.png)

### Answer: 10.10.10.10
