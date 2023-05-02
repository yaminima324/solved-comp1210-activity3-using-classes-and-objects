Download Link: https://assignmentchef.com/product/solved-comp1210-activity3-using-classes-and-objects
<br>
<strong>Terminology: </strong>

<table width="548">

 <tbody>

  <tr>

   <td width="210"><strong>new</strong> operatorclass objectreference variable instantiation nullmethod static method constructor</td>

   <td width="210">dot (<strong>.</strong>) operator parameter return aliasgarbage collection String class immutable Java API package</td>

   <td width="128">import declarationRandom classMath classNumberFormat class DecimalFormat class wrapper class autoboxing unboxing</td>

  </tr>

 </tbody>

</table>




<strong>Course Coding Standard Additions </strong>

<ul>

 <li>When using the import declaration, import classes from the same package individually (i.e. do <u>not</u> use the * notation). For example, you should have import java.util.Scanner and import util.Random rather than having import java.util.* which imports everything in the java.util package.</li>

 <li>When making calculations with π, use Math.PI rather than the literal value such as 3.141. You should always use constants when they are available.</li>

 <li>From now on, when using a Scanner object to scan input (e.g., from the keyboard), use nextLine to get numerical input from the user and convert it to a number using methods from the corresponding wrapper class.</li>

</ul>

For example to read in an int value from Scanner userInput:

int myInt = Integer.parseInt(userInput.nextLine());

For example to read in a double value from Scanner scan:

<h1>      double myDouble = Double.parseDouble(userInput.nextLine());</h1>

<strong> </strong>




<strong>            </strong>

<strong>Goals:</strong>

By the end of this activity you should be able to do the following: Ø Understand how to instantiate an object using the <strong>new</strong> operator

<ul>

 <li>Use the Java standard library (the Java API) to look up a class</li>

 <li>Use the String class and the Scanner class</li>

 <li>Construct a viewer canvas and run your program in the canvas</li>

</ul>




<strong>Program Description: </strong>

You will create a program that exchanges letters in a String to encode a message.

<strong> </strong>

<strong>In-lab Directions: </strong>

As you build your program incrementally by entering each of the code segments below, you should compile and run your program after each segment is completed.  This will allow you to verify that your program is correct after each step as you progress toward the completed program.

<strong>MessageConverter.java </strong>

<ul>

 <li>This program will read in a message from the user and then require the user to enter a number. The following will happen based on the number entered by user: o If the user enters a 1, the message will be printed trimmed.

  <ul>

   <li>If the user enters a 2, the message will be printed in lower case. o If the user enters a 3, the message will be printed in upper case.</li>

   <li>If the user enters a 4, the message will be printed with all vowels replaced with underscores.</li>

   <li>If the user enters a 5, the message will be printed without the first and last character.</li>

   <li>Any other number should generate an appropriate message.</li>

  </ul></li>

</ul>




<ul>

 <li>Create a class called <strong>MessageConverter</strong> that includes a main method. Also add an import statement for the java.util.Scanner class. The import statement should be the first line in your Java file (i.e., it comes before the class declaration as well as comments).</li>

</ul>




<ul>

 <li>In the main method, declare the following variables:

  <ul>

   <li>userInput: Scanner object for reading the user input from the keyboard.</li>

  </ul></li>

</ul>

Scanner userInput = new Scanner(System.in);

<ul>

 <li><strong>message</strong>: String object for the user input; initialized to an empty String.</li>

</ul>

<h1>String message = <strong>“”</strong>;</h1>

<ul>

 <li><strong>outputType</strong>: An int representing the type of output the user wants.</li>

 <li><strong>result</strong>: String object for the converted message; initialized to an empty String.</li>

</ul>

<h1>String result = <strong>“”</strong>;</h1>




<ul>

 <li>Request input from the user then get user input using the nextLine() method of the Scanner class.</li>

</ul>




Now get the user’s input for the output type. Make sure that you understand how the code below works. Notice that this is a call to the print method rather than println.




<ul>

 <li>Set up an <em>if</em> statement that will print out the appropriate message based on the user’s selected output type. Note that you can write code for alternate conditions in the <em>if</em> statement using <em>else if</em> after the <em>if</em></li>

</ul>




<ul>

 <li><u>After</u> the <u>entire</u> <em>if-else</em> statement, add the following line of code to print out the result.</li>

</ul>




<strong><u>Compile now and after each step below</u> as you fill in the <em>if</em>-else-if-else in the following steps.</strong>

<ul>

 <li>The first condition for outputType equal to 0 sets the result to the original message which may include leading and/or trailing spaces.</li>

</ul>







Because message references an instance of the String class, we can use the methods in the String class to return a new String that is a modified version of the original String referenced by message (<u>the original String object is not changed</u>).  To see the available methods in the String class, go to the Java API at <u>http://docs.oracle.com/javase/8/docs/api/</u> and find the <strong>String</strong> class in the lower left pane on the page and left-click on it.  This will open the String page in large right window of the API as shown below.  You should become familiar with the API since it describes all of the classes that come with the JDK.




