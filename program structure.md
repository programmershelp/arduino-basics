The most basic Arduino sketch consists of two functions called setup() and loop(). 

The Arduino IDE once installed has a basic example that shows this. 

Open the Arduino IDE and select File → Examples → 01.Basics → BareMinimum to see the following in the IDE

<pre>
void setup() 
{ 
// put your setup code here, to run once: 
} 

void loop() 
{ 
// put your main code here, to run repeatedly: 
}
</pre>

The setup() function is called when a sketch starts. Use it to initialize variables, pins, start using libraries, etc. 

The setup function will only run once, after each power-up or reset of the Arduino board. Statements in the loop() function will run continuously from top to bottom and then back to the top. 

Lets you had 2 statements in your loop(), statement 1 would run first, and then statement 2, once statement 2 had completed you would go back to statement 1 again and so on.

### **Code example**

 
<pre>
void setup() 
{ 
  Serial.begin(9600); 
  Serial.println("*** We are in the setup loop ***");
  delay(2000); 
} 

void loop() 
{ 
  Serial.println("Now in main loop about to pause for 2 seconds."); 
  delay(2000); 
  Serial.println("This would be a statement or function"); 
  delay(2000); 
  Serial.println("Arduino now at bottom of main loop."); 
}
</pre>

Open the serial monitor and you should see the following

<pre>
\*\*\* We are in the setup loop ***
Now in main loop about to pause for 2 seconds.
This would be a statement or function
Arduino now at bottom of main loop.
Now in main loop about to pause for 2 seconds.
This would be a statement or function
Arduino now at bottom of main loop.
Now in main loop about to pause for 2 seconds.
This would be a statement or function
Arduino now at bottom of main loop.
Now in main loop about to pause for 2 seconds.
This would be a statement or function
Arduino now at bottom of main loop.
Now in main loop about to pause for 2 seconds.
This would be a statement or function
Arduino now at bottom of main loop
</pre>

As you can see the serial output in the setup() ran once and the other serial output will keep running  that is in the loop()
