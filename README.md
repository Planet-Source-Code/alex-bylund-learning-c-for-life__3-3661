<div align="center">

## Learning C\+\+ for Life


</div>

### Description

This is a tutorial I wrote to teach C++ to people who want to learn it. I decided to post it here to help as many people as possible. Please leave feedback, and if you like it vote ;)
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Alex Bylund](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/alex-bylund.md)
**Level**          |Beginner
**User Rating**    |4.1 (65 globes from 16 users)
**Compatibility**  |C\+\+ \(general\), Microsoft Visual C\+\+, Borland C\+\+, UNIX C\+\+
**Category**       |[Miscellaneous](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/miscellaneous__3-1.md)
**World**          |[C / C\+\+](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/c-c.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/alex-bylund-learning-c-for-life__3-3661/archive/master.zip)





### Source Code

Learning C++ for Life -- Part 1<br>
Revision 1.1.3<br>
By: AxE (voodooorbital@hotmail.com)<br><br>
===Intro============================================================<br><br>
This is my first text, I don't do spell check, and I don't write a lot.<br>
This text is also ment for someone not knowing much about C++.<br><br>
If you know another language, C++ wont be hard to learn. First if you don't<br>
have a compiler go to http://www.bloodshed.net/ and download the Dev-C++<br>
IDE. It comes with everything you need. Its for Windows, but I'm guessing <br>
if you are in Linux, you already have a compiler...<br><br>
===Getting started==================================================<br><br>
I'll start by a basic C++ program you could write, Hello world :)<br><br>
///////////////////////////////////////////////////////////////////<br>
/* Hello world */<br><br>
<xmp>#include <iostream.h></xmp>
<pre>
int main()
{
  cout << "Hello world" << endl;
  return 0;
}</pre>
///////////////////////////////////////////////////////////////////<br><br>
This code will print "Hello world" to the screen. If you run it from a<br>
DOS window from windows, it will look like it doesnt work because will<br>
flash up and then close. It only stays open while the program is runing,<br>
and will close after the program is done (the program only prints to the<br>
screen). You should run command.com so you can see the results. Later in<br>
this text, you will learn how to make it so the user must press a key to <br>
continue.<br><br>
Now for the explanations:<br><br>
The first line '/* Hello world */' is completly ignored by the compiler.<br>
These are called comments. Everything between '/*' and '*/' is ignored.<br>
Even line returns. Other valid comments would look like this:<br><br>
/* This is also<br>
  a valid comment */ <br><br>
/*<br>
This is also a valid comment<br>
*/<br><br>
Just about anything works as long as you start the comment, and then end<br>
it. You can comment out entire lines of code if needed. These type of<br>
comments are usally called C comments, and can be used in both. The other<br>
type of comment is using '//' and only works in C++. These comments only<br>
work for the same line. After you hit return it ends the comment. Here is<br>
a example of a correct comment:<br><br>
// This is a comment<br><br>
Here is a example of a incorrect comment:<br><br>
// This is not<br>
  A comment<br><br>
