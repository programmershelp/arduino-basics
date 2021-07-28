In this article we will look at the If statement if, which is used in conjunction with a comparison operator, tests whether a certain condition has been reached, such as an input being above a certain number. 

If the expression evaluates to true, then the block of code inside the 'if' statement will be executed. The syntax of the if statement is as follows:

<pre>
if (expression > 50)
{
// do something here
}
</pre>

The program tests to see if expression is greater than 50. If it is, the program takes a particular action. 

Put another way, if the statement in parentheses is true, the statements inside the brackets are run. If not, the program skips over the code. 

The brackets may be omitted after an if statement. If this is done, the next line (defined by the semicolon) becomes the only conditional statement. 

The following examples are all valid ways of writing an if statement  

<pre>
if (x > 120) digitalWrite(LEDpin, HIGH);

if (x > 120)
digitalWrite(LEDpin, HIGH);

if (x > 120){ digitalWrite(LEDpin, HIGH); }

if (x > 120){
digitalWrite(LEDpin1, HIGH);
digitalWrite(LEDpin2, HIGH);
}
</pre>

My personal preference is to use the following approach, even if there was only a statement to be executed, it is only best to be consistent and use the same approach in all of your code.

<pre>
if (x > 120)
{
digitalWrite(LEDpin1, HIGH);
}
</pre>

#### **Code Examples**

Let's look at a code example, this uses a while loop and will run 10 times. 

In our if statement we will only run the statements in the brackets which output via the serial monitor if the value of i is less than or equal to 5

<pre>
void setup()
{
  int i = 1;
  Serial.begin(9600);
  while(i<=10)
  {
    if(i <=5 )
    {
      Serial.print("i = ");
      Serial.println(i);
    }
  i++;
  }
}

void loop() {
}
</pre>

Compile and run the serial monitor, you will see the following

<pre>
i = 1
i = 2
i = 3
i = 4
i = 5
</pre>

You can use other comparison operators as well. Change the code to the following and run again. 

This one will only run the statements in the brackets if the value of i is equal to 5  

<pre>
void setup()
{
  int i = 1;

  Serial.begin(9600);
  while(i<=10)
  {
    if(i ==5 )
    {
      Serial.print("i = ");
      Serial.println(i);
    }
    i++;
  }
}

void loop() {
}
</pre>

This time in the serial monitor window you will see the following

<pre>
i = 5
</pre>

Now change the code to the following and run again. This one will only run the statements in the brackets if the value of i is greater than or equal to 5  

<pre>
void setup()
{
  int i = 1;

  Serial.begin(9600);
  while(i<=10)
  {
    if(i >=5 )
    {
      Serial.print("i = ");
      Serial.println(i);
    }
    i++;
  }
}

void loop() {
}
</pre>

This time in the serial monitor window you will see the following

<pre>
i = 5
i = 6
i = 7
i = 8
i = 9
i = 10
</pre>

We have shown you some comparison operators above, here is a list of comparison operators you can use.
<pre>

x == y (x is equal to y)
x != y (x is not equal to y)
x < y (x is less than y)
x > y (x is greater than y)
x <= y (x is less than or equal to y)
x >= y (x is greater than or equal to y)
</pre>

Later on, you will see that you can also use other operators such as boolean operators as well

<pre>
if (digitalRead(2) == HIGH && digitalRead(3) == HIGH)
{
//statements to be run here only if both conditions are met
}
</pre>
