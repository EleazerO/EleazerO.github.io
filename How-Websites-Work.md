---
layout: post
tags: [Websites]
title: "How the Web works"
permalink: /How-Websites-Work
---

## Task 1 - How websites work ##
![howtheweb](/howthewebworks.png)

When you visit a website, your browser (like Safari or Google Chrome) sends a request to another computer called a web server, which is located somewhere else in the world. This web server's job is to respond to your request by sending back the information your browser needs to show you the page.

For example, if you type in "example.com," your browser asks the server for the details of that webpage. The server sends back all the information (like text, images, and code), and your browser uses this to display the page on your screen.

In short, your browser asks for the page, the web server gives it, and then your browser shows it to you.

The 2 main parts that make a website:

Front End and Back End

Front End (Client-Side): This is what you see and interact with when you visit a website. It's the design, buttons, images, and text that appear on your screen. Your browser (like Chrome, Firefox, etc.) is responsible for displaying all of this in a way that looks nice and is easy to use. Think of it as the "face" of the website.

Back End (Server-Side): This is like the "brain" of the website that you don't see. It's a server (a powerful computer) that stores the website's information and handles any requests you make. When you click a link or fill out a form, your browser sends a request to the server. The server processes this request, gathers the necessary data (like pulling information from a database), and sends it back to your browser, which then shows it to you on the front end.






***Question***<br>
What term best describes the component of a web application rendered by your browser?


<details>
  <summary><strong>Click to see Answer</strong></summary>
    Front End
</details>

## Task 2 - HTML  ##

***HTML (Hypertext Markup Language)***: This is like the foundation of a website. It tells the browser what content to show and how it's organized. HTML uses things called "tags" (like <h1>, <p>, etc.) to structure text, images, links, and other content. Think of it as the skeleton of a webpage.

***CSS (Cascading Style Sheets):*** This is what makes the website look good. It controls the colours, fonts, layout, and overall style of the webpage. CSS works on top of HTML to "decorate" the content, making it visually appealing.

***JavaScript:*** This adds interactivity and makes the website more dynamic. It can do things like create buttons that respond when clicked or update content without reloading the whole page. JavaScript makes the site come to life and respond to user actions.

Here's a basic breakdown:

***HTML*** creates the structure.
<br>
***CSS*** styles and beautifies the page.
<br>
***JavaScript*** adds functionality and interactivity.

Every website uses these tools to give users both content and a good experience.



Hypertext Markup Language (HTML) is the language websites are written in. Elements (also known as tags) are the building blocks of HTML pages and tells the browser how to display content. The code snippet below shows a simple HTML document, the structure of which is the same for every website



***HTML Structure*** This is like the blueprint or skeleton of a website, which tells the browser what to show on a webpage.
![](/HTMLlanguage.png)


***Features of HTML***

```<!DOCTYPE html>``` This is just a signal to the browser that the page is written using HTML5, the latest version. It helps ensure everything is displayed properly.

```<html>``` element. This is the main container for everything on the webpage. All the other parts of the webpage will be placed inside this.

```<head>``` element. This part contains important information about the webpage, like its title (what you see in the browser tab), but it doesn’t show directly on the page itself.

```<body>``` element. This is the part of the webpage that users actually see and interact with. It contains the content like text, images, buttons, and other visible elements.






```<h1>``` element.  This is a heading tag, like the title of a section. It is usually displayed big and bold.

```<p>``` This stands for "paragraph" and is used for regular blocks of text.

Other elements/tags: There are many other types of tags used to create different things on a webpage.
such as

```<button>``` To create clickable buttons.

```<img>``` To show images.


HTML tags (which define elements like paragraphs or images on a webpage) can have extra details called  ***attributes*** that give instructions to the browser on how to display or handle them.

For example:

The class attribute, like in ```<p class="bold-text">```, allows you to style a group of elements in a similar way, such as changing the color or size of the text. Basically everything enclosed in it will be bold in this case

The src attribute in an image tag (```<img src="img/cat.jpg>```) tells the browser where to find the image file to display.


You can add multiple attributes to an element, each with a specific role. For example:

```<p attribute1="value1" attribute2="value2">```

Here, the element <p> has two different attributes with their own purposes.

There's also an id attribute, like <p id="example">. Each element's id must be unique on the page, so you can identify it separately. It's like giving each element a unique name tag that can be used to style it or interact with it in JavaScript.

Finally, if you're curious about how a webpage is built, you can right-click anywhere on the page and choose "View Page Source" to see its HTML code.

This is the basic foundation of how websites are built and structured!


***Question***<br>
Let's play with some HTML! First click the "View Site" button inside this task. On the right-hand side, you should see a box that renders HTML - If you enter some HTML into the box and click the green "Render HTML Code" button, it will render your HTML on the page; you should see an image of some ca

NO ANSWER NEEDED.

***Question***<br>
One of the images on the cat website is broken - fix it, and the image will reveal the hidden text answer!

The problem here was that the file format was not specified like the first image scripted.
The image should be rendered and the text wil be revealed in the image.
![ww](/fixedhtmlcode.png)
<details>
  <summary><strong>Click to see Answer</strong></summary>
  HTMLHERO
</details>

<br>
<br>

***Question***<br>
Add a dog image to the page by adding another img tag (<img>) on line 11. The dog image location is img/dog-1.png. What is the text in the dog image?

All you have to do this time is create source path and saying its location is img/dog-1.png as shown as below. If done correctly the image will be shown as previously and will show text
![dd](/srcimagepathhtml.png)

<details>
  <summary><strong>Click to see Answer</strong></summary>
  DOGHTML
</details>



## Task 3 - JavaScript ##

JavaScript (JS) is like the magic that makes websites interactive and dynamic. While HTML gives structure and content to a webpage (like text, images, and buttons), JavaScript is what allows the page to do things when you interact with it, like changing a button color when you click it or showing a pop-up.
