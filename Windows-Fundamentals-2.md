---
layout: post
tags: [Windows-Fundamentals-2 ]
title: "Windows-Fundamentals 2 "
permalink: /Windows-Fundamentals-2
---

## Task 1 - Introduction ##
![ll](/windowssignin.png)

![Description of the image](noanswerneeded.png)


## Task 2 - System Configuration ##

The ***System Configuration utility***, also called MSConfig, is a tool on your computer that helps fix problems when your computer starts up. Think of it as a troubleshooting assistant—it lets you find and fix things that might be slowing your computer down or causing errors when it turns on.

You can open this tool in a few ways. One simple way is to use the Start Menu. If you need detailed instructions on how to use this tool, check out this [document](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/system-configuration-utility-troubleshoot-configuration-errors) for more information.

![kk](/systemconfiguration.png)


***Note***: You need local administrator rights to open this utility.

The utility has five tabs across the top. Below are the names for each tab. We will briefly cover each tab in this task.:

- General
- Bot
- Services
- Startup
- Tools

![xx](/systemconfiguration22.png)

In the General tab, we can select what devices and services for Windows to load upon boot. The options are: ***Normal***, ***Diagnostic***, or ***Selective***.

In the Boot tab, we can define various boot options for the Operating System.


![ss](/bootsystemconfiguration.png)

The ***Services*** tab lists all services configured for the system regardless of their state (running or stopped). A service is a special type of application that runs in the background.

![jj](/servicessystemconfiguration.png)

In the ***Startup*** tab, you won't see anything interesting in the attached VM.  Below is a screenshot of the Startup tab for MSConfig from my local machine.

![zz](/startsysgtemconfiguration.png)
As you can see, Microsoft advises using Task Manager (taskmgr) to manage (enable/disable) startup items. The System Configuration utility is NOT a startup management program.

Note: If you open Task Manager for the attached VM, you will notice that Task Manager doesn't show a Startup tab.

There is a list of various utilities (tools) in the Tools tab that we can run to configure the operating system further. There is a brief description of each tool to provide some insight into what the tool is for.

![29](/toolssystemconfiguration.png)

Notice the Selected command section. The information in this textbox will change per tool.

To run a tool, we can use the command to launch the tool via the run prompt, command prompt, or by clicking the Launch button.



***Question***<br>
What is the name of the service that lists Systems Internals as the manufacturer?

***Step 1*** search the system configuration utility  .Thats where we can find the all the services
![ff](/systemconfigsearch.png)



***Step 2***
Run as administrator on to have full access to all features.
![vv](/systemconfigo.png)


***Step 3***
If you scroll through all the services you'll see the services that lists the System internals as the manufacturer
![hh](/Psshutdown.png)

<details>
  <summary><strong>Click to see Answer</strong></summary>
  PsShutdown
</details>


***Question***<br>
Whom is the Windows license registered to?
<details>
  <summary><strong>Click to see Answer</strong></summary>
  Windows User
</details>


***Question***<br>
What is the command for Windows Troubleshooting?
***Step 1***
same as before search the system configuration utility  .Thats where we can find the all the services
![ff](/systemconfigsearch.png)



***Step 2***
Run as administrator on to have full access to all features.
![vv](/systemconfigo.png)


***Step 3***
Scroll over to tool and click on it.
![](/toolsystemconfig.png)



***Step 4***
Click on launch on the "About Windows" and you'll see "This product is licensed under the Microsoft Software License Terms to:<ANSWER>

![yum](/toolsoopenedsysconfig.png)


<details>
  <summary><strong>Click to see Answer</strong></summary>
control.exe
</details>


***Question***<br>
What command will open the Control Panel? (The answer is  the name of .exe, not the full path and research to find answer

<details>
  <summary><strong>Click to see Answer</strong></summary>
control.exe
</details>


## Task 3 Change UAC settings ##

![minus](/Changeuacsettings.png)


***Question***<br>
What is the command to open User Account Control Settings? (The answer is the name of the .exe file, not the full path and research)

<details>
  <summary><strong>Click to see Answer</strong></summary>
UserAccountControlSettings.exe
</details>


## Task 4 Change UAC settings ##


![bite](/computermanagementpanel.png)

In short In simple terms, Computer Management is a tool in Windows that helps you control and check different parts of your computer to make sure it's working properly.

If you want to:

Manage your computer's hardware:<br>
 You can see what devices (like printers or cameras) are connected and make sure their drivers are working right.

Check your hard drive:<br>
You can see how much space you have on your computer and manage things like creating new folders or partitions on your hard drive.

Look at error messages or logs:<br>
You can check for any warnings or problems that might be happening in the background.
Control running programs and services: You can stop or start background programs that help your computer run, like antivirus software or file-sharing services.
It's a tool mainly used by people who fix or manage computers, but it can also be useful for you to solve simple computer issues or get a better idea of what's going on inside your system.

Lets go over the features of the Computer Management..
![dog](/systemtoolscomputermanagement.png)
<br>
![hut](/EventViewercomputermanagement.png)

<br>
![git](/eventtypesysconfig.png)


![](/eventlogpart2.png)
![](/Windowslogu.png)
![](/EventLogsj.png)
![](/sessionexplainedui.png)
![](/systemsummaryui.png)
![](/devicemanagerh.png)
![](/serviceandapplications.png)


WMI Control is a tool that helps manage and control a feature in Windows called Windows Management Instrumentation (WMI). WMI is a system built into Windows that allows programs, scripts, and even administrators to gather information or make changes to the system.

For example, it can be used to check system performance, manage hardware settings, and track software across many computers, either locally or over a network. Think of WMI as a way for IT professionals to remotely monitor and manage multiple computers at once, without needing to physically touch each one.

Historically, there was a command-line tool called WMIC (Windows Management Instrumentation Command-line) to interact with WMI. However, as of a newer version of Windows (Windows 10, version 21H1), WMIC has been replaced by Windows PowerShell, a more advanced tool. PowerShell offers more powerful capabilities and is now the preferred way to work with WMI.


***Question***<br>
What is the command to open Computer Management (The answer is the name of the .msc file, not the full path)


<details>
  <summary><strong>Click to see Answer</strong></summary>
  Compmgmt
</details>


***Question***<br>
At what time every day is the GoogleUpdateTaskMachineUA task configured to run?

To solve this we go to the task manager, scroll on active tasks then you'll eventually see it with the time it starts.
![](/Screenshot 2024-11-29 223817.png)



<details>
  <summary><strong>Click to see Answer</strong></summary>
  6:15
</details>



***What is the name of the hidden folder that is shared?***

***Step 1***
Click on shared folders to see all the shared sharedfolderscomputermanagement
![](sharedfolderscomputermanagement.png)


***Step2***
Look through the shares and you will eventually see the hiden share.
![](Screenshot 2024-11-29 230701.png)

<details>
  <summary><strong>Click to see Answer</strong></summary>
  sh4r3dF0Ld3r
</details>


## Task 5  -  System Information ##

![](/msinfo.png)
![](/systemsummaryhardwareresources.png)
![](/componentswindows.png)
![](/softwareenviroment10.png)
![](/recallfromwindowsfundementals.png)


***Question***<br>
What is the command to open System Information (The answer is the name of the .exe file not the full path)

***Question***<br>
What is listed under System Name?
THM-WINFUN2

***Question***<br>
Under Environment Variables, what is the value for ComSpec?

## Task 6  -  Resource Monitor ##


## Task 7  -  Command Prompt ##


## Task 8  -  Registry Editor ##


## Task 9 - Conclusion ##