<ul>

 <li>In the main window on the right side, click method at the top or scroll down to Method Summary to see the methods that our String object <strong>message</strong> can use.</li>

</ul>




<ul>

 <li><u>String methods do not modify the String object upon which they are called</u>. Instead, if a method has a String return type, then it returns <u>a new String object</u> which may be a modified version of the original String.</li>

</ul>

The second condition for outputType equal to 1 sets the result to the trimmed value of the message; i.e., we can use the trim method removes any leading or trailing whitespace. The API entry for a method shows the return type for the method in the left and the method name with formal parameters, if any, on the right along with a brief description of what the method does.  So the entry shown below for the <em>trim</em> method indicates that it returns a String and takes no parameters. Remember, <u>the <strong><em>trim</em></strong> method does not modify the String object upon</u> <u>which it is called</u>. Instead it returns a new String object which is the trimmed version of original String.




Returns a String             Method name – there are no formal parameters for this method




<u>Be sure to compile</u> each time you complete a part of the <strong><em>if</em>-else-if-else </strong>below.




<ul>

 <li>The third condition for outputType equal to 2 sets the result to the lower case value of the message; i.e., we can use the toLowerCase method. The Java API entry shown below for the <em>toLowerCase</em> method indicates that it returns a String and takes no parameters.</li>

</ul>




Returns a String             Method name – there are no formal parameters for this method




Based on this knowledge, you can now invoke the toLowerCase method on our <strong>message</strong> object to return its value in lower case. Place the following code in second block of the if statement:







<ul>

 <li>Look at the API description for the toUpperCase method and place the following line in the second block of the if statement:</li>

</ul>







<ul>

 <li>Now write code that will replace specified characters in the message with other characters. In order to change a character, we need to use the <em>replace</em> method of String to change certain characters of our string. Take a look at the <em>replace</em> method in the Java API. We see that it returns a String and that it requires two parameters: the character you want to replace and the new character.  Note there are two versions of replace: the first takes parameters of type <em>char</em> (e.g., ‘a’ or ‘e’).and the second takes parameters of type <em>CharSequence</em> which includes String literals (e.g., “a” or “abc”).  In the code below, we will use the <em>char</em></li>

</ul>




Returns a String             Method name and two formal parameters







<u>As with the other String methods, the <strong><em>replace</em></strong> method does not modify the String object it</u>. Instead it returns a new String object in which the new character has replaced the old character.




<ul>

 <li>First, use the <em>replace</em> method to change all of the a’s to underscores. The following line of code replaces the ‘a’ characters of the message value and then assigns the new version of message to result. Again, note that message itself remains unchanged.</li>

</ul>




<strong> </strong>

Now complete the translation by converting the remaining vowels to underscores for outputType equal to 4 .







<ul>

 <li>Now use the <em>substring</em> method and length method to extract a part (or substring) of the message.</li>

</ul>

Returns a String             Method name and formal parameters







Recall the characters in a String are indexed beginning at 0. Since the requirement here is for result to include everything except the first and last character, use the second version of




<em>substring</em> with 1 as the parameter beginIndex and message.length() – 1 as endIndex.







<ul>

 <li>Finally, if the user enters a number other than 1, 2, 3, 4, or 5, result should be set to an error message.</li>

</ul>







<ul>

 <li>Test your program under each of the conditions.</li>

</ul>

<strong> </strong>

<strong>Original</strong> (“as is”): For the message, enter: “     This is a test.”   <u>Be sure to include the five leading spaces, but omit the quotes</u>.  For choice, enter 0.

<table width="551">

 <tbody>

  <tr>

   <td width="551">Type in a message and press enter:&gt;      This is a test. Output types:    0: As is1: Trimmed2: lower case3: UPPER CASE4: v_w_ls r_pl_c_d5: Without first and last characterEnter your choice: 0 This is a test.<strong> </strong></td>

  </tr>

 </tbody>

</table>

<strong> </strong>

<strong>Trimmed</strong>: Use the Up arrow key to retrieve the message you entered above, then for choice, enter 1.  Notice the five leading spaces have been removed in the output.

<table width="551">

 <tbody>

  <tr>

   <td width="551">Type in a message and press enter:&gt;      This is a test. Output types:    0: As is1: Trimmed2: lower case3: UPPER CASE4: v_w_ls r_pl_c_d5: Without first and last characterEnter your choice: 1 This is a test. <strong> </strong></td>

  </tr>

 </tbody>

</table>




<strong>Lower case</strong>: Use the Up arrow key to retrieve the message you entered above, then for choice, enter 2.  Notice the output is in all lower case but the five leading spaces have <u>not</u> been removed.

<table width="551">

 <tbody>

  <tr>

   <td width="551">Type in a message and press enter:&gt;      This is a test. Output types:0: As is1: Trimmed2: lower case3: UPPER CASE4: v_w_ls r_pl_c_d5: Without first and last characterEnter your choice: 2this is a test.<strong> </strong></td>

  </tr>

 </tbody>

