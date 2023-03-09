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

The '-i' parameter is really helpful because it helps us search for words even when we don't know how they're written.


### Recursive searches with grep

Reference Used: [How To Geek Reference](https://www.howtogeek.com/496056/how-to-use-the-grep-command-on-linux/)

The '-r' parameter can be used to recursively search for a keyword through a folders subdirectories, not just in the current file.
The output would be a file path with the sentence containing the keyword.

```
//Input (after cd'ing to a parent folder about 3 levels up)
grep -r -i Sermon .
```

OUTPUT:
![image](https://user-images.githubusercontent.com/70964947/223902051-32bfa9d0-d268-4f36-beb8-bd63cbd4c350.png)

Note: the . in the input command tells grep to look in the current directory

```
//Input (after cd'ing to a parent folder about 3 levels up)
grep -r -i ATONEMENT .
```

OUTPUT:
![image](https://user-images.githubusercontent.com/70964947/223902409-1ba55186-b896-40a1-aea1-85be765ee3db.png)

In both cases, the 'grep -r -i' command was used to recursively look for a keyword in the current subdirectories. Because we used the '-i' option in
conjunction to the '-r' option, the grep was case insensitive while looking for the keyword, as demonstrated in Example 2.

The '-r' command is really helpful because if we don't know where the keyword is located (file-wise), we can simply navigate to a parent directory
and look for the keyword recursively, making it a lot easier to find something.


### Using grep with multiple search terms

Reference Used: [How To Geek Reference](https://www.howtogeek.com/496056/how-to-use-the-grep-command-on-linux/)

The grep parameter '-E' can also be used to search for multiple terms at once, as demonstrated below.

```
//Input
grep -E -i "civilized|proceed" ch1.txt
```

OUTPUT:
![image](https://user-images.githubusercontent.com/70964947/223903427-513c842e-bef3-4cba-99c3-44fb390cf817.png)

The sentences containing each corresponding word are displayed (civilized and proceed).

```
//Input
grep -E -i "ATONEMENT|blahblahblah" ch1.txt
```

OUTPUT:
![image](https://user-images.githubusercontent.com/70964947/223903710-e6849806-ae10-4bc8-a38e-e4a23f51734c.png)

In this case, only the sentence containing atonement was printed since the second keyword wasn't found in the file. Since we used the '-t' parameter,
even though we typed the keyword into the command in all caps, grep was still able to find the right word since '-i' makes it case insensitive.

### Use grep to only display matching text

Reference Used: [How To Geek Reference](https://www.howtogeek.com/496056/how-to-use-the-grep-command-on-linux/)

The '-o' alternative can be used to simply display the matching word instead of printing out the entire sentence. Here are some examples:

```
//Input
grep -o -i ATONEMENT ch1.txt
```

OUTPUT:
![image](https://user-images.githubusercontent.com/70964947/223906502-fb8a4dd1-c6d4-4b60-85e6-7a313fb2d08d.png)

```
//Input
grep -o The ch1.txt
```

OUTPUT:
![image](https://user-images.githubusercontent.com/70964947/223906687-9b9d06aa-682f-4786-ac33-c8f0f8753aba.png)

In both cases, by using the '-o' command, only the keyword was displayed rather than the entire sentence. When the '-i' parameter was used, the case was
ignored.

This command is really useful if we simply want to check if a word exists in a file without having to deal with a really long sentence being outputted.
Since only the word is printed, the overall output is a lot cleaner.