This is incorrect because the compiler will only ignore everything on the<br>
same line after it. The compiler will thing you were meaning 'A comment'<br>
as some instruction, and come up with some error.<br><br>
Use comments when you think something is important to remember. So you don't<br>
need comments when just printing to the screen. More like, leaving a comment<br>
above a function saying what it does (More on that later).<br><br>
The next line of code (third line in text) '#include <iostream.h>' Means to<br>
include other code already writin so you don't have to re-program it when<br>
ever you want to use it. iostream.h is a header file that holds the code you<br>
need to use cout. <br><br>
The next line of code 'int main()' starts the main function. Every program<br>
needs a main function. The '{' and the '}' are parts of the main function.<br>
Everything between { and } is the main function, this is where you put all <br>
of your code. { and } are there to let the compiler know thats the start ({)<br>
and the end ({) of the main function. The main function executes commands<br>
and calles to other functions (more later).<br><br>
The next line of code 'cout << "Hello world" << endl;' prints Hello world<br>
to the screen... you probably already guessed that though :P endl means <br>
to end the line. This is so if you print out anything else they will be<br>
on different lines. When you put ';' at the end of the line, its telling<br>
the compiler thats the end of that instruction. The insertion operation<br>
(<<) is used to send the data to the stream. You could also put it like<br>
this:<br><br>
cout <<<br>
"Hello world"<br>
<<<br>
endl;<br><br>
You can do this because the compiler will ignore white space (spaces, line<br>
returns, etc.). You wouldnt want to put this over multiple lines though<br>
because its easyer to read it when its just on one line. You could also<br>
do it like this if you wanted:<br><br>
cout    <<      "Hello world" <<    endl<br>
;<br><br>
Multiple line and spaced around ;) Like I said though, you wouldnt want to<br>
do that because it just makes it harder to read.<br><br>
The last line of code in the main function 'return 0;' tells it that the <br>
program is done. When you return zero in the main function it will end<br>
the program.<br><br>
===For loops========================================================<br><br>
Lets edit the program to print "Hello world" to the screen ten times,<br>
without typing "cout << "Hello world" << endl;" ten times. To do this <br>
we need a loop. A loop will execute the same instructions until what <br>
you have programmed it for is complete.<br><br>
Here is the full Hello World loop program:<br><br>
///////////////////////////////////////////////////////////////////<br>
/* Hello world */<br>
<xmp>#include <iostream.h></xmp>
<pre>
int main()
{
  for (int x = 0; x < 10; x++)
  {
    cout << "Hello world" << endl;
  }
  return 0;
}</pre>
///////////////////////////////////////////////////////////////////<br><br>
Looking at the for loops:<br><br>
for (int x = 0; x < 10; x++)<br><br>
The first part 'int x = 0;' initializes x, and sets it to zero. More on <br>
variables on the next section.<br><br>
The second part 'x < 10;' means the loop will keep running until this <br>
statement is false. So it will keep running as long as x is less than 10.<br><br>
The last part 'x++' is what the loop should do every time it runs threw <br>
it. 'x++' is like 'x = x + 1'. So every time the loop is ran it will add <br>
one to the value of x.<br><br>
Everything between the '{' and '}' will be done. Don't confuse the<br>
main {} with the for {}. The for loops also need {} to know everything<br>
part of it. You can make a loop without them, but it can only execute<br>
one line of code. Example would be:<br><br>
for (int x = 0; x < 10; x++)<br>
  cout << "Hello world" << endl;<br><br>
It looks the same, but anything under the cout will be considered out<br>
of the loop. A loop you would need brackets would be like this:<br><br>
for (int x = 0; x < 10; x++)<br>
{<br>
  cout << x << ": ";<br>
  cout << "Hello world" << endl;<br>
}<br><br>
Of corse that same loop could be done in one statement, but its just a<br>
example. If you're wondering what it would look like in one statement<br>
it would be like this:<br><br>
for (int x = 0; x < 10; x++)<br>
  cout << x << ": " << "Hello world" << endl;<br><br>
===Variables========================================================<br><br>
Now you will learn how to make variables to hold numbers. This is a<br>
demonstration on how to get two numbers from a user, and then add them <br>
together:<br><br>
///////////////////////////////////////////////////////////////////<br>
<xmp>#include <iostream.h></xmp>
<pre>
int main()
{
  int number1, number2, number3;
  cout << "Please enter a number ";
  cin >> number1;
  cout << "Please enter another number ";
  cin >> number2;
  number3 = number1 + number2;
  cout << endl << number1 << "+" << number2 << "=" << number3 << endl;
  return 0;
}</pre>
///////////////////////////////////////////////////////////////////<br><br>
This example introduces you do cin. cin will take a input from the user.<br><br>
'int number1, number2, number3;' tells the compiler those variables will<br>
hold numbers. Putting the varialbes on one line seperating them with a <br>
comma is like killing three birds with one stone ;) Instead of telling <br>
each one what they are, you can just put commas and the compiler knows you <br>
want them all to be ints. <br><br>
If you int a variable, it will hold values -2,147,483,648 to <br>
2,147,483,647 (32-bit). There are other ways to tell the computer you are <br>
going to use numbers.<br><br>
The way they are different is because they hold different values. For <br>
example, if you did 'double number1;' it would hold values 2.2e-308 to <br>
1.8e308. Thats WAY to much to get user input on two numbers to add. So using<br>
int is probably good for now.<br><br>
After you have told the compiler you want three variables, you can use them. <br>
:P You must declare the variable before you use it.<br><br>
'cin >> number1;' will get the number for variable number1, and the same<br>
will happen for 'cin >> number2;'<br><br>
'number3 = number1 + number2;' does exactly what it says. It makes variable <br>
number3 equal the sum of number1 and number2.<br><br>
'cout << endl << number1 << "+" << number2 << "=" << number3 << endl;'<br>
might look strange at first glance, but its easy if you look through<br>
it ;) It first goes to a new line, then prints the value of number1,<br>
"+", number2, "=", number3, and then ends that line.<br><br>
===Functions========================================================<br><br>
You should know that the main function is needed at all times. What about <br>
other functions though? Now you will learn how to add two numbers like <br>
before, except the addition will be done by a function other than main.<br><br>
///////////////////////////////////////////////////////////////////<br>
<xmp>#include <iostream.h></xmp>
<pre>
int add(int numb1, int numb2);
int main()
{
  int number1, number2, number3;
  cout << "Please enter a number ";
  cin >> number1;
  cout << "Please enter another number ";
  cin >> number2;
  number3 = add(number1, number2);
  cout << endl << number1 << "+" << number2 << "=" << number3 << endl;
  return 0;
}
int add(int numb1, int numb2)
{
  return numb1 + numb2;
}</pre>
///////////////////////////////////////////////////////////////////<br>
'int add(int numb1, int numb2);' is needed for all functions. You have to <br>
declare the function before it is used. The int before the function means <br>
it will return a int number. When you declare a function this way, it has<br>
to be the same format as the actual function. So if its a int, and has two<br>
ints that are sent to it, so must the declaration.<br><br>
'number3 = add(number1, number2);' this sets the variable number3 to what<br>
ever the add function returns. It sends number1 and number2 to the function.<br><br>
The function:<br>
int add(int numb1, int numb2)<br>
{<br>
  return numb1 + numb2;<br>
}<br>
The function input variables are numb1 and numb2. You sent the values of<br>
number1 and number2 to act as numb1 and numb2. The function then adds the<br>
two values, and returns the product.<br><br>
Sence number3 will equal what ever the function returns, it now equals<br>
number1 plus number2.<br><br>
===IF Statements====================================================<br><br>
If statements will run the code if a expresion is ture. For example:<br><br>
if (number1 > 10)<br>
 cout << "That value is greater than 10";<br><br>
It would only display the message if the number was greater than 10.<br><br>
If statements can also be multiple line, this is a example:<br><br>
if (number1 > 10)<br>
{<br>
  cout << "That value is greater than 10";<br>
  cout << endl;<br>
}<br>
You can also use ELSE. Here is a example:<br><br>
if (number1 > 10)<br>
{<br>
  cout << "That value is greater than 10";<br>
  cout << endl;<br>
}<br>
else<br>
{<br>
  cout << "That value is less than 10";<br>
  cout << endl;<br>
}<br><br>
So if 'number1 > 10' is false, then it will go to the else section and do<br>
what ever code you have there.<br><br>
===Conclusion=======================================================<br><br>
You should now understand more about how C++ works, and be able to learn new<br>
things on your own.<br><br>
This is the end right now, because I don't know what else to put in ;)<br>
To get part 2 when it comes out, or a newer version of this text go to one<br>
of these sites:<br><br>
http://gremlin.vectorstar.net/cgi-bin/1.cgi/<br>
http://www.axion-network.net/<br>
http://kickme.to/axe/<br><br>
You may distribute this text as you wish, as long as you leave everything<br>
the way it is. If you feel something needs to be changed or added, e-mail<br>
me.