</table>

<strong> </strong>

<strong>Upper case</strong>: Use the Up arrow key to retrieve the message you entered above, then for choice, enter 3.  Notice the output is in all upper case but the five leading spaces have <u>not</u> been removed.

<table width="551">

 <tbody>

  <tr>

   <td width="551">Type in a message and press enter:&gt;      This is a test. Output types:    0: As is1: Trimmed2: lower case3: UPPER CASE4: v_w_ls r_pl_c_d5: Without first and last characterEnter your choice: 3 THIS IS A TEST.<strong> </strong></td>

  </tr>

 </tbody>

</table>

<strong> </strong>

<strong>Vowels replaced</strong>: Use the Up arrow key to retrieve the message you entered above, then for choice, enter 4.  Notice the output has the vowels removed but the five leading spaces have <u>not</u> been removed.

<table width="551">

 <tbody>

  <tr>

   <td width="551">Type in a message and press enter:&gt;      This is a test. Output types:    0: As is1: Trimmed2: lower case3: UPPER CASE4: v_w_ls r_pl_c_d</td>

  </tr>

 </tbody>

</table>

5: Without first and last character

Enter your choice: 4




Th_s _s _ t_st.

<strong> </strong>

<strong> </strong>

<strong>Without first and last character</strong>: For the message, enter “This is a test.”  <u>This time</u> <u>do not enter any leading or trailing spaces</u>.  Then for choice, enter 5.  Notice the output has the first and last character removed.

<table width="551">

 <tbody>

  <tr>

   <td width="551">Type in a message and press enter:&gt; This is a test. Output types:    0: As is1: Trimmed2: lower case3: UPPER CASE4: v_w_ls r_pl_c_d5: Without first and last characterEnter your choice: 5 his is a test<strong> </strong></td>

  </tr>

 </tbody>

</table>

<strong> </strong>

<strong>Invalid input</strong>:

<table width="551">

 <tbody>

  <tr>

   <td width="551">Type in a message and press enter:&gt; This is a test. Output types:    0: As is1: Trimmed2: lower case3: UPPER CASE4: v_w_ls r_pl_c_d5: Without first and last characterEnter your choice: 7 Error: Invalid choice input.<strong> </strong></td>

  </tr>

 </tbody>

</table>

<strong> </strong>

<ul>

 <li><strong>Try the input “A message” for the message and choose to replace all vowels with underscores. What do you notice about the output? Why do you think that one of the vowels was not replaced? How would you go about correcting the issue? You don’t have to make this change – – just think about it. </strong></li>

</ul>

<strong> </strong>

<strong>Web-CAT</strong> – After you have completed the program in this activity, you should submit your

MessageConverter.java file to Web-CAT.  This is the only file you will submit for this activity.

<strong>             </strong>




<h1><strong> of 11    </strong></h1>

<strong>Using the Viewer Canvas with your MessageConverter program  </strong>

<strong> </strong>

Now we want to create a viewer canvas so we can see what is happening in the MessageConverter program step-by-step as it runs.  Note that we could have done this step as soon as the variables had been declared above.  For your project assignments, you should consider creating a canvas at any point that you need insight into exactly what is happening in your program.




<ul>

 <li>With MessageConverter.java in the CSD edit window, click the Run in Canvas button on the toolbar.  In the CSD window, you should see that the program is stopped at the first executable statement, and you should see an empty viewer canvas window as shown below.</li>

</ul>







<ul>

 <li>As indicated by the message in the canvas, click the debug step button to execute the statement to create a Scanner object on System.in which is the keyboard. You should now see the variable name userInput in the Debug tab.  Now click the step button  <u>three</u> more times so that you see message, result, and outputType in the Debug tab.  Now drag each of these variables into the canvas window and arrange them as shown in the figure below.  Click the Save button</li>

</ul>




<strong>   </strong>

<h1><strong> of 11    </strong></h1>

<ul>

 <li>Now click the play button , and your program will begin auto-stepping until is pauses waiting for input. After you enter the requested input each time, the viewers on canvas will be updated.  The <em>run in canvas</em> will continue until your program terminates at which time the viewers on the canvas will display their last values as shown in the example below for <em>message</em> “This is a test” and <em>outputType</em> = 4.</li>

</ul>










Although we created the canvas for the MessageConverter after the program was completed, it would have been even more appropriate to create the canvas as the program was being coded, especially if you were encountering logical errors in your program. For example, if you sense that an error has occurred at particular place in the program, you should set a breakpoint on the statement where you want to examine the behavior.  [To set a breakpoint, move the mouse over the margin to the left of the statement until you see the red octagon (stop sign symbol) and then left-click the mouse.]  Then instead of clicking the Run in Canvas button  on the toolbar, click the Debug button .  The program will run to the breakpoint and stop.  You can single-step  (or perhaps step-in ) and observe the variables in the canvas and debug tab to help determine the nature of the error so that you can correct it.

<strong>   </strong>