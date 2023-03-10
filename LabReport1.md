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

``` cd ``` will change the current working directory to whatever directory is mentioned after the cd. Note: .. will go back a directory. Additiionally, the tilda symbol (~) represents the home directory, which is where all of the users files are stored.

``` ls ``` will list out all the files and folders in the current working directory. This is helpful if we don't know what our current directory contains.

``` pwd ``` will print out what the current working directory is. This is helpful if we don't know what directory we're located in after cd'ing.

``` mkdir ``` will make a directory at the provided path location. This is helpful if a specific file doesn't exist.

``` cp ``` will copy one or multiple files that can be put elsewhere.

This is what the terminal looks like when some of these commands are being run:
<img width="594" alt="image" src="https://user-images.githubusercontent.com/70964947/211932560-6b95c446-6604-4c6b-8374-c23484085836.png">

Finally, to log out of the remote desktop, the ``` exit ``` command can be run. This will return you back to your own desktop.
