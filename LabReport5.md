# Week 9 Lab Report: Revisiting Old Lab Report

I'm choosing to revisit LabReport 3. Previously, I explored the 'less' command, now I would like to explore the 'grep' command and how we can use
the alternate 'grep' commands to perform various tasks.

The 'grep' command by itself can be used to look for keywords in a file. The general syntax is that we provide the keyword we're looking for follwed by
the file we're looking in.

```
//Example:
grep keyword file.txt
```

### Searching for words by ignoring case

Reference Used: [How To Geek Reference](https://www.howtogeek.com/496056/how-to-use-the-grep-command-on-linux/)

The '-i' parameter can be passed into a grep command to help us look for a keyword by ignoring its case. The output is a display of the line contaning
the keyword.

```
//Input
grep -i INDULGING ch1.txt
```

OUTPUT:
![image](https://user-images.githubusercontent.com/70964947/223900958-0865efa0-2bb4-4ea1-8cd9-ef788c3d6ce7.png)

Even though I used all uppercase letters in the command, the final result was the sentence containing the word in all lowercase letters. This is because
grep ignored the case while searching for the word.

```
//Input
grep -i Sermon ch1.txt
```

OUTPUT:
![image](https://user-images.githubusercontent.com/70964947/223901252-395a496e-0488-4c79-baa2-978c6ba070d0.png)

In this case, the sentence with the word "Sermon" was the output, the -i didn't really make a difference here because the word was written exactly the 
same in the text file.

