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

![image](https://user-images.githubusercontent.com/70964947/220812342-47b22707-80bf-4d67-a05d-010d8f54cab3.png)

```
//Commands ran:
javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java
java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore TestListExamples
```
However, I already had both these commands in my history, so I just had to use the ```<up arrow>``` a few times (6 times specifically) to actually run them.

### Step 7: Edit code to fix failing test
Code fix:
![image](https://user-images.githubusercontent.com/70964947/220812421-da2254cf-6d9c-4872-8fb3-b2810b22a970.png)

To fix the code I had to change the index1 += 1 to index2 +=1
```
//Commands ran:
nano ListExamples.java
//Code edit made
^O
^X
```
To actually get to the right point in the file, I had to press the <down arrow key> about 42 times and the <right arrow key> about 10 times

### Step 8: Run tests, demoing that they succeed

![image](https://user-images.githubusercontent.com/70964947/220812956-0352eeaa-aebc-45f7-8311-ae490268fd9a.png)

```
//Commands ran:
javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java
java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore TestListExamples
```
I already had the commands in my history (from a previous step), so I just had to hit the <up arrow> 3 times for each command and I was then able to hit <enter> to run the commands.

### Step 9: Commit and Push

![image](https://user-images.githubusercontent.com/70964947/220813364-d065ed88-4dd9-4d91-8a98-54cdbed546bc.png)

```
//Commands ran:
git add ListExamples.java
git commit -m "Latest Update"
git push
```
These commands add the ListExamples file to the latest commit, commits the file with a message and pushes the commit up to GitHub.
Upon checking the repo, it is up to date with all the commits.
