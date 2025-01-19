---
layout: post
tags: []
title: "Principles of Security"
permalink: /principles-of-security
---


## Task 1 - Introduction ##

No answer or info needed lets proceed.


![Description of the image](noanswerneeded.png)



## Task 2 - The CIA Triad ##
![](/CIATRIAD.png)

The CIA triad is a simple way to think about protecting information. It stands for Confidentiality, Integrity, and Availability—three big ideas that help keep information safe.

***Confidentiality***: This means keeping secrets safe. For example, only the right people should see private files, like your bank details or personal photos.

***Integrity***: This means making sure information is accurate and hasn’t been changed by accident or on purpose. For example, if someone sends money, the amount shouldn’t be changed halfway through.

***Availability***: This means the information should be easy to access when it’s needed. For example, you should be able to log into your email or access your files without long delays.

The CIA triad is used because businesses need to protect their important data. It helps them figure out what’s valuable and how to keep it safe, whether it’s stored on a computer, written on paper, or in some other form. It’s like a guide to make sure information is handled properly and stays secure.


***Question***<br>
What element of the CIA triad ensures that data cannot be altered by ***unauthorised*** people?

<details>
  <summary><strong>Click to see Answer</strong></summary>
  Integrity
</details>


***Question***<br>
What element of the CIA triad ensures that data is available?

<details>
  <summary><strong>Click to see Answer</strong></summary>
  Availability
</details>


***Question***<br>
What element of the CIA triad ensures that data is only accessed by ***authorised*** people?

<details>
  <summary><strong>Click to see Answer</strong></summary>
  Confidentiality
</details>



## Task 3 - Principles of Privileges ##

Managing who can access an organization's IT systems is really important. It ensures that people can only see or do what they need to for their job, and nothing more.

Access is decided based on two things:

What the person does at work (their role or function).
How sensitive the information is (how much protection it needs).
There are two main tools to help with this:

***Privileged Identity Management (PIM)***: This matches a person's job role to the right access level on a system.<br>
***Privileged Access Management (PAM)***: This handles what those access levels can do and includes extra security measures like managing passwords and keeping track of who does what.
Though PIM and PAM sound similar, they have different jobs. PIM decides who gets access. PAM controls what that access allows and keeps everything secure.

A key rule here is the principle of least privilege. This means people should only get the bare minimum access they need to do their work—no more, no less. This limits risks and helps others trust the system.

PAM does more than just decide access levels. It also:

Enforces strong password rules.
Audits activity to track changes and actions.
Reduces system vulnerabilities by limiting unnecessary permissions.
This keeps systems safe and helps prevent misuse or attacks.


***Question***<br>
What does the acronym "PIM" stand for?



<details>
  <summary><strong>Click to see Answer</strong></summary>
  Privileged Identity Management
</details>


***Question***<br>
What does the acronym "PAM" stand for?



<details>
  <summary><strong>Click to see Answer</strong></summary>
Privileged Access Management
</details>



