The condition is evaluated, and if the condition is true, the code within all of their following in the block is executed. 

This repeats until the condition becomes false. 

Because the while loop checks the condition before the block is executed, the control structure is often also known as a pre-test loop.

Compare this with the do while loop, which tests the condition after the loop has executed. 

**Let us look at a basic C example**

<pre>
int x = 0;

while (x < 5)
{
printf ("x = %d\\n", x);
x++;
}
</pre>

This first checks whether x is less than 5, which it is, so then the {loop body} is entered, where the printf function is run and x is incremented by 1. 
  
After completing all the statements in the loop body, the condition, (x < 5), is checked again, and the loop is executed again, this process repeating until the variable x has the value 5. 

**Note** 

That it is possible for the condition to always evaluate to true, this creates what is known as an infinite loop. 

When such a loop is created intentionally, there is usually another control structure (such as a break statement) that controls termination of the loop. 

For example:
<pre>
while (true)
{
if (someCondition)
break;
// continue with rest of program
}
</pre>
Now let's look at some Arduino related examples, the first one requires no extra hardware

#### Example 1 : serial monitor example
 
<pre>
void setup() 
{ 
  int i = 1; 
  Serial.begin(9600); 
  
  while(i<=10) 
  { 
    Serial.print("i = "); 
    Serial.println(i); 
    i++; 
  } 
} 

void loop() 
{ 
}
</pre>

As you can see we set the variable to 1, we then test whether the variable is less than or equal to 10. 

If it is not then the statements will run in the brackets which are basically outputting this value via the serial monitor. 

The important part is that we increment the variable using i++. 

This increments the value of the variable by 1, this is the same incidentally as writing i = i + 1; which is sometimes used as well. 

Forgetting this would cause the while loop to always run - this is would be an infinite loop. 

You can remove the i++ and see what happens. Open the serial monitor and you will see something like this
<pre>
i = 1
i = 2
i = 3
i = 4
i = 5
i = 6
i = 7
i = 8
i = 9
i = 10
</pre>

#### Example 2: flashing something example

If you want to start building something then here is a simple example, if not then you can keep experimenting simply outputting to the serial monitor like the example above 

Let us look at an example where we connect an RGB LED to an Arduino Uno You will need to connect up the RGB led like this for the following examples. 

This particular RGB led example is a common anode type, you need to watch as you can get common anode types which require to be connected to the ground rather than 5v.

If you have one of these the code would need to be adapted. ![](http://www.aboutmicros.com/wp-content/uploads/2020/09/Arduino-Uno-and-RGB-LED.png)  

#### Code example 1

This first example would flash the red led of the RGB led ten times
<pre>
//flash the red led of the RGB led 10 times 
int redled = 11; 
int i = 1; //init the variable 

void setup() 
{ 
  Serial.begin(9600); 
  pinMode(redled, OUTPUT); //set the LED pin as an output 
  
  //this will run 10 times 
  while(i<=10) 
  { 
    Serial.print("loop = "); 
    Serial.println(i); 
    digitalWrite(redled, LOW); // led on 
    delay(500); 
    digitalWrite(redled, HIGH); //led off 
    delay(500); 
    i++; //dont forget this 
  } 
} 
  
void loop() 
{
}
</pre>

#### Code Example 2

This example will fade the red led Let's talk about the analogWrite function

`analogWrite(pin, value)`

`pin`: the Arduino pin to write to. Allowed data types: `int`. `value`: the duty cycle: between 0 (always off) and 255 (always on). Allowed data types: `int`. 

So we set this to 255 in the while loop and we decrement the count by 1 which in turn makes the LED appear to fade

<pre>
//change the brightness of an LED 
int redled = 11; 
int i =0; 

void setup() 
{ 
  pinMode(redled, OUTPUT); //set the LED pin as an output 
  Serial.begin(9600); 
  while(i<=255) 
  { 
    Serial.print("loop = "); 
    Serial.println(i); 
    analogWrite(redled, i); 
    delay(10); 
    i++; 
  } 
}

void loop() 
{ 
  
}

</pre>
