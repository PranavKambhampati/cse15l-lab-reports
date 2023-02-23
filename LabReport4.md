# Week 7 Lab Report: CSE Labs Done Quick

##### Initial Setup:
Before doing anything, I set up an ssh key on my IENG 6 machine so that it would be easy to login (without having to type in my password everytime).
I also connected by IENG6 machine to my github account via SSH so that I don't have to provide autentication.

### Step 1: Delete existing forks of the repository

![image](https://user-images.githubusercontent.com/70964947/220807769-01b7721f-2a5b-40d3-901e-ddb06e44267e.png)
![image](https://user-images.githubusercontent.com/70964947/220807821-a4ff5c94-ba5f-487b-b4d3-70df8bd2b06c.png)

```
//Command Ran:
rm -r lab7
```

### Step 2: Fork the repository

Forked the lab7 repository on my GitHub account through Microsoft Edge.
Navigated to lab7 link on lab write up and hit "fork" on the top right corner.
This created a copy of the repository for me to use, without any changes I make to my copy affecting the main lab7 repository.

### Step 3: Start the timer

N/A

### Step 4: Log into ieng6

![image](https://user-images.githubusercontent.com/70964947/220808583-d0737da4-d7c3-4278-aa95-b4805a5df0de.png)

```
//Command ran:
ssh cs15lwi23alz@ieng6.ucsd.edu
```
The ssh key I saved beforehand allowed me to log in without me having to put in my password (also seen in the picture).

### Step 5: Clone fork of the github repo

![image](https://user-images.githubusercontent.com/70964947/220808853-7015e289-aa87-4e91-adbe-c867c9cbdd5a.png)

I copied the ssh link of the lab7 repo that I forked and went back to the terminal and ran this command:
```
//Command ran
git clone git@github.com:PranavKambhampati/lab7.git
```

### Step 6: Run Tests, demoing that they fail

![image](https://user-images.githubusercontent.com/70964947/220811920-56b7b763-8421-4f03-8a57-7d3e9d3b83a0.png)

```
//Commands ran:
javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java
java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore TestListExamples
```
However, I already had both these commands in my history, so I just had to use the up arrow a few times (6 times specifically) to actually run them.

### Step 7: Edit code to fix failing test



![image](https://user-images.githubusercontent.com/70964947/220807821-a4ff5c94-ba5f-487b-b4d3-70df8bd2b06c.png)
