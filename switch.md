A switch case is used to control the flow of a program by allowing programmers to specify different code that should be executed in various conditions. 

In particular, a switch statement compares the value of a variable to the values specified in case statements. 

A switch statement is written across many individual lines using one or two keywords. 

A typical syntax involves: the first select, followed by an expression which is often referred to as the control expression or control variable of the switch statement subsequent lines defining the actual cases, with corresponding sequences of statements for execution when a match occurs a break statement typically follows a case statement to end said statement. 

Each alternative begins with the particular value, or list of values , that the control variable may match and which will cause the control to goto the corresponding sequence of statements. 

The value (or list/range of values) is usually separated from the corresponding statement sequence by a colon or by an implication arrow. 

In many languages, every case must also be preceded by a keyword such as case 

An optional default case is typically also allowed, specified by a default keyword. 

This executes when none of the other cases match the control expression.

In C if no case matches and the default is omitted the switch statement simply exits 

In the example below the expression can be an integer expression or a character expression.  

<pre>
switch (var) 
{
  case label1:
    // statements
    break;
  case label2:
    // statements
    break;
  default:
    // statements
    break;
}
</pre>
   

### Arduino Serial example

In this example we read value via the serial port and depending on the character that is received we use a switch...case to display a string via the serial port depending on the input 

When you type in a character such as 1 the switch statement will check to see if there is a matching case. 

It will see that there is a 1 and then display the You selected 1 message on the serial monitor window. 

The next break statement is used to break out of the switch statement which means we are basically awaiting the next character to be entered to evaluate.

<pre>
void setup() 
{
  Serial.begin(9600);
}

char rx_byte = 0;

void loop() {
  if (Serial.available() > 0) 
  {    
    // is a character available?
    rx_byte = Serial.read();
  
    switch (rx_byte) 
    {
      case '1':
        Serial.println("You selected 1");
      break;
      
      case '2':
        Serial.println("You selected 2");
      break;
      
      case '3':
        Serial.println("You selected 3");
      break;
      
      default:
        Serial.println("Invalid option selected");
      break;
    } 
  }
}
</pre>

Compile and run this example, open the serial monitor and send some sample data. 

This is a trial run that I had

<pre>
You selected 1
You selected 2
You selected 3
Invalid option selected
Invalid option selected
You selected 3
You selected 2
You selected 1
You selected 1
</pre>
