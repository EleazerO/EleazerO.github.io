```markdown




---
layout: post
tags: []
title: "HTTP in Detail"
permalink: /HTTP-in-Detail
---


### Task 1 - What is HTTPS(S) ##

HTTP (Hypertext Transfer Protocol) is the standard protocol for viewing and interacting with web pages. However, it is not secure, meaning that the data transmitted between the user's browser and the website server is not encrypted. This can make the data vulnerable to interception by third parties (such as hackers).

**HTTPS (Hypertext Transfer Protocol Secure)** is the secure version of HTTP. It uses encryption (usually via SSL/TLS) to protect the data being transmitted between the user's browser and the server. This encryption ensures that third parties cannot easily intercept or view the data.

**Question**<br>
What does HTTP stand for?


<details>
  <summary><strong>Click to see Answer</strong></summary>
    Hypertext Transfer Protocol
</details>
<br>
<br>


**Question**<br>
What does the S in HTTPS stand for?
<details>
  <summary><strong>Click to see Answer</strong></summary>
    Secure
</details>
<br>
<br>


**Question**<br>
On the mock webpage on the right there is an issue, once you've found it, click on it. What is the challenge flag?

If you go on the site you see a cancelled padlock indicating its not secure. Click on it  

![http](/httpnotsecure.png)


<details>
  <summary><strong>Click to see Answer</strong></summary>
    THM{INVALID_HTTP_CERT}
</details>




## Task 2- Requests And Responses ##


![uniform](/uniformresourcerloader.png)

A URL (Uniform Resource Locator) is like the address you type into your browser to go to a specific webpage or resource on the internet. It tells your computer where to find what you’re looking for and how to get there.

Let’s break it down:

**Scheme** (http): This tells your browser what method to use to get the data, like HTTP (for regular websites) or HTTPS (for secure websites).

**User (user)**: Sometimes, if a website requires you to log in, you can include your username and password in the URL (though this is rare and not very secure).

**Host** (tryhackme.com): This is the website’s address, like "www.google.com."

**Port (80)**: Think of a port like a specific door on the website’s server that your browser knocks on. Usually, for websites, the common ports are 80 for HTTP and 443 for HTTPS.

**Path (/view-room):** This is like a folder or page on the website you want to access.
**Query String (?id=1):** This is extra info sent to the website to get specific data. For example, it might tell a blog to show the post with ID number 1.


**Fragment (#task3):** This is like jumping to a specific section of a page, making it so you start at a certain part when the page loads.
GET / HTTP/1.1:

This is the browser asking for the homepage (represented by "/").
"GET" is the method used to request the page.

"**HTTP/1.1**" is the version of the protocol the browser is using to communicate with the server.
Host: tryhackme.com:

This tells the server that we are trying to access the website "tryhackme.com."
User-Agent: Mozilla/5.0 Firefox/87.0:

This informs the server that the request is coming from the Firefox browser, version 87.

Referer: **https://tryhackme.com**:This tells the server that we came from another page on the same website, "https://tryhackme.com."

Blank Line: Every HTTP request ends with a blank line to indicate that the request has been completed.
In short, the request is asking the server for the homepage of "tryhackme.com," while also providing details about the browser used and the previous page visited.
In simple terms, the URL is the address that helps guide you to exactly what you want to see on the internet.


## **Making a request** ##

![makingarequest](/makingarequest.png)

Example Request:
```
GET / HTTP/1.1
Host: tryhackme.com
User-Agent: Mozilla/5.0 Firefox/87.0
Referrer: https://tryhackme.com/

```
Line 1 (GET / HTTP/1.1): This is saying, "I want to view the home page of this website." The "GET" is the action (just looking), the / refers to the home page, and "HTTP/1.1" is the version of the communication method used (like a language version).

Line 2 (Host: tryhackme.com): This tells the server which website you want to access, in this case, "tryhackme.com."

Line 3 (User-Agent: Mozilla/5.0 Firefox/87.0): This tells the server what browser you are using—here, it's Firefox version 87. The server uses this info to give you a version of the site that works well with your browser.

Line 4 (Referer: https://tryhackme.com/): This lets the server know what website you were on before making this request, which in this case is also "tryhackme.com." It’s like saying, "I clicked a link from this page."

Line 5 (Blank Line): This empty line is like saying, "That's all for my request!" It signals to the server that the request is complete and ready for a response.

Example Response:
```

HTTP/1.1 200 OK
Server: nginx/1.15.8
Date: Fri, 09 Apr 2021 13:34:03 GMT<br>
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

```

Line 1 (HTTP 1.1 200 OK): This tells you the server is using HTTP version 1.1 to talk back to your browser. The "200 OK" means the request was successful—like saying, "Everything worked!"

Line 2 (Server Info): This is the server telling you what software and version it’s using. It’s like saying, "I’m running on this software version."

Line 3 (Date and Time): This tells you the exact date and time when the server sent this response. It helps both sides track when the communication happened.

Line 4 (Content-Type): This tells your browser what kind of content it’s about to receive, like saying, "I’m sending you a webpage" or "I’m sending you an image."

Line 5 (Content-Length): This is the server letting you know how big the response is. It’s like saying, "The response is this many bytes long" to make sure everything gets sent correctly.

Line 6 (Blank Line): Just like in the request, this blank line is the server’s way of saying, "That’s it, I’m done!" The response is complete.

Lines 7-14 (Requested Data): These lines contain the actual content you requested, like the homepage of the site. This is where the server delivers what you asked for, whether it’s a webpage, an image, or some other file.




**Question**

What HTTP protocol is being used in the above example?

<details>
  <summary><strong>Click to see Answer</strong></summary>
    HTTP/1.1
</details>


<br>
<br>


**Question**
What response header tells the browser how much data to expect?

<details>
  <summary><strong>Click to see Answer</strong></summary>
    Content-Length
</details>


## Task 3- HTTP Methods ##
HTTP methods are like instructions that tell a web server what you want to do with the data.

**GET**: You are asking the server for some information, like asking a librarian for a book. You just want to see it but not change anything.

**POST**: You are sending new information to the server, like filling out a form and submitting it. This might create something new, like a new user account.

**PUT**: You are updating something that already exists on the server, like correcting a typo in your online profile.

**DELETE**: You are telling the server to remove something, like asking to delete an old account or a file you don’t need anymore.



**Question**
What method would be used to create a new user account?

<details>
  <summary><strong>Click to see Answer</strong></summary>
    POST
</details>

<br>
<br>

**Question**
What method would be used to update your email address?

<details>
  <summary><strong>Click to see Answer</strong></summary>
    PUT
</details>

<br>
<br>


**Question**
What method would be used to remove a picture you've uploaded to your account?

<details>
  <summary><strong>Click to see Answer</strong></summary>
    PUT
</details>

<br>
<br>


**Question**
What method would be used to remove a picture you've uploaded to your account?

<details>
  <summary><strong>Click to see Answer</strong></summary>
    PUT
</details>

<br>
<br>

**Question**
What method would be used to remove a picture you've uploaded to your account?

<details>
  <summary><strong>Click to see Answer</strong></summary>
   DELETE
</details>

<br>
<br>


**Question**
What method would be used to view a news article?

<details>
  <summary><strong>Click to see Answer</strong></summary>
   GET
</details>

<br>
<br>


## Task 4 - HTTP status codes ##


## Task 5 - HTTP headers ##

## Task 6 - HTTP cookies ##


## Task 7- HTTP making requests  ##
