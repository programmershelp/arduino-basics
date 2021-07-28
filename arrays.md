An array is a group of the same kind of data that are placed consecutively in memory. 

You can have an array of integers which are two or more integer numbers occurring one after the other. 

An element in an array refers to each value in the array. If we have an array of integers, then each individual integer is referred to as an element of the array. 

To refer to a particular location or element in the array, we specify the name of the array and the position number of the particular element in the array. 

The key here is that each element in an array is placed directly after the previous element which allows us to access each element, in turn, using a loop.

### Arduino Example 1

<pre>
void setup() 
{
  int sample_array\[3\];     // an array with 3 integer elements
  int i;               // used as an index into the array
  
  Serial.begin(9600);
  
  sample_array\[0\] = 25;    // assign a value of 25 to the 1st element
  sample_array\[1\] = 12;  // assign a value of 12 to the 2nd element
  sample_array\[2\] = 1995; // assign a value of 1995 to the 3rd element
  
  // display each number from the array
  for (i = 0; i < 3; i++) 
  {
    Serial.println(sample_array\[i\]);
  }
}

void loop() 
{
}
</pre>

You would see this in the serial monitor
<pre>
25
12
1995
</pre>
Let's break this down

#### Defining the Array

In the example above, we define an array which contains 3 elements. This makes space in memory for 3 integers that are put in the memory one after the other. 

The values that each element contains after the array is defined can contain any random data that is in memory at that time.

#### Defining an array of 3 integers:

int sample_array\[3\]; // an array with 3 integer elements

In this example the array is of type int, you can use other data types such as float, char etc The array has a name which is sample_array in the example.

#### Assigning Values to Elements in the Array

Each element is assigned an integer value by referencing it using square brackets \[\] with the number of the element to access in the brackets.

<pre>
sample_array\[0\] = 25; // assign a value of 25 to the 1st element
sample_array\[1\] = 12; // assign a value of 12 to the 2nd element
sample_array\[2\] = 1995; // assign a value of 1995 to the 3rd element
</pre>

Please be aware that the numbering starts from 0 and not 1

In the same way, the last element in the array is numbered one less than the size of the array. 

In the example above, the size of the array is 3, so the number of the last element is 2. 

This is something you have to be careful about when using arrays

#### Accessing an Array in a Loop

You can use a for loop to get the contents of each element in the array.

<pre>
for (i = 0; i < 3; i++) 
{
Serial.println(sample_array\[i\]);
}
</pre>

In the example above we display all the values via the serial monitor window 

The variable i is used in the for loop as an index into the array to access each element of the array. 

In the loop, i is then initialized to 0 and then incremented by one each time through the loop so that it counts from 0 to 2. 

The loop is exited when i becomes 3. The i variable is used in the array to get the value that the array element is holding starting with element 0 and ending with 4.

### Arduino Example 2

You can actually the elements of an array can also be initialized in the array declaration by following the array name with an equal-to sign and a brace-delimited comma-separated list of initializers. 

Let's re-write the first example to show this  

<pre>
void setup() 
{
  int sample_array\[3\] = {25,12,1995};     // an array with 3 integer elements
  int i;               // used as an index into the array
  
  Serial.begin(9600);
  
  // display each number from the array
  for (i = 0; i < 3; i++) 
  {
    Serial.println(sample_array\[i\]);
  }
}

void loop() {
}
</pre>

As you can see we now have the following

int sample_array\[3\] = {25,12,1995}; // an array with 3 integer elements
