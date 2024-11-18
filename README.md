java c
EECS 1710
Programming for Digital Media
Lab #3 - Using and Defining Methods
Prerequisite
All previous labs.
Prior to starting this lab, ensure your PRISM account is setup and you can log into the PRISM lab machines. Also, make sure you are familiar with the Linux terminal and using the submit command.
Step 1 - Importing an Archived Project
As with the previous labs, use the following URL to download the project files for this lab:
http://www.eecs.yorku.ca/course_archive/2024-25/F/1710/labs/lab3/lab3.zip
Open Eclipse and import the above project. if you are not sure how to do this, follow the instructions in Lab #0 (click here).
Step 2 - Lab Exercises
WARNING: YOU HAVE 2 WEEKS TO FINISH THIS LAB, BUT DO NOT LEAVE THIS LAB TO THE LAST MINUTE!!
Open (expand) the project in Eclipse's Project Explorer. Complete the four questions in the project. Each question requires you to modify/complete some methods and test with calls from the main program.
The reference API useful for the exercises is found here:
Java API → http://docs.oracle.com/javase/8/docs/api/
Direct links to class documentation:
Math → https://docs.oracle.com/javase/8/docs/api/java/lang/Math.html
StdIn → https://introcs.cs.princeton.edu/java/stdlib/javadoc/StdIn.html
StdOut → https://introcs.cs.princeton.edu/java/stdlib/javadoc/StdOut.html
StdDraw → https://introcs.cs.princeton.edu/java/stdlib/javadoc/StdDraw.html
Follow the instructions below and enter your work in the java files that appear in the imported Eclipse project.
Question 1 - Creating Static Methods With/Without Inputs
In upcoming labs, we will organize some of our programs using a simple menu of options: The user selects one of the options to advance the program in a particular direction. In this exercise, the goal is simply to modularize the statements used to construct and display a menu on the console/terminal. It is likely that such a menu is displayed multiple times in a program;   so, it is useful to create a method to display the menu.
· First (part A), write the code to output the following menu to the screen:
Please choose a graphic to draw :
[1] Draw a Target
[2] Draw a Smiley Face
[3] Draw the LG Logo ( remember, Life's Good!)
[4] Quit Program
.  Create and debug this menu within the main() method first, then move the code to a
method called displayMenu(). Note that this method does not return a value (i.e., returns  void). The method simply generates output to the screen using StdOut or System.out print  statements. Take care to format the output exactly as shown above, where each item in the menu is indented by a single tab character ('/t').
Include a statement within the main() method that calls (invokes) the displayMenu() method.
· Next (part B), create another version of the displayMenu() method that accepts a String value as an input argument. Here's the method header :
public static void disp lay Menu (Str in g s tr)
This version of the method should interpret the argument str as the name of the user. For instance, if str = "Bob" is passed to the method, the output should be:
I understand that you want to see some gnarly visuals, Bob? Please choose a graphic to draw :
[1] Draw a Target
[2] Draw a Smiley Face
[3] Draw the LG Logo ( remember, Life's Good!)
[4] Quit ProgramInclude a second statement in the main() method that invokes the second version of the displayMenu(...) method with a string argument that is the equivalent of your eecs login  name.
When finished, submit your work: submit 1710 lab3 Question1.java 
Question 2 - Creating and Using Static Methods with Input and Output
In this exercise, we will create methods that accept inputs and return/generate an output. The methods are related to calculating the total amounts represented by a of series of coins put    into a piggy bank.
· The first is a method called dollarAmount with the following header : public static double dollar Amoun t ( in t cen ts)
This method receives a single integer argument as its input, cents, then computes and returns the equivalent decimal value (in dollars). Remember, no magic numbers!In the main method, some calls are provided for you to test the dollarAmount method. Running the Question2.java file should output the following when the dollarAmount  method is working:
part 1 :
-------
dollarAmount(154) = $1.54
dollarAmount(2317) = $23.17
dollarAmount(45308) = $453.08
Note: you may use method calls like this in your main at any time, to test various results of your methods (given different inputs). It is therefore useful to use main to test methods you create (a test with one set of inputs that gives an expected output is called a "unit" test).  Now, create a second method called totalCents with the following header :   public static in t total Cen ts ( in t n ickels, in t dimes, in t quar ter s)
This method returns an int that represents the total value of a set of coins being added into a Piggy Bank. The number of coins of each coin type is represented by the integer  arguments: nickels(5 cents), dimes(10 cents),and quarters (25 cents). The method
should then return the total value of these coins combined (in cents) as an integer.
Add three unit tests (similar to those setup for part 1), to display the output of this
method as per the example below. If working, your output should look something like this:
part 2 :
-------
totalCents(2,4,6) = 200
totalCents(10,4,62) = 1640
totalCents(10,4,62) = 1640Note: the formatting for output in part 1  2 is not that important, as you are just testing what your methods return. When marking, we will test the methods directly to see if they are correctly calculating the output for particular inputs.
.  Create a third method called addToPiggyBank with the following header :
public static void add To Piggy Bank (double balance, in t n ickels, in t dimes, in t quar ter s)
This method does not return anything, but rather, uses the methods from part 1  2 to    compute the totalCents and dollarAmount based on the coins provided through its input arguments. Save the results returned from these methods in appropriate variables inside  this method, so that you can display them.
This method should then add the dollarAmount of these coins to the (balance) previously stored in the Piggy Bank, to get the new total amount stored in the Piggy Bank.
Finally, format and display the result of adding these coins to the Piggy Bank as shown    below (note: this example only represents the result of one set of input arguments - you can test others also from your main)
Example output:
part 3 :
-------
My Piggy Bank :
========================
balance :        $ 10.00
adding :
-> nickels :       10
-> dimes :           4
-> quarters :      62
=========================
TOTAL FUNDS :    $ 26.40
=========================
When you are happy with your methods, submit your work: submit 1710 lab3 Question2.java 
Question 3 - Boolean method practice
In Question3.java you will write several methods that test input variables to代 写EECS 1710 Programming for Digital Media Lab #3Java
代做程序编程语言 determine a boolean outcome (true/false). The first two methods are sample problems from the coding bat website, while the third attempts to determine whether a particular day of the year is "Family Day " or not.
· In the first task, you will complete the method icyHot with the following header : public static boolean icy Hot ( in t temp 1, in t temp2)The coding bat URL for this problem can be found here. Comments are provided in the Question3.java file, and tests are also provided in the main method (run them by running the java file).
You may also go to the coding bat URL, and code this solution there (type statements
directly into the method, and press GO button to test). Note: you do NOT need to declare the method parameters, just use the variables already declared in the header. Once working, paste your solution back into the method shell provided for you in the question file.
· In the second task, you will complete the method answerCell with the following header :
public static boolean an swer Cell (boolean is Morn in g, boolean is Mom, boolean is Asleep)The coding bat URL for this problem can be found here. Comments are provided in the Question3.java file, and tests are also provided in the main method (run them by running the java file).You may also go to the coding bat URL, and code this solution there (as discussed in task 1). When you have coded your solution and it has passed all tests, paste the solution into your question file.
.  The third method to complete isFamilyDay () determines if the current day of the year is "Family Day " or not. It has the following header :
public static boolean is Family Day (char day Of Week, in t mon th, in t day)
The method works in Canada and Australia, and should return true if it is either the 1st Monday of October (Australia) or the 3rd Monday of February (Canada),and false
otherwise.
The inputs to the method are:
o  a character (day Of Week) representing the day of the week (i.e. Mon='M', Tue='T', Wed='W', Thu='K', Fri='F', Sat='S', Sun='Q')
o  an integer (mon th) representing the month of the year (e.g. 1,2,...,12 = Jan, Feb, ..., Dec)
o  an integer (day) representing the day of the month (e.g. 18 = 18th day of the month)
Examples of calling is Family Day (day Of Week,mon th,day) with resulting output are shown below:
o   isFamilyDay ('S',8,10) returns false o   isFamilyDay ('M',10,2) returns true
o   isFamilyDay ('M',10,10) returns false o   isFamilyDay ('T',11,26) returns false o   isFamilyDay ('M',2,18) returns true
o   isFamilyDay ('K',2,15) returns false
HINT: integer division of the day (by the number of days in a week) can tell you how many weeks have passed (i.e. which week of the month you are in). Complete your    method and run the tests included in the main method to check your output.
When finished and happy with your results, submit your work: submit 1710 lab3 Question3.java 
Question 4 - Using Std Draw methods to draw simple graphicsIn Question4.java, you will invoke the displayMenu() method from Question1 and will use StdIn to capture the users choice/selection and based on this, draw one of 4 different graphics into an application (StdDraw) window.
The StdDraw class is not one you have had much experience with, and so this question
forces you to explore the documentation file, and experiment with its methods (based on some reference code provided). The link for this class is given at the top of this document (and will be discussed more in lectures later in weeks 4/5).In this question, some initial code is provided that implements a method drawPrimitives() which can be invoked for learning about basic things that can be drawn using StdDraw. It  gives examples of drawing standard lines/rectangles/ellipses/arcs (filled or outlined).
It also includes a method (for reference) that draws a "Target" graphic. The 1st and 2nd figures below show the outputs of these two methods. The goals of the question is to complete the remaining two draw methods to create the SmileyFace graphic, and the LG logographic (also shown below).

Note: the StdDraw canvas size is already set for you (to 500x500 pixels),while the
positions of primitive lines/shapes use real valued coordinates (on the range 0-1 for both x andy), where (0.5,0.5) is the middle of the window. Browse through the drawPrimitives
and drawTarget methods for more insight into the method calls needed to create some of their features.
Convince yourself of the positioning of objects in the drawPrimitives() method by
modifying some of their parameter arguments and re-running to look at any changes in positioning/sizing that occur.
HINT: each draw call will paint OVER the previously drawn graphics
Finally, complete the code in the main method so that when a user types 1-3, each of the 3
graphics (target, smiley or LG logo) will be drawn. You first need to complete the
drawSmiley () and drawLGLogo() methods to create graphics that resemble those shown in the figures above). These can be tested by manually setting the choice variable (to = 2 or 3).
To complete the main:
o   call the displayMenu() method via its class name (in this case Question1), since it resides in the Question1 class. This will prompt the user to type in a choice (1-3). Note: you
wont need an import for this since all Question files sit inside the same "default" package.
o  Capture a value from user that indicates their choice from the menu. To do this, you need to use the StdIn class to read an integer typed in by the user at runtime (see
lectures for weeks 3-4). You can overwrite (re-assign) the typed value to the choice variable.
o   Observe (but do not modify) the branching statement (switch/case) that diverts to the method that will draw the chosen graphic.
o  Within each draw method, use StdDraw to set pen colours and draw simple shapes
(filled rectangles/circles or lines/arcs) to create the graphic picture (SmileyFace or LG Logo) as shown above
When you are happy with the look of your graphics (they do not have to be exact, but should look similar), submit your work:
submit 1710 lab3 Question4.java
SUBMISSION [** 2 weeks to complete!!!! Due: Tuesday Oct 8, 11:59pm (worth 4%)]
To complete this lab, you must submit the Java source files containing your solutions. Ensure your name and student number appear in comment lines at the top of each     source file submitted. To submit a file, open the Linux terminal and navigate to the
workspace for this lab. Then type
submit 17 10 lab3 Qu estion*.java
where "*" represents the wildcard character.
DO NOT SUBMIT A ZIP VERSION OF YOUR PROJECT!! Use the above submit command or do a separate submit for each question file.
You can repeat this to submit a second or third file. If you submit a file twice, it will
overwrite the previous version of that file. You can submit an unlimited number of times up until the deadline.
To check the files you have currently submitted, type submit – l 17 10 lab3
Alternatively, you can use web submit: https://webapp.eecs.yorku.ca/submit/.


         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
