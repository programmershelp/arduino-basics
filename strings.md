There are two types of strings that you can use in Arduino programming:

1) Arrays of characters which are the same as the strings used in C programming 
2) The Arduino String which lets us use a string object in a sketch

### 1: String Character Arrays

The first type of string that we will learn about is the string that is a series of characters of the type char. 

A string is an array of char variables. A string is a special array that has one extra element at the end of the string, which always has a value of 0. 

This is known as a null-terminated string, this allows other functions to tell where the end of a string is. 

So this means that your string needs to have space for one extra character than the actual text you want it to contain. Let us look at an example  

<pre>
void setup()
{
char hello_str1\[6\] = {'h', 'e', 'l', 'l', 'o'};
char hello_str2\[6\] = {'h', 'e', 'l', 'l', 'o', '\\0'};
char hello_str3\[\] = "hello";
char hello_str4\[6\] = "hello";
char hello_str5\[15\] = "hello";
Serial.begin(9600);
Serial.println(hello_str1);
Serial.println(hello_str2);
Serial.println(hello_str3);
Serial.println(hello_str4);
Serial.println(hello_str5);
}

void loop() {

}
</pre>

  Now let us look at the following, all of these are valid ways of declaring a string

<pre>
void setup()
{
char hello_str1\[6\] = {'h', 'e', 'l', 'l', 'o'};
char hello_str2\[6\] = {'h', 'e', 'l', 'l', 'o', '\\0'};
char hello_str3\[\] = "hello";
char hello_str4\[6\] = "hello";
char hello_str5\[15\] = "hello";
Serial.begin(9600);
Serial.println(hello_str1);
Serial.println(hello_str2);
Serial.println(hello_str3);
Serial.println(hello_str4);
Serial.println(hello_str5);
}

void loop() {

}
</pre>

  Run this and you should see the following in the serial monitor
  
<pre>
hello
hello
hello
hello
hello
</pre>

Let us look at some functions that you can use with strings 

<pre>
void setup()
{
char str\[\] = "This is a test string"; // create a string
char out_str\[40\]; // output from string functions placed here
int num;

Serial.begin(9600);

Serial.println(str);// print the string

num = strlen(str); //get the length of the string
Serial.print("String length is: ");
Serial.println(num);

strcpy(out_str, str); //copy a string
Serial.println(out_str);

strcat(out_str, " which is bigger now."); //join two strings
Serial.println(out_str);

}

void loop() {
}
</pre>

  When you run this in the serial monitor you should see something like this
  
<pre>
This is a test string
String length is: 21
This is a test string
This is a test string which is bigger now.
</pre>

### 2: String Object

A **String** object is a special type of variable that is used to hold groups of characters

There are multiple versions that construct Strings from different data types (i.e. format them as sequences of characters), including:

* a constant string of characters, in double-quotes (i.e. a char array)
* a single constant character, in single quotes
* another instance of the String object
* a constant integer or long integer
* a constant integer or long integer, using a specified base
* an integer or long integer variable
* an integer or long integer variable, using a specified base
* a float or double, using a specified decimal places

#### Various string functions

<pre>
String aString = "This is a Test String";
String newString = "";

void setup()
{
  Serial.begin(9600);
  Serial.println(aString); //print the test string
  Serial.println(aString.length()); //length of the string
  Serial.println(aString.charAt(2)); //character at position 3 
  Serial.println(aString.substring(0,4)); //characters 0 to 4
  Serial.println(aString.endsWith("object"));
  newString = aString;
  newString.replace("e","_");
  Serial.println(newString);

  newString = aString;
  newString.toLowerCase(); //convert to lower case
  Serial.println(newString);

  newString = aString;
  newString.toUpperCase(); //convert to upper case
  Serial.println(newString);
  Serial.println(aString.equals("Another String")); //are teh strings equal
}

void loop(){
}
</pre>

Run this and you should see the following

<pre>
This is a Test String
21
i
This
0
This is a T_st String
this is a test string
THIS IS A TEST STRING
0
</pre>
