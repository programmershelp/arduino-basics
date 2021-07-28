A do while loop is a control flow statement that executes a block of code at least once, and then either repeatedly executes the block or it stops executing depending on the condition at the end of the block. 

The do while construct consists of a process symbol and a condition. 
First of all, the code within the block is executed, and then the condition is evaluated. 

If the condition is true the code within the block is executed again. This repeats until the condition becomes false. 

Because do while loops check the condition after the block is executed, the control structure is often also known as a post-test loop. When you compare this to the while loop, which tests the condition before the code within the block is executed, the do-while loop is an exit-condition loop. 

This means that the code must always be executed first and then the expression or test condition is evaluated. 

If it is true, the code executes the body of the loop again. This process is repeated as long as the expression evaluates to true. 

If the expression is false, the loop terminates and control transfers to the statement following the do-while loop. 

It is possible for the condition to always evaluate to true which is called an infinite loop. 

When such a loop is created on purpose, there is normally another control structure like a break statement that allows termination of the loop.

**So here it is in its most basic form**  
<pre>
do {
Statement 1
Statement 2
...
} while (test expression);
</pre>

So if you want to run the code at least one you would pick a do while loop 
  
**Let's see this in action**

### Example 1: serial output

The following example will simply output to the serial monitor window
<pre>
void setup()
{
int i = 1;

  Serial.begin(9600);

  do
  {
    Serial.print("i = ");
    Serial.println(i);
    i++;
    }while(i<=10);
 }

void loop() 
{
}
</pre>

Open the serial monitor window and you should see something like this
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

Let's remove the i++ from the code above and run again and look at the serial monitor window

<pre>
i = 1
i = 1
i = 1
i = 1
i = 1
i = 1
i = 1
i = 1
i = 1
i = 1
i = 1
i = 1
i = 1
</pre>

As you can see because the variable wasn't incremented then the test expression will always be true, it will always be less than or equal to 10. 

Now you have an Infinite loop.

### Example 2 : flashing something

Again if you do not have an RGB LED then you can continue experimenting with the above example but if you want to build something then here we go. ![](http://www.aboutmicros.com/wp-content/uploads/2020/09/Arduino-Uno-and-RGB-LED.png)  

#### Example 1: flash the red led 10 times

Again in this example we will flash the red part of the RGB led 10 times, you can change the number, or even change to the blue led or green led by changing the pin number to 9 or 10

<pre>
//flash the red led of the RGB led 10 times
int redled = 11;
int i = 1; //init the variable

void setup()
{
  Serial.begin(9600);
  pinMode(redled, OUTPUT); //set the LED pin as an output
  //this will run 10 times
  do
  {
    Serial.print("loop = ");
    Serial.println(i);
    digitalWrite(redled, LOW); // led on
    delay(500);
    digitalWrite(redled, HIGH); //led off
    delay(500);
    i++; //dont forget this
  }while(i<=10);
}

void loop()
{
}
</pre>

#### Example 2: fading the led

<pre>

//change the brightness of an LED
int redled = 11;
int i =1;

void setup()
{
  pinMode(redled, OUTPUT); //set the LED pin as an output
  Serial.begin(9600);
  do{
    Serial.print("loop = ");
    Serial.println(i);
    analogWrite(redled, i);
    delay(10);
    i++;
  }while(i<=255);
}

void loop()
{
}
</pre>
