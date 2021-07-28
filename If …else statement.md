An if statement can be followed by an optional else statement, which executes when the expression is false. 

**Syntax** 

The syntax of an if...else statement is
<pre>
if(expression) 
{ 
/\* statement(s) will execute if the expression is true */ 
} 
else 
{ 
/\* statement(s) will execute if the expression is false */ 
}
</pre>

If the expression evaluates to true, then the if block will be executed, otherwise, the else block will be executed. else can proceed another if test, so that multiple, mutually exclusive tests can be run at the same time. 

Each test will proceed to the next one until a true test is encountered. When a true test is found, its associated block of code is run, and the program then skips to the line following the entire if/else construction. 

If no test proves to be true, the default else block is executed, if one is present, and sets the default behavior. Note that an else if block may be used with or without a terminating else block and vice versa. 

An unlimited number of such else if branches are allowed. 

Let's look at some examples

#### **Code**

<pre>
void setup() 
{ 
  int i = 1; 
  Serial.begin(9600); 
  while(i<=10) 
  { 
    if(i >=5 ) 
    {  
      Serial.print("if (true) = "); 
      Serial.println(i); 
    } 
    else 
    { 
      Serial.print("else (false) = "); 
      Serial.println(i); 
    } i++;
  }
} 
  
void loop() 
{ 
}
</pre>

Open the serial monitor and you will see the following

<pre>
else (false) = 1
else (false) = 2
else (false) = 3
else (false) = 4
if (true) = 5
if (true) = 6
if (true) = 7
if (true) = 8
if (true) = 9
if (true) = 10
</pre>

#### Example 2

In this example we use the built-in LED on the Arduino, when we send an 'a' via the serial monitor the led will switch on, and if you send any other character the led will switch off

<pre>
void setup() 
{
  Serial.begin(9600);
  pinMode(13, OUTPUT);
}

void loop() 
{
  char rx_byte;
  
  if (Serial.available() > 0) 
  {
    rx_byte = Serial.read();
    if (rx_byte == 'a') 
    {
      // switch the LED on if the character 'a' is received
      digitalWrite(13, HIGH);
    }
    else 
    {
      // switch the LED off if any character except 'a' is received
      digitalWrite(13, LOW);
    }
  }
}
</pre>
