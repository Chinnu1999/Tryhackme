![image](https://user-images.githubusercontent.com/94435318/154881500-d80eb616-9787-4f1d-a2f3-59a9c2b53d83.png)

Task-1 Introduction

Without a doubt, the ability to research effectively is the most important quality for a hacker to have. By its very nature, hacking requires a vast knowledge base -- because how are you supposed to break into something if you don't know how it works? The thing is: no one knows everything. Everyone (professional or amateur, experienced or totally new to the subject) will encounter problems which they don't automatically know how to solve. This is where research comes in, as, in the real world, you can't ever expect to simply be handed the answers to your questions.

As your experience level increases, you will find that the things you're researching scale in their difficulty accordingly; however, in the field of information security, there will never come a point where you don't need to look things up.

This room will serve as a brief overview of some of the most important resources available to you, and will hopefully aid you in the process of building a research methodology that works for you.

We will be looking at the following topics:
• An example of a research question
• Vulnerability Searching tools
• Linux Manual Pages

Let's begin.

Tak-2 Example Research Question

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

1. In the Burp Suite Program that ships with Kali Linux, what mode would you use to manually send a request (often repeating a captured request numerous times)?

![image](https://user-images.githubusercontent.com/94435318/154883281-3b213148-436f-4d11-9c51-8f41ff2124ff.png)

![image](https://user-images.githubusercontent.com/94435318/154883153-dba6bae2-3a45-4112-81b5-a4e8828b49e8.png)

Answer - Repeater

2. What hash format are modern Windows login passwords stored in?

![image](https://user-images.githubusercontent.com/94435318/154883744-103b30fa-1fe5-40c6-ad47-c6866e573a02.png)

Answer - NTLM
