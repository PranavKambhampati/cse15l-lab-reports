# Week 3 Lab Report: Creating a Web Server and Testing Code

### Part 1: StringServer Web Server
This web server is meant to take in a parameter and display it on the webpage. It does so one after another, with each input being displayed on a new line.

###### This is the code in StringServer.java:

![image](https://user-images.githubusercontent.com/70964947/214756838-4729ac6f-8a63-4009-b619-c913cc828eab.png)


###### This is one example of using /add-message:

<img width="618" alt="image" src="https://user-images.githubusercontent.com/70964947/214757081-04c4279f-ad0e-43cc-b805-277aa0726adb.png">

In this example, the main method in the StringServer class and the handleRequest method in the Handler class are called. The main method takes in an array of command line arguments, which in this case, is how the program knows what port to run the web server on. The handleRequest method takes in a URI, which is the link to the webpage that is displayed on the browser. Based on the query and path, the webpage is updated to reflect the newest entry while simultaneously displaying the old ones. For this case, the query was the only parameter that changed since the "/add-message" is always constant when trying to add a new entry to the String output. The only time "/add-message" will change is when the url path is "/", indicating the home page. In any other case, a 404 error is thrown.


###### This is another example of using /add-message:

<img width="471" alt="image" src="https://user-images.githubusercontent.com/70964947/214757134-f4f1208a-e7da-4c6f-8c6a-89db7d2387bf.png">

Like in the previous example, the main method in the StringServer class and the handleRequest method in the Handler class are called. The main method takes in an array of command line arguments, which in this case, is how the program knows what port to run the web server on. The handleRequest method takes in a URI, which is the link to the webpage that is displayed on the browser. Based on the query and path, the webpage is updated to reflect the newest entry while simultaneously displaying the old ones. Similar to the last example, the query was the parameter that changed, from "Hi, how are you doing" to "Testing,testing". The URL path stayed as "/add-message" since that was the operation we were performing.

### Part 2: Testing Bugs
The bug I chose to analyze is the bug in the Reversed method of ArrayExamples.java. This code is supposed to return an array in which the elements from the input array are reversed.

An failure-inducing input was {0,1,2,3}.
This is what the JUnit Test looked like:
```
@Test
  public void testReversed2(){
    int[] input = {0,1,2,3};
    System.out.println(ArrayExamples.reversed(input));
    assertArrayEquals(new int[]{3,2,1,0}, ArrayExamples.reversed(input));
  }
```

An input that didn't induce a failure was {}. This is an empty array.
This is what the JUnit Test looked like:
```
@Test
  public void testReversed() {
    int[] input1 = { };
    assertArrayEquals(new int[]{ }, ArrayExamples.reversed(input1));
  }
```

This was the symptom of running these tests:
<img width="1098" alt="image" src="https://user-images.githubusercontent.com/70964947/214759954-ff7dbb8b-1fac-46cf-ac4c-c66a839d5c39.png">

This is what the original, buggy code looks like, **before** any changes have been made:
```
static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
  }
```

This is the code for the method **after** the bug has been fixed:
```
static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      newArray[i] = arr[arr.length - i - 1];
    }
    return newArray;
  }
```

These fixes fix the bug because now, instead of setting the elements in the original array with empty elements from the newArray, we make sure to use the elements from the old array to reverse it through the new array. We also return the new array instead of the old array - this way we're reversing the reversed array instead of the original. Finally, the bound in the for loop is also adjusted to ensure we don't get IndexOutOfBounds errors.

### Part 3: Reflection
In these last two labs, I've learned many new things, such as building my own web server that takes inputs through the URL as well as using JUnit to debug my code. While I've known that you could run a web server through Java, I never actually knew how to do it, so last week's lab was great in showing me how to do this. The next step to developing the webpage could be to add some HTML (if possible) so that there's more information and formatting on the webpage.

Additionally, we have just started using JUnit in CSE 12 as well, so using it in today's lab was really good exposure to writing test cases for the Programming Assignments in that class. I never knew that Java had an entire library dedicated to helping users test their code - I always thought that we'd have to do it manually through print statements. I've learned how much more flexibility and ease JUnit can add to the debugging process, so I'll definitely continue using this tool in the future.


