# Week 3 Lab Report: Creating a Web Server and Testing Code

#### Part 1: StringServer Web Server
This web server is meant to take in a parameter and display it on the webpage. It does so one after another, with each input being displayed on a new line.

#####This is the code in StringServer.java:

![image](https://user-images.githubusercontent.com/70964947/214756838-4729ac6f-8a63-4009-b619-c913cc828eab.png)


#####This is one example of using /add-message:

<img width="618" alt="image" src="https://user-images.githubusercontent.com/70964947/214757081-04c4279f-ad0e-43cc-b805-277aa0726adb.png">

In this example, the main method in the StringServer class and the handleRequest method in the Handler class are called. The main method takes in an array of command line arguments, which in this case, is how the program knows what port to run the web server on. The handleRequest method takes in a URI, which is the link to the webpage that is displayed on the browser. Based on the query and path, the webpage is updated to reflect the newest entry while simultaneously displaying the old ones. For this case, the query was the only parameter that changed since the "/add-message" is always constant when trying to add a new entry to the String output. The only time "/add-message" will change is when the url path is "/", indicating the home page. In any other case, a 404 error is thrown.


#####This is another example of using /add-message:

<img width="471" alt="image" src="https://user-images.githubusercontent.com/70964947/214757134-f4f1208a-e7da-4c6f-8c6a-89db7d2387bf.png">

Like in the previous example, the main method in the StringServer class and the handleRequest method in the Handler class are called. The main method takes in an array of command line arguments, which in this case, is how the program knows what port to run the web server on. The handleRequest method takes in a URI, which is the link to the webpage that is displayed on the browser. Based on the query and path, the webpage is updated to reflect the newest entry while simultaneously displaying the old ones. Similar to the last example, the query was the parameter that changed, from "Hi, how are you doing" to "Testing,testing". The URL path stayed as "/add-message" since that was the operation we were performing.




