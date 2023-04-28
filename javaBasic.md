I open another file because last time my laptop crashed and lots of code still on GitHub was not saved.
I guess only when you really experience it once then you know why you should use the local repository, when git\push, now I truly understand.

Contiune on Jshell:

jshell> String myString = "This is my string";
myString ==> "This is my string"

jshell> myString = myString + ", and there is more!";
myString ==> "This is my string, and there is more!"

jshell> myString = "I have \u00241,000,000";
myString ==> "I have $1,000,000"

jshell> {
...> String numberString = "250.55";
...> numberString = numberString + "49.45";
...> System.out.print(numberString);
...> }
250.5549.45

jshell> String lastString = "10"; int lastInt = 50; lastString = lastString + lastInt; System.out.print(lastString);
lastString ==> "10"
lastInt ==> 50
lastString ==> "1050"
1050

Strings are immutable, so as for the code above, I didn't actually change the 'lastString', instead java create a new string with lastString + "50", the older will be discard.
So it is slow, no good.
So in this case, I wanna use "StringBuilder".

BTW, String is not a primitive type, it is a class.

jshell> char firstChar = 'A'; char secondChar = 'B';
firstChar ==> 'A'
secondChar ==> 'B'

jshell> System.out.print(firstChar + secondChar);
131
jshell> System.out.print("" + firstChar + secondChar);
AB

04/27/2023 continue learn Java Basic, goog news: somehow I linked VS Code with Github, and you know what, many important files on my desktop just lost.... Tear in my eyes.....^\_^....

jshell> {
...> int result = 10;
...> result -= 5.5;
...> System.out.print(result);}
4

jshell> {
...> int result = 10;
...> result = result - 5.5;
...> System.out.print(result);}
| Error:
| incompatible types: possible lossy conversion from double to int
| result = result - 5.5;
| ^-----

jshell> {
...> int result = 10;
...> result = (int)( result - 5.5);
...> System.out.print(result);}
4

\*\*so x -=y is acutally means x = (x data type) (x - y);
