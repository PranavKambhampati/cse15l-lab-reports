# Week 1 Lab Report: VSCode, Remotely Connecting and Terminal Commands

#### Setting up VSCode
To set up VSCode, first install the application from [VSCode's Website](https://code.visualstudio.com/).
Because my computer already had VSCode on it from using it for CSE 11, I was able to skip the installation step.
After installing the application, open up the terminal (located at the bottom of the window) in order to connect to a server in the CSE Basement.

This is what the VSCode application looks like:

<img width="672" alt="image" src="https://user-images.githubusercontent.com/70964947/211930459-d799d4e0-7532-4748-b687-9b753bcf81f8.png">
The terminal section is located at the bottom of the applciation window.

#### Remotely Connecting using SSH
Before being able to remotely connect to a server in the CSE Basement, I had to reset my password on [this website](https://sdacs.ucsd.edu/~icc/index.php).
After resetting my password, I was ready to remotely connect to a server using the terminal window on VSCode.

First I ran the command to initialize the connection to a CSE Basement computer through SSH:
```
$ ssh cs15lwi23alz@ieng6.ucsd.edu
```
It then asks me for my accounts password. This is the same password that I reset it to through the UCSD Educational Technology Services website.
An important thing to note here is that while I was typing my password, the actual characters don't show up. I just had to press the return key after typing in all characters of my password.

Upon typing my password correctly, the system asked me to authorize the connection by typing in a "yes" and my password again. This completed the connection process and this is the resulting information that showed up: 
<img width="459" alt="image" src="https://user-images.githubusercontent.com/70964947/211930153-9ff212a6-6ae4-4f6c-b411-819a4fbd5653.png">

#### Terminal Commands
Here are some terminal commands that can be run in order to understand the file structure of either the client computer or the server.
```
cd
``` 
will change the work directory to whatever is specified after the command.
