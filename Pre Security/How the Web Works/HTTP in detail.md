![image](https://user-images.githubusercontent.com/94435318/161420700-2fdcc2da-2c21-4da7-87d1-e530690d15eb.png)

# 🟥 Task-1 What is HTTP(S)?

## What is HTTP? (HyperText Transfer Protocol)

HTTP is what's used whenever you view a website, developed by Tim Berners-Lee and his team between 1989-1991. HTTP is the set of rules used for communicating with web servers for the transmitting of webpage data, whether that is HTML, Images, Videos, etc.

## What is HTTPS? (HyperText Transfer Protocol Secure)

HTTPS is the secure version of HTTP. HTTPS data is encrypted so it not only stops people from seeing the data you are receiving and sending, but it also gives you assurances that you're talking to the correct web server and not something impersonating it.

--------------------------------------------------------------------------------------------------

Answer the questions below----------------------------------------------------------------------
--

### 1. What does HTTP stand for?

![image](https://user-images.githubusercontent.com/94435318/161420939-e2b3f6bd-b736-4832-b419-80747707afe6.png)

### Answer: HyperText Transfer Protocol

### 2. What does the S in HTTPS stand for?

![image](https://user-images.githubusercontent.com/94435318/161420968-2ec5dc78-8b27-41b9-bb39-42cf634d8391.png)

### Answer: Secure

### 3. On the mock webpage on the right there is an issue, once you've found it, click on it. What is the challenge flag?

![image](https://user-images.githubusercontent.com/94435318/161421030-28e9819e-003b-4bc1-a895-081f890b834b.png)

### Answer: THM{INVALID_HTTP_CERT}

--------------------------------------------------------------------------------------------

# 🟥 Task-2 Requests And Responses

When we access a website, your browser will need to make requests to a web server for assets such as HTML, Images, and download the responses. Before that, you need to tell the browser specifically how and where to access these resources, this is where URLs will help.

## What is a URL? (Uniform Resource Locator)

If you’ve used the internet, you’ve used a URL before. A URL is predominantly an instruction on how to access a resource on the internet. The below image shows what a URL looks like with all of its features (it does not use all features in every request).

![image](https://user-images.githubusercontent.com/94435318/161421131-300430b6-e1d7-4fb4-bcb0-d43af2fc8911.png)

Scheme: This instructs on what protocol to use for accessing the resource such as HTTP, HTTPS, FTP (File Transfer Protocol).

User: Some services require authentication to log in, you can put a username and password into the URL to log in.

Host: The domain name or IP address of the server you wish to access.

Port: The Port that you are going to connect to, usually 80 for HTTP and 443 for HTTPS, but this can be hosted on any port between 1 - 65535.

Path: The file name or location of the resource you are trying to access.

Query String: Extra bits of information that can be sent to the requested path. For example, /blog?id=1 would tell the blog path that you wish to receive the blog article with the id of 1.

Fragment: This is a reference to a location on the actual page requested. This is commonly used for pages with long content and can have a certain part of the page directly linked to it, so it is viewable to the user as soon as they access the page.

## Making a Request
             It's possible to make a request to a web server with just one line "GET / HTTP/1.1"
             
 <p align="center">
  <img width="460" height="300" src="https://user-images.githubusercontent.com/94435318/161421168-f78b626f-5a56-4b6a-875b-2467d3f722c1.png">
</p>            

But for a much richer web experience, you’ll need to send other data as well. This other data is sent in what is called headers, where headers contain extra information to give to the web server you’re communicating with, but we’ll go more into this in the Header task.

Example Request:
GET / HTTP/1.1
Host: tryhackme.com
User-Agent: Mozilla/5.0 Firefox/87.0
Referer: https://tryhackme.com/

To breakdown each line of this request:

Line 1: This request is sending the GET method ( more on this in the HTTP Methods task ), request the home page with / and telling the web server we are using HTTP protocol version 1.1.

Line 2: We tell the web server we want the website tryhackme.com

Line 3: We tell the web server we are using the Firefox version 87 Browser

Line 4: We are telling the web server that the web page that referred us to this one is https://tryhackme.com

Line 5: HTTP requests always end with a blank line to inform the web server that the request has finished.

Example Response:

HTTP/1.1 200 OK
Server: nginx/1.15.8
Date: Fri, 09 Apr 2021 13:34:03 GMT
Content-Type: text/html
Content-Length: 98

<html>
<head>
    <title>TryHackMe</title>
</head>
<body>
    Welcome To TryHackMe.com
</body>
</html>

To breakdown each line of the response:

Line 1: HTTP 1.1 is the version of the HTTP protocol the server is using and then followed by the HTTP Status Code in this case "200 Ok" which tells us the request has completed successfully.

Line 2: This tells us the web server software and version number.

Line 3: The current date, time and timezone of the web server.

Line 4: The Content-Type header tells the client what sort of information is going to be sent, such as HTML, images, videos, pdf, XML.

Line 5: Content-Length tells the client how long the response is, this way we can confirm no data is missing.

Line 6: HTTP response contains a blank line to confirm the end of the HTTP response.

Lines 7-14: The information that has been requested, in this instance the homepage.

Answer the questions below-------------------------------------------------------------------
--

### 1. What HTTP protocol is being used in the above example?

![image](https://user-images.githubusercontent.com/94435318/161421466-1eb4ad54-aee2-440e-b705-33a90389e09e.png)

### Answer: HTTP/1.1

### 2. What response header tells the browser how much data to expect?

![image](https://user-images.githubusercontent.com/94435318/161421490-464783c9-8114-4c6f-add8-c33d195e614d.png)

### Answer: content-length

---------------------------------------------------------------------------------------------

# 🟥 Task-3 HTTP Methods

HTTP methods are a way for the client to show their intended action when making an HTTP request. There are a lot of HTTP methods but we'll cover the most common ones, although mostly you'll deal with the GET and POST method.

## GET Request

This is used for getting information from a web server.

## POST Request

This is used for submitting data to the web server and potentially creating new records

## PUT Request

This is used for submitting data to a web server to update information

## DELETE Request

This is used for deleting information/records from a web server.

---------------------------------------------------------------------------------------------

Answer the questions below----------------------------------------------------------------
--

### 1. What method would be used to create a new user account?

![image](https://user-images.githubusercontent.com/94435318/161421689-d2451329-b02b-4df4-bdfe-69d4b819c20c.png)

### Answer: POST

### 2. What method would be used to update your email address?

![image](https://user-images.githubusercontent.com/94435318/161421708-920bbfff-0b05-4d4a-8b41-f633e511a1cb.png)

### Answer: PUT

### 3. What method would be used to remove a picture you've uploaded to your account?

![image](https://user-images.githubusercontent.com/94435318/161421733-9e9e13e8-534d-4190-9c6a-e29ace0d6d1e.png)

### Answer: DELETE

### 4. What method would be used to view a news article?

![image](https://user-images.githubusercontent.com/94435318/161421757-671412cf-4a64-4b49-b078-f077c59500f3.png)

### Answer: GET

-----------------------------------------------------------------------------------------------

# 🟥 Task-4 HTTP Status Code

## HTTP Status Codes:

In the previous task, you learnt that when a HTTP server responds, the first line always contains a status code informing the client of the outcome of their request and also potentially how to handle it. These status codes can be broken down into 5 different ranges:

![image](https://user-images.githubusercontent.com/94435318/161421815-d562f0dc-984b-4bde-b75d-d9aa2f28f20f.png)

## Common HTTP Status Codes:

There are a lot of different HTTP status codes and that's not including the fact that applications can even define their own, we'll go over the most common HTTP responses you are likely to come across:

![image](https://user-images.githubusercontent.com/94435318/161421840-2c9588e6-09c1-4bd8-8026-6bf4ff97dbdb.png)

Click the "View Site" button on the right to see what some of these HTTP status messages look like in a browser.

---------------------------------------------------------------------------------------------

Answer the questions below----------------------------------------------------------------
--

### 1. What response code might you receive if you've created a new user or blog post article?

![image](https://user-images.githubusercontent.com/94435318/161422078-8048c0ae-a40c-4193-a16b-c715de5cf277.png)

### Answer: 201

### 2. What response code might you receive if you've tried to access a page that doesn't exist?

![image](https://user-images.githubusercontent.com/94435318/161422106-70352c57-9da1-4fc4-92a9-15f3b0e7adb3.png)

### Answer: 404

### 3. What response code might you receive if the web server cannot access its database and the application crashes?

![image](https://user-images.githubusercontent.com/94435318/161422144-d27efa89-dbdb-4882-85af-ac9e33fe724b.png)

### Answer: 503

### 4. What response code might you receive if you try to edit your profile without logging in first?

![image](https://user-images.githubusercontent.com/94435318/161422185-4d31f9f9-1357-4fcb-9f7c-9e9aeec1bb5a.png)

### Answer: 401

---------------------------------------------------------------------------------------------

# 🟥 Task-5 Headers

Headers are additional bits of data you can send to the web server when making requests.

Although no headers are strictly required when making a HTTP request, you’ll find it difficult to view a website properly.

## Common Request Headers

﻿These are headers that are sent from the client (usually your browser) to the server.

Host: Some web servers host multiple websites so by providing the host headers you can tell it which one you require, otherwise you'll just receive the default website for the server.

﻿User-Agent: This is your browser software and version number, telling the web server your browser software helps it format the website properly for your browser and also some elements of HTML, JavaScript and CSS are only available in certain browsers.

﻿Content-Length: When sending data to a web server such as in a form, the content length tells the web server how much data to expect in the web request. This way the server can ensure it isn't missing any data.

﻿Accept-Encoding: Tells the web server what types of compression methods the browser supports so the data can be made smaller for transmitting over the internet.


﻿Cookie: Data sent to the server to help remember your information (see cookies task for more information).
 
## Common Response Headers

These are the headers that are returned to the client from the server after a request.

﻿Set-Cookie: Information to store which gets sent back to the web server on each request (see cookies task for more information).

﻿Cache-Control: How long to store the content of the response in the browser's cache before it requests it again.

﻿Content-Type: This tells the client what type of data is being returned, i.e., HTML, CSS, JavaScript, Images, PDF, Video, etc. Using the content-type header the browser then knows how to process the data.

﻿Content-Encoding: What method has been used to compress the data to make it smaller when sending it over the internet.

------------------------------------------------------------------------------------------------

Answer the questions below----------------------------------------------------------------------
--

### 1. What header tells the web server what browser is being used?

![image](https://user-images.githubusercontent.com/94435318/161422647-599d6a2c-0556-468b-93e5-666e900083a8.png)

### Answer: user-agent

### 2. What header tells the browser what type of data is being returned?

![image](https://user-images.githubusercontent.com/94435318/161422679-3fd3f587-a595-458a-a80a-a37f3106e01e.png)

### Answer: Content-type

### 3. What header tells the web server which website is being requested?

![image](https://user-images.githubusercontent.com/94435318/161422718-5b0d9b62-b5dd-494d-b4e7-30e77285a653.png)

### Answer: Host

-------------------------------------------------------------------------------------------

# 🟥 Task-6 Cookies

You've probably heard of cookies before, they're just a small piece of data that is stored on your computer. Cookies are saved when you receive a "Set-Cookie" header from a web server. Then every further request you make, you'll send the cookie data back to the web server. Because HTTP is stateless (doesn't keep track of your previous requests), cookies can be used to remind the web server who you are, some personal settings for the website or whether you've been to the website before. Let's take a look at this as an example HTTP request:

![image](https://user-images.githubusercontent.com/94435318/161422781-1b00a54c-c2ff-4923-9d33-25fd756f2054.png)

Cookies can be used for many purposes but are most commonly used for website authentication. The cookie value won't usually be a clear-text string where you can see the password, but a token (unique secret code that isn't easily humanly guessable).

## Viewing Your Cookies

You can easily view what cookies your browser is sending to a website by using the developer tools, in your browser. If you're not sure how to get to the developer tools in your browser, click on the "View Site" button at the top of this task for a how-to guide.

Once you have developer tools open, click on the "Network" tab. This tab will show you a list of all the resources your browser has requested. You can click on each one to receive a detailed breakdown of the request and response. If your browser sent a cookie, you will see these on the "Cookies" tab of the request.

-----------------------------------------------------------------------------------------------

Answer the questions below---------------------------------------------------------------
--

### 1. Which header is used to save cookies to your computer?

*Cookies are saved when you receive a "Set-Cookie" header from a web server. 

### Answer: Set-Cookie

---------------------------------------------------------------------------------------------


# 🟥 Task-7 Making Request

Click the "View Site" button on the right.

This is an emulator for making demo HTTP requests, using what you've learnt from the above tasks you can use it to complete the below questions.

-----------------------------------------------------------------------------------------------

Answer the questions below--------------------------------------------------------------------
--

### 1. Make a GET request to /room

![image](https://user-images.githubusercontent.com/94435318/161423307-dcd19562-15e5-4d1a-b137-bee5040ad267.png)

### Answer: THM{YOU'RE_IN_THE_ROOM}

### 2. Make a GET request to /blog and using the gear icon set the id parameter to 1 in the URL field

![image](https://user-images.githubusercontent.com/94435318/161423245-15e0aac9-eade-4ac7-9468-70eb2279534a.png)

### Answer: THM{YOU_FOUND_THE_BLOG}

### 3. Make a DELETE request to /user/1

![image](https://user-images.githubusercontent.com/94435318/161423335-5e4a2776-1773-4dcb-a430-3cf6632b15c5.png)

### Answer:  THM{USER_IS_DELETED}

### 4. Make a PUT request to /user/2 with the username parameter set to admin

![image](https://user-images.githubusercontent.com/94435318/161423454-4fc1e8bd-84c2-4aa3-8d86-a4c2efd871f2.png)

### Answer: THM{USER_HAS_UPDATED}

### 5. POST the username of thm and a password of letmein to /login

![image](https://user-images.githubusercontent.com/94435318/161423552-8b166efc-43f2-46f4-a865-2b8d9b2eed74.png)

### Answer: THM{HTTP_REQUEST_MASTER}

------------------------------------------------------------------------------------------------