***Question***<br>
If you wanted to manage the privileges a system access role had, what methodology would you use?<br>
(hint:I'm looking for the short acronym here (PIM/PAM))


<details>
  <summary><strong>Click to see Answer</strong></summary>
PAM
</details>




## Task 4 - Security Models Continued ##
Any technology or device that stores information is called an information system. Let's look at a well-known way to keep information safe by focusing on one part of the CIA triad: confidentiality (keeping information private).


![](/BELLMODEL.png)
<br>
***The Bell-LaPadula*** Model<br>
This model is all about making sure that information stays confidential, meaning only the right people can see or use it. It assumes that the organization has a clear structure where everyone knows their job and level of responsibility.

Here’s how it works:

People are only given access to the information they need to know for their job.
It follows a simple rule:<br>
<br>"No write down": You can’t save information to a lower security level (to stop leaking secrets).
<br>"No read up": You can’t look at information above your security level (to stop snooping).<br>
This keeps information safe by limiting access to exactly what’s necessary and preventing both accidental and intentional misuse.

The Bell-LaPadula Model is often used in organizations like governments and the military. Why? Because people in these organizations are usually vetted before they join.

Vetting is a background check that looks into someone's history to see if they might be a risk. If someone passes vetting, they’re considered trustworthy.

This is where the Bell-LaPadula Model fits perfectly:

It assumes the people using the system can be trusted because they’ve already been checked.
The model then limits their access to only the information they need for their job, using strict rules like "no write down" and "no read up."
By combining vetting with these rules, sensitive information stays safe, and risks are minimized.


![](/BIBAMODEL.png)
***The Biba model***<br>
The Biba model is a way of ensuring data integrity, meaning it helps prevent data from being accidentally or intentionally corrupted. It’s like a rule for who can make changes to data and who can view it.



Subjects are users or programs (like you or a computer application).
Objects are the data or files (like documents or databases).
The key rule of the Biba model is "***no write up, no read down***". Here’s what it means:

No write up: A user or program can only modify (write to) data that is at their level or lower. They can't make changes to data that’s more important or secure than they are. For example, a regular employee cannot change sensitive data in a top-secret file.

No read down: A user or program can only read data that is at their level or higher. They cannot access or read data that’s less important than what they are allowed to access. For instance, a high-level manager can read a general document, but they cannot read a document meant only for lower-level employees.

In short, the Biba model is like setting up a hierarchy of permissions where people can only influence or access data at their level or below, but they can only read data above their level to make sure higher-level information stays safe and unaltered.


***Question***<br>
What is the name of the model that uses the rule "can't read up, can read down"?
<details>
  <summary><strong>Click to see Answer</strong></summary>
  The Bell-LaPadula Model
</details>


***Question***<br>
What is the name of the model that uses the rule "can't read up, can read down"?

<details>
  <summary><strong>Click to see Answer</strong></summary>
  The Bell-LaPadula Model
</details>


***Question***<br>
What is the name of the model that uses the rule "can read up, can't read down"?

<details>
  <summary><strong>Click to see Answer</strong></summary>
  The Bell-LaPadula Model
</details>

***Question***<br>
If you were a military, what security model would you use?
<details>
  <summary><strong>Click to see Answer</strong></summary>
  The Biba Model
</details>



***Question***<br>
If you were a software developer, what security model would the company perhaps use?
<details>
  <summary><strong>Click to see Answer</strong></summary>
  The Biba Model
</details>



## Task 5 - Threat Modelling & Incident Response  ##

Threat modelling is like planning a security system for your house but for your organization’s technology. It’s about figuring out what might go wrong, what’s weak, and how to protect it better. This process isn’t a one-time thing—it needs regular updates and teamwork.

Just like workplaces do risk assessments for their employees’ safety, threat modelling follows these four basic steps:

***Preparation*** – Get ready by understanding what needs protection.

***Identification*** – Spot the risks and weak spots.
Mitigations – Decide on ways to fix or reduce those risks.

***Review*** – Check back often to make sure everything still works as planned.
To create a strong threat model, you’ll need to include:

***Threat intelligence*** – Research on potential dangers (like burglars targeting houses, but for IT systems).
Asset identification – Know what’s valuable (like doors, windows, or cash, but in IT terms, it’s data, apps, or devices).
Mitigation capabilities – Tools and processes to protect what matters.

***Risk assessment*** – Figuring out how likely something bad is and how bad it would be.
There are frameworks to make this easier, like STRIDE and PASTA. Let’s break down STRIDE (created in 1999 by Microsoft researchers) into its six areas:

***Spoofing identity*** – Someone pretending to be someone else, like a fake ID.
Tampering with data – Messing with your stuff, like rewriting a note you left.

***Repudiation threats*** – Denying actions, like saying, “It wasn’t me!” even if it was.
Information disclosure – Spilling secrets, like reading someone’s private letter.

***Denial of Service (DoS)*** – Blocking access, like locking the front door so no one can get in.


***Elevation of privilege*** – A lower-level worker sneaking into the manager’s office to access sensitive files.

Threat modelling is crucial because it helps organizations stay ahead of potential problems, just like securing your house against burglars before they try to break in. Frameworks like STRIDE make the process structured and easier to understand!

![](/incidentresponsechart.png)

When something goes wrong with a company’s security—like a hacker breaking in or a virus spreading—it’s called a ***security incident***. No matter how strong the defenses are, these incidents can still happen. Fixing and dealing with these problems is known as Incident Response (IR), which is an important job in cybersecurity.

Understanding Incidents
Urgency: How quickly do we need to act? This depends on the type of attack, like a burglar breaking in (urgent!) versus someone trying to pick the lock (less urgent).

Impact: How bad is it? This depends on what’s affected—if the incident crashes a critical system, it can cause serious problems for business operations.
Who Handles It?

When an incident happens, it’s addressed by a special team called the Computer Security Incident Response Team (CSIRT). This team is like a SWAT team for cybersecurity. They’re already trained and ready to handle emergencies because they know the systems and the potential problems inside out.

The Six Phases of Incident Response
Think of these like steps to handle a fire in a building, but for computer systems:

Preparation: Just like having fire drills, the team plans ahead, gets tools ready, and practices for potential incidents.<br>

Identification: Spot the problem—figure out where the fire is and what caused it.<br>
Containment: Stop it from spreading, like closing doors to prevent a fire from engulfing the whole building.<br>

Eradication: Put out the fire completely—remove the virus or block the hacker.<br>
Recovery: Fix the damage, like repairing the burned parts of the building, and get everything running smoothly again.<br>

Lessons Learned: After the incident, the team reviews what happened, what worked, and what didn’t, like improving fire safety rules for the future.<br>
Incident Response ensures that when a cyberattack happens, it’s handled quickly and with minimal damage, just like firefighters putting out a blaze and preventing future ones!



***Question***<br>
What model outlines "Spoofing"?
<details>
  <summary><strong>Click to see Answer</strong></summary>
  STRIDE
</details>




***Question***<br>
What does the acronym "IR" stand for?
<details>
  <summary><strong>Click to see Answer</strong></summary>
Incident Response
</details>

***Question***<br>
You are tasked with adding some measures to an application to improve the integrity of data, what STRIDE principle is this?

<details>
  <summary><strong>Click to see Answer</strong></summary>
Tampering
</details>


***Question***
An attacker has penetrated your organisation's security and stolen data. It is your task to return the organisation to business as usual. What incident response stage is this?

<details>
  <summary><strong>Click to see Answer</strong></summary>
Recovery
</details>


This blog post explores the foundational principles of security in information systems, focusing on key frameworks, methodologies, and processes for safeguarding data.

1. CIA Triad
The CIA Triad forms the backbone of information security, emphasizing:

Confidentiality: Ensuring only authorized users access data.
Integrity: Keeping data accurate and unaltered.
Availability: Making data accessible when needed.
These principles guide organizations in protecting critical information.

2. Principles of Privileges
Managing access is vital to system security, relying on tools like:

Privileged Identity Management (PIM): Assigns access based on job roles.
Privileged Access Management (PAM): Controls and secures what those roles can do.
The principle of least privilege minimizes risks by granting only the necessary access.

3. Security Models
Two major models discussed:

Bell-LaPadula Model: Focuses on confidentiality with rules like "no write down, no read up" to prevent data leaks.
Biba Model: Ensures data integrity with "no write up, no read down" to avoid data corruption.
These models are applied in sectors like military (Bell-LaPadula) or software development (Biba).

4. Threat Modelling
Threat modelling is proactive risk management, helping organizations identify vulnerabilities and improve defenses. Steps include:

Preparation: Understand assets and risks.
Identification: Spot potential threats.
Mitigation: Implement protections.
Review: Regularly assess security measures.
Frameworks like STRIDE (addressing threats like spoofing, tampering, and DoS) simplify the process.

5. Incident Response
Despite robust security measures, incidents (e.g., breaches) happen. The Incident Response (IR) process ensures swift containment and recovery through six phases:

Preparation
Identification
Containment
Eradication
Recovery
Lessons Learned
The Computer Security Incident Response Team (CSIRT) is responsible for executing this structured approach.

This post highlights how principles, models, and processes collectively maintain and enhance security in IT systems.
