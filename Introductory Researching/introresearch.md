![image](https://user-images.githubusercontent.com/94435318/154881500-d80eb616-9787-4f1d-a2f3-59a9c2b53d83.png)

Task-1 Introduction
---
Without a doubt, the ability to research effectively is the most important quality for a hacker to have. By its very nature, hacking requires a vast knowledge base -- because how are you supposed to break into something if you don't know how it works? The thing is: no one knows everything. Everyone (professional or amateur, experienced or totally new to the subject) will encounter problems which they don't automatically know how to solve. This is where research comes in, as, in the real world, you can't ever expect to simply be handed the answers to your questions.

As your experience level increases, you will find that the things you're researching scale in their difficulty accordingly; however, in the field of information security, there will never come a point where you don't need to look things up.

This room will serve as a brief overview of some of the most important resources available to you, and will hopefully aid you in the process of building a research methodology that works for you.

We will be looking at the following topics:
• An example of a research question
• Vulnerability Searching tools
• Linux Manual Pages

Let's begin.

Tak-2 Example Research Question
---
We'll begin by looking at a typical research question: the kind that you're likely to find when working through a CTF on TryHackMe.

Let's say you've downloaded a JPEG image from a remote server. You suspect that there's something hidden inside it, but how can you get it out?
How about we start by searching for “hiding things inside images” in Google:

![image](https://user-images.githubusercontent.com/94435318/154881819-e4745987-889b-4f1e-8cc7-cf1c3edac5c0.png)

Notice that the second link down gives us the title of a technique: “Steganography”. You can then click that link and read the document, which will teach you how files are hidden inside images.


Ok, so we know how it's done, let's try searching for a way to extract files using steganography:

![image](https://user-images.githubusercontent.com/94435318/154881938-fe26817b-6a85-4bde-8cbf-8628969c49e1.png)

Already virtually every link is pointing to something useful. The first link contains a collection of useful tools, the second is more instructions on how to perform steganography in the first place. Realistically any of these links could prove useful, but let's take a look at that first one (https://0xrick.github.io/lists/stego/):

![image](https://user-images.githubusercontent.com/94435318/154882093-8a1bb77a-358d-4a44-b965-f91d0e33177c.png)

![image](https://user-images.githubusercontent.com/94435318/154882206-44338f5d-b8a9-4333-98cd-7919edfd4ec7.png)

The very first tool there looks to be useful. It can be used to extract embedded data from JPEG files -- exactly what we need it to do! This page also tells you that steghide can be installed using something called “apt”.
Let's search that up next!

![image](https://user-images.githubusercontent.com/94435318/154882349-a01a969e-1a92-41ae-9dc5-fb00b2b7cffe.png)

Great -- so apt is a package manager that lets us install tools on Linux distributions like Ubuntu (or Kali!).
How can we install packages using apt? Let's search it!

![image](https://user-images.githubusercontent.com/94435318/154882462-f72972c4-df63-44a8-ae76-96fa61ecb1ee.png)

Perfect -- right at the top of the page we're given instructions. We know that our package is called steghide, so we can go ahead and install that:

![image](https://user-images.githubusercontent.com/94435318/154882784-09bfaa25-dd3b-454a-ab25-7168d60508db.png)

Now, let's switch back to that collection of steganography tools we were looking at before. Did you notice that there were instructions on how to use steghide right there?

Useful commands:
steghide info file : displays info about a file whether it has embedded data or not.
steghide extract -sf file : extracts embedded data from a file

There we go! That's how we can extract an image from a file. Our research has paid off and we can now go and complete the task.

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Notice the methodology here. We started with nothing, but gradually built up a picture of what we needed to do. We had a question (How can I extract data from this image). We searched for an answer to that question, then continued to query each of the answers we were given until we had a full understanding of the topic. This is a really good way to conduct research: Start with a question; get an initial understanding of the topic; then look into more advanced aspects as needed.

Now it's your turn. See if you can answer the following questions using your research skills. The first three questions have appropriate search queries in the hints:

Answer the questions below -------------------------------------
---
1. In the Burp Suite Program that ships with Kali Linux, what mode would you use to manually send a request (often repeating a captured request numerous times)?

![image](https://user-images.githubusercontent.com/94435318/154883281-3b213148-436f-4d11-9c51-8f41ff2124ff.png)

![image](https://user-images.githubusercontent.com/94435318/154883153-dba6bae2-3a45-4112-81b5-a4e8828b49e8.png)

Answer - Repeater
---
2. What hash format are modern Windows login passwords stored in?

![image](https://user-images.githubusercontent.com/94435318/154883862-aeca730e-00cf-40c4-b06e-59b942a2fd41.png)

![image](https://user-images.githubusercontent.com/94435318/154883744-103b30fa-1fe5-40c6-ad47-c6866e573a02.png)

Answer - NTLM
---
3. What are automated tasks called in Linux?

![image](https://user-images.githubusercontent.com/94435318/154883946-8b5e46a9-c951-438a-8233-66ceba2fe5c4.png)

![image](https://user-images.githubusercontent.com/94435318/154883991-cb689807-9475-427a-9c4e-e3f81f263d9e.png)

Answer - Cron Jobs
---
4. What number base could you use as a shorthand for base 2 (binary)?

![image](https://user-images.githubusercontent.com/94435318/154884074-4e848ab1-c5ec-44c2-a7ea-ceec9522a465.png)

![image](https://user-images.githubusercontent.com/94435318/154884250-07fc9045-a9fc-46d9-8e94-05f464fff3ba.png)

Answer - base 16
---
5. If a password hash starts with $6$, what format is it (Unix variant)?

![image](https://user-images.githubusercontent.com/94435318/154884775-014edffa-de4c-4164-820f-886804af8120.png)

![image](https://user-images.githubusercontent.com/94435318/154884729-6b52c16d-5c22-4639-8962-61538dd981eb.png)

Answer - sha512crypt
---
Task-3 Vulnerability Searching 
---
Often in hacking you'll come across software that might be open to exploitation. For example, Content Management Systems (such as Wordpress, FuelCMS, Ghost, etc) are frequently used to make setting up a website easier, and many of these are vulnerable to various attacks. So where would we look if we wanted to exploit specific software?

The answer to that question lies in websites such as:

    ExploitDB
    NVD
    CVE Mitre

NVD keeps track of CVEs (Common Vulnerabilities and Exposures) -- whether or not there is an exploit publicly available -- so it's a really good place to look if you're researching vulnerabilities in a specific piece of software. CVEs take the form: CVE-YEAR-IDNUMBER
(Hint Hint: It's going to be really useful in the questions!)

ExploitDB tends to be very useful for hackers, as it often actually contains exploits that can be downloaded and used straight out of the box. It tends to be one of the first stops when you encounter software in a CTF or pentest.

If you're inclined towards the CLI on Linux, Kali comes pre-installed with a tool called "searchsploit" which allows you to search ExploitDB from your own machine. This is offline, and works using a downloaded version of the database, meaning that you already have all of the exploits already on your Kali Linux!

Let's take an example. Say we're playing a CTF and we come across a website:

![image](https://user-images.githubusercontent.com/94435318/154885417-d666b50f-f9b5-46ed-a158-d452929d181c.png)

Well, this is quite obviously FuelCMS. Usually it won't be this obvious, but hey, we'll work with what we've got!

We know the software, so let's search for it in ExploitDB.
(Note: I'm going to use the CLI tool in Kali, as it tends to be quicker from a workflow perspective -- however, you are welcome to use the website)

I'm using the command searchsploit fuel cms to search for exploits:

![image](https://user-images.githubusercontent.com/94435318/154885527-5533288c-674a-4cd6-89c9-89bdb442ef2e.png)

If you prefer doing things in the website, here are the results from there:

![image](https://user-images.githubusercontent.com/94435318/154885792-fddf17bb-e345-4a02-846b-f41ebbbcff17.png)

Success! We've got an exploit that we can now use against the website!

Actually using the exploit is outwith the scope of this room, but you can see the process. 

If you click on the title you'll be given a bit more of an explanation about the exploit:

Information about a remote code execution in FuelCMS 1.4.1

![image](https://user-images.githubusercontent.com/94435318/154885903-dc8c4ba0-8d58-424c-8454-85cdc5ec088c.png)

Pay particular attention to the CVE numbers; you'll need them for the questions!

The format will be like so: CVE-YEAR-NUMBER

Answer the questions below ----------------------------------------------
---
1. What is the CVE for the 2020 Cross-Site Scripting (XSS) vulnerability found in WPForms?

![image](https://user-images.githubusercontent.com/94435318/154886297-33cd9b2f-13fb-4a58-952f-452a15c3fc02.png)

Answer - CVE-2020-10385
---
2. There was a Local Privilege Escalation vulnerability found in the Debian version of Apache Tomcat, back in 2016. What's the CVE for this vulnerability?

![image](https://user-images.githubusercontent.com/94435318/154886521-f0cb1c14-a386-4895-83f5-00e4b4193f9b.png)

Answer - CVE-2016-1240
---
3. What is the very first CVE found in the VLC media player?

![image](https://user-images.githubusercontent.com/94435318/154890713-429ca294-241a-43b7-b9b5-893fd59080b4.png)

Answer - CVE-2007-0017
---
4. If you wanted to exploit a 2020 buffer overflow in the sudo program, which CVE would you use?

![image](https://user-images.githubusercontent.com/94435318/154891440-eadb3b25-912c-40dc-a3d6-a643343c6002.png)

Answer - CVE-2019-18634
---
Task-4 Manual Pages
---
If you haven't already worked in Linux, take a look at the Linux Fundamentals module. Linux (usually Kali Linux) is without a doubt the most ubiquitous operating system used in hacking, so it pays to be familiar with it!

One of the many useful features of Linux is the inbuilt man command, which gives you access to the manual pages for most tools directly inside your terminal. Occasionally you'll find a tool that doesn't have a manual entry; however, this is rare. Generally speaking, when you don't know how to use a tool, man should be your first port of call.

Let's give this a shot!

Say we want to connect to a remote computer using SSH, but we don't know the syntax. We can try man ssh to get the manual page for SSH:

![image](https://user-images.githubusercontent.com/94435318/154892065-a71994a2-12c5-4da0-ac66-bead652f39f9.png)

Awesome!

We can see in the description that the syntax for using SSH is <user@host>:
    
We can also use the man pages to look for special switches in programs that make the program do other things. An example of this would be that (from our very first example) steghide can be used to both extract and embed files inside an image, based on the switches that you give it. 

For example, if you wanted to display the version number for SSH, you would scroll down in the man page until you found an appropriate switch:

   ![image](https://user-images.githubusercontent.com/94435318/154892278-02580037-f31e-4d65-99c1-a7436231f396.png)
   
Then use it:

![image](https://user-images.githubusercontent.com/94435318/154892845-83659f6a-b183-40d3-a8f6-2ce9ca109031.png)

Another way to find that switch would have been to search the man page for the correct switch using grep:

![image](https://user-images.githubusercontent.com/94435318/154892881-91c0528d-4544-40a8-9ca7-0bf38a51edd8.png)

Now your turn! Answer the following questions using the man command:

Answer the questions below ----------------------------------------------------
---
1. SCP is a tool used to copy files from one computer to another. What switch would you use to copy an entire directory?

use man scp command in terminal

![image](https://user-images.githubusercontent.com/94435318/154893203-4999a764-2e41-4857-aea4-dad38d63e9a6.png)

Answer: -r
---
2. fdisk is a command used to view and alter the partitioning scheme used on your hard drive. What switch would you use to list the current partitions?
 
![image](https://user-images.githubusercontent.com/94435318/154894231-d3030ea0-176d-4ff0-9a5d-2b7b5d760f77.png)

Answer:  -l
---
3. nano is an easy-to-use text editor for Linux. There are arguably better editors (Vim, being the obvious choice); however, nano is a great one to start with. What switch would you use to make a backup when opening a file with nano?

![image](https://user-images.githubusercontent.com/94435318/154894359-8a83307c-347f-4cae-aa09-4e9165806b2c.png)

AnswerL -B
---
4. Netcat is a basic tool used to manually send and receive network requests. What command would you use to start netcat in listen mode, using port 12345?

![image](https://user-images.githubusercontent.com/94435318/154894765-2198f301-7d5a-483d-af8a-9564308ab000.png)
![image](https://user-images.githubusercontent.com/94435318/154894792-f48cf8fc-7e0e-4487-9bf9-05533827eb94.png)

Answer: nc -l -p 12345
---
Task-5 Final Thoughts
---

You may have been told in school that there are good sources and bad sources of information. That may be true when it comes to essays and referencing information; however, it's my pleasure to state that it does not apply here. Any information can potentially be useful -- so feel free to use blogs, wikipedia, or anything else that contains what you're looking for! Blogs especially can often be very valuable for learning when it comes to information security, as many security researchers keep a blog.

Having completed this room, you hopefully now have established the basis of a methodology to tackle research questions that you come across by yourself. The vast majority of rooms on TryHackMe can be solved purely using knowledge found on Google, so please take the opportunity to improve your skills by Googling any problems you come across!

As a follow-up to this room, complete CMNatic's Google Dorking room to learn some advanced Google tricks!

Completed:
---
![image](https://user-images.githubusercontent.com/94435318/154894907-ef8ab152-4962-4a24-8899-2336b5ce05f0.png)

![image](https://user-images.githubusercontent.com/94435318/154894961-0370cc67-5172-4663-ac19-66ad54cb9c8d.png)

-----------------------------------------------------------------------------------------------------
