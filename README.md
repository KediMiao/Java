# Java
Basci Java Notes



****************Jshell***********************

MacBook-Air:Desktop miao$ jshell

jshell> /help

jshell> /list -all

jshell> /list -start

jshell> {
   ...>     


jshell> /exit
|  Goodbye


jshell> /var
|    int myFristNumber = 35
|    int mySecondNumber = 12
|    int myThridNumber = 6



****************BACIS KNOWLEDGE***********************

int range : 
jshell> int myMinIntValue = Integer.MIN_VALUE;           BTW,Integer is a class store some values.              32bits
myMinIntValue ==> -2147483648

jshell> int myMaxValue = Integer.MAX_VALUE;
myMaxValue ==> 2147483647



jshell> System.out.print(myMaxValue + 1);        Overflow and Underflow
-2147483648
jshell> System.out.print(myMinIntValue - 1);
2147483647



jshell> int willThisCompile = Integer.MAX_VALUE + 1;         Compile error
willThisCompile ==> -2147483648

jshell> int willThisCompile2 = 2147483648;
|  Error:
|  integer number too large
|  int willThisCompile2 = 2147483648;
|                         ^


jshell> int willThisCompile2 = 2_147_483_647;              , == _
willThisCompile2 ==> 2147483647



jshell> System.out.print("Byte value (" + Byte.MIN_VALUE + " to " + Byte.MAX_VALUE + ")");                 8bits
Byte value (-128 to 127)

jshell> System.out.print("Short value (" + Short.MIN_VALUE + " to " + Short.MAX_VALUE + ")");              16bits
Short value (-32768 to 32767)

jshell> System.out.print("long value (" + Long.MIN_VALUE + " to " + Long.MAX_VALUE + ")");
long value (-9223372036854775808 to 9223372036854775807)




jshell> long myLongValue = 100L;                      Always add "L" after the value                        64bits
myLongValue ==> 100

jshell> long myLongValue = 50_000L + 10L * (myByteValue + myShortValue + myIntValue);
myLongValue ==> -425430




jshell> byte a = 1, b = 2;                     
a ==> 1
b ==> 2

******************Casting***********************

jshell> int myTotal = (myMinIntValue / 2);
myTotal ==> -1073741824


jshell> byte myMinByte = Byte.MIN_VALUE;
myMinByte ==> -128

jshell> byte myNewByteValue = (myMinByte / 2);                       BTW, doesn't matter what is the value inside of the 'myMinByte', even if just 1,                                                                           because JAVA will treat it like a int.
|  Error:
|  incompatible types: possible lossy conversion from int to byte
|  byte myNewByteValue = (myMinByte / 2);
|                         ^-----------^


jshell> byte myNewByteValue = (-128 / 2);
myNewByteValue ==> -64


jshell> byte myNewByteValue =(byte) (myMinByte / 2);              We need to do this!
myNewByteValue ==> -64






