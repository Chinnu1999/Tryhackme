![image](https://user-images.githubusercontent.com/94435318/154964482-0b24e62a-990c-4e0e-8652-d0ba23611806.png)

🌟 Google Dorking 
--

🔴 Task-1 Ye 0l' Search Engine
--


Google is arguably the most famous example of “Search Engines”, I mean who remembers Ask Jeeves? shudders

Now it might be rather patronising explaining how these “Search Engines” work, but there’s a lot more going on behind the scenes then what we see. More importantly, we can leverage this to our advantage to find all sorts of things that a wordlist wouldn’t. Researching as a whole - especially in the context of Cybersecurity encapsulates almost everything you do as a pentester. MuirlandOracle has created a fantastic room on learning the attitudes towards how to research, and what information you can gain from it exactly.

"Search Engines" such as Google are huge indexers – specifically, indexers of content spread across the World Wide Web.

These essentials in surfing the internet use “Crawlers” or “Spiders” to search for this content across the World Wide Web, which I will discuss in the next task.

Answer the questions below ----------------------------------------------------------------
--

🔴 Tasl-2 Let's Learn About Crawlers
--

What are Crawlers and how do They Work?

These crawlers discover content through various means. One being by pure discovery, where a URL is visited by the crawler and information regarding the content type of the website is returned to the search engine. In fact, there are lots of information modern crawlers scrape – but we will discuss how this is used later. Another method crawlers use to discover content is by following any and all URLs found from previously crawled websites. Much like a virus in the sense that it will want to traverse/spread to everything it can.

Let's Visualise Some Things...

The diagram below is a high-level abstraction of how these web crawlers work. Once a web crawler discovers a domain such as mywebsite.com, it will index the entire contents of the domain, looking for keywords and other miscellaneous information - but I will discuss this miscellaneous information later.

![image](https://user-images.githubusercontent.com/94435318/154965175-d5b67670-a215-4817-9f86-941332fbf425.png)

In the diagram above, "mywebsite.com" has been scraped as having the keywords as “Apple” “Banana" and “Pear”. These keywords are stored in a dictionary by the crawler, who then returns these to the search engine i.e. Google. Because of this persistence, Google now knows that the domain “mywebsite.com” has the keywords “Apple", “Banana” and “Pear”. As only one website has been crawled, if a user was to search for “Apple”...“mywebsite.com” would appear. This would result in the same behaviour if the user was to search for “Banana”. As the indexed contents from the crawler report the domain as having “Banana”, it will be displayed to the user.

As illustrated below, a user submits a query to the search engine of “Pears". Because the search engine only has the contents of one website that has been crawled with the keyword of “Pears” it will be the only domain that is presented to the user. 

![image](https://user-images.githubusercontent.com/94435318/154965293-615d36e7-9457-427a-8811-1ca25b53c256.png)

However, as we previously mentioned, crawlers attempt to traverse, termed as crawling, every URL and file that they can find! Say if “mywebsite.com” had the same keywords as before (“Apple", “Banana” and “Pear”), but also had a URL to another website “anotherwebsite.com”, the crawler will then attempt to traverse everything on that URL (anotherwebsite.com) and retrieve the contents of everything within that domain respectively.

This is illustrated in the diagram below. The crawler initially finds “mywebsite.com”, where it crawls the contents of the website - finding the same keywords (“Apple", “Banana” and “Pear”) as before, but it has additionally found an external URL. Once the crawler is complete on “mywebsite.com”, it'll proceed to crawl the contents of the website “anotherwebsite.com”, where the keywords ("Tomatoes", “Strawberries” and “Pineapples”) are found on it. The crawler's dictionary now contains the contents of both “mywebsite.com” and “anotherwebsite.com”, which is then stored and saved within the search engine.

![image](https://user-images.githubusercontent.com/94435318/154965426-d30a7a87-f948-45bd-8fe0-1b7d03ac2d64.png)

Recapping
--
So to recap, the search engine now has knowledge of two domains that have been crawled:
1. mywebsite.com
2. anotherwebsite.com

Although note that “anotherwebsite.com” was only crawled because it was referenced by the first domain “mywebsite.com”. Because of this reference, the search engine knows the following about the two domains:

Domain Name                     	Keyword
mywebsite.com	                    Apples
mywebsite.com
	Bananas
mywebsite.com
	Pears
anotherwebsite.com	Tomatoes
anotherwebsite.com	Strawberries
anotherwebsite.com	Pineapples
