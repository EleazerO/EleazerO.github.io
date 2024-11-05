---
layout: post
tags: [Linux Fundamentals Part 3 ]
title: "Linux Fundamentals Part 3   "
permalink: /Linux-Fundamentals-Part-3
---


## Task 1 - Introduction ##

![Description of the image](noanswerneeded.png)




## Task 2 - Deploy your Linux Machine ##
![](/sshguideA.png)



## TASK 3 -  Terminal Text  Editors ##
***Nano***
Nano is a user-friendly text editor that is easy to use for creating and editing text files in the terminal. Here’s how it works:

Opening a File: To create or edit a file, you type ```nano``` filename in the terminal. Replace "filename" with the name of your file. For example, nano myfile will open (or create) a file named "myfile."

Here we see what happens when we enter nano  like this:


```
tryhackme@linux3:/tmp# nano myfile
  GNU nano 4.8                                             myfile                                                       

^G Get Help    ^O Write Out   ^W Where Is    ^K Cut Text    ^J Justify     ^C Cur Pos     M-U Undo       M-A Mark Text
^X Exit        ^R Read File   ^\ Replace     ^U Paste Text  ^T To Spell    ^_ Go To Line  M-E Redo       M-6 Copy Text
```


Now that we are in, we can write a something in to save it  
```
tryhackme@linux3:/tmp# nano myfile
  GNU nano 4.8                                             myfile                                             Modified  

Hello TryHackMe
I can write things into "myfile"


^G Get Help    ^O Write Out   ^W Where Is    ^K Cut Text    ^J Justify     ^C Cur Pos     M-U Undo       M-A Mark Text
^X Exit        ^R Read File   ^\ Replace     ^U Paste Text  ^T To Spell    ^_ Go To Line  M-E Redo       M-6 Copy Text
```







Editing Text: Once you’re in Nano, you can start typing right away. You can use the arrow keys on your keyboard to move around the text. Press "Enter" to create a new line.

Saving Your Work: When you want to save what you've written, press ```Ctrl``` + ```O``` (this means hold down the "Ctrl" key and then press "O"). After that, press "Enter" to confirm the filename.

Exiting Nano: To leave Nano, press ```Ctrl``` + ```X```. If you have unsaved changes, Nano will ask if you want to save them before exiting.

Useful Commands:

Search for text: Press ```Ctrl``` + ```W```.
Copy and paste text: ````Use Ctrl``` + ```K``` to cut text and ```Ctrl + U``` to paste it.
Jump to a specific line: Press ```Ctrl + _```, then type the line number.


***VIM***
VIM is a more advanced text editor that offers a lot of powerful features, but it has a steeper learning curve than Nano. Here are some basics:

Opening VIM: To open a file with VIM, type vim filename in the terminal, replacing "filename" with your desired file name.

Editing in VIM:

VIM starts in Normal mode, where you can't directly type text. To start editing, you need to press ```i``` to enter Insert mode. In this mode, you can type and make changes.
To return to Normal mode, press the Esc key.


Saving and Exiting:
To save your changes in Normal mode, type ```:w``` and press "Enter."
To exit VIM, type :q and press "Enter." If you want to save and exit at the same time, type :wq and press "Enter."
If you want to exit without saving changes, type :q! and press "Enter."
Additional Features: VIM has many powerful features for programming and text editing, like syntax highlighting and advanced search capabilities, but it requires more practice to learn.




## Task 4 -  General/Useful  Utilities ##


Here's a breakdown of how to use wget to download files, with the example provided:

Downloading Files with wget
The wget command is a useful tool for downloading files directly from the web via HTTP, HTTPS, or FTP protocols. This command can retrieve any file from a specified URL and save it to your local machine.

Let's walk through a simple example to understand how wget works :

```
wget https://assets.tryhackme.com/additional/linux-fundamentals/part3/myfile.txt
```



Here's a breakdown of how to use wget to download files, with the example provided:

Downloading Files with wget
The wget command is a useful tool for downloading files directly from the web via HTTP, HTTPS, or FTP protocols. This command can retrieve any file from a specified URL and save it to your local machine.

Let's walk through a simple example to understand how wget works.

Example Usage
Imagine you want to download a file called "myfile.txt" from a given URL. Using wget, you can do this easily by typing:

bash
Copy code
wget https://assets.tryhackme.com/additional/linux-fundamentals/part3/myfile.txt
Explanation of the Command
wget: The command itself. It tells your system that you want to retrieve (download) a file from the web.
https://assets.tryhackme.com/additional/linux-fundamentals/part3/myfile.txt: This is the URL of the file you want to download. You need to provide the complete URL so wget knows exactly where to find the file online.


## Task 5 -  Processes 101 ##


## Task 6 - Maintaining Your system: Package Management ##



## Task 7 - Maintain your system: Logs   ##


## Task 8 Maintain your system: Logs  ##



## Conclusions & Summaries ##
