---
layout: post
tags: [File inclusion]
title: "File-inclusion"
permalink: /file-inclusion
---


## TASK 1 - Introduction ##
####What is file inclusion?###
File inclusion is a type of vulnerability in web applications where an attacker tricks the website into loading or including files they shouldn’t have access to. This can lead to leaking sensitive information, exposing system files, or even taking control of the server.



How does it happen?
Websites often use parameters in URLs to load specific files. For example, if a website allows users to view documents they uploaded, it might have a URL like:
http://webapp.thm/get.php?file=userCV.pdf
Here, the file parameter tells the website to show userCV.pdf. If the website doesn’t check what file is being requested, an attacker could manipulate it to access other files, such as:
http://webapp.thm/get.php?file=/etc/passwd
(This is a file on Linux that contains usernames.)

Why is this dangerous?
Leaking sensitive information – Hackers can read important files, like passwords or configuration files.
Taking over the server – If the attacker can upload their own malicious file and include it, they might execute harmful commands and gain full control.
Types of File Inclusion:
Local File Inclusion (LFI) – Accessing files stored on the same server.
Remote File Inclusion (RFI) – Loading files from an external source, which can lead to executing malicious code.
Real-world impact
If a bank’s website had this flaw, a hacker might steal customer records or gain admin access. That’s why websites should always validate and sanitize user input to prevent this attack.



![Description of the image](noanswerneeded.png)


## Task 2 -Deploy the VM ##


Deploy the attached VM to follow and apply the technique as well as do the challenges. In order to access this VM, please make sure to connect to the TryHackMe network via OpenVPN or access it directly from the AttackBox, which can be launched by clicking the blue button on the top-right.

Please visit the link http://MACHINE_IP/, which will show you the following page:


Once you've deployed the VM, please wait a few minutes for the webserver to start, then progress to the next section!



![Description of the image](noanswerneeded.png)



## Task 3 - Path Traversal ##
What is Path Traversal?
Path traversal (or directory traversal) is a security vulnerability where an attacker tricks a website into giving them access to files they shouldn't be able to see. This happens when a website doesn’t properly check what files a user is trying to access.

How does it work?
Most websites store files in specific folders. For example, a web app might keep user files in:
/var/www/app/CVs/

A normal request to get a user’s CV might look like this:
http://webapp.thm/get.php?file=userCV.pdf

But if the website doesn't check input properly, an attacker can manipulate the request to move up in the directory structure. They do this by using ../ (dot-dot-slash), which tells the system to go up one folder.

For example, instead of:
http://webapp.thm/get.php?file=userCV.pdf

The attacker could send:
http://webapp.thm/get.php?file=../../../../etc/passwd

This tells the system:

Go up multiple directories until it reaches the root /.
Go into the /etc/ directory (where Linux stores system information).
Open the passwd file, which contains usernames.
If the website doesn’t block this, it could leak important system files, configuration details, or even passwords.

Windows Example
The same technique works on Windows, but with different file paths. Instead of /etc/passwd, an attacker might try:
http://webapp.thm/get.php?file=../../../../boot.ini
This would attempt to access system boot configuration settings.

Why is this dangerous?
Leaking sensitive system files – Attackers can view configuration files, usernames, or even password-related files.
Exposing logs and history – They might check user command history or web server logs for more weaknesses.
Gaining deeper access – If attackers find SSH keys or authentication files, they can escalate privileges and take over the server.
How to prevent it?
Validate input – Only allow access to specific directories.
Use absolute file paths – Don’t rely on user input for file locations.
Restrict special characters – Block ../ in user input.
Run applications with limited permissions – Even if an attacker finds a way in, they shouldn’t have access to critical files.
Real-World Impact
If a bank’s website had this vulnerability, an attacker could steal customer data, view system logs, or even find admin credentials. This is why developers must properly validate and filter user input.
