There are four different time manipulation functions. They are delay() delayMicroseconds() micros() millis() Lets look at these

### delay()

This function pauses the program for the specified amount of time (in milliseconds) 

This is the common flash an LED on and off example which uses 2 delays of 1000 milliseconds

<pre>
int ledPin = 13; // LED connected to digital pin 13

void setup()
{
pinMode(ledPin, OUTPUT); // sets the digital pin as output
}

void loop()
{
digitalWrite(ledPin, HIGH); // sets the LED on
delay(1000); // waits for a second
digitalWrite(ledPin, LOW); // sets the LED off
delay(1000); // waits for a second
}
</pre>
   

### delayMicroseconds()

This function will pause the program for the amount of time (in microseconds) 

This function works accurately in the range 3 microseconds and up and the largest value that will produce an accurate delay is 16383, after that you should use the delay function above  

<pre>
int outPin = 8; // pin 8

void setup()
{
pinMode(outPin, OUTPUT); // sets the digital pin as output
}

void loop()
{
digitalWrite(outPin, HIGH); // sets the pin on
delayMicroseconds(1000); // pauses for 1000 microseconds
digitalWrite(outPin, LOW); // sets the pin off
delayMicroseconds(1000); // pauses for 1000 microseconds
}
</pre>

I've seen examples which flash the built-in LED for 1 second, these are incorrect and let's look why this is. 

There are a thousand microseconds in a millisecond and a million microseconds in a second. 

So you would need delayMicroseconds(1000000), but remember that 16383 is the maximum guaranteed value that will give you accurate delay  

### micro ()

Returns the number of microseconds since the Arduino board began running the current program. 

This number will overflow (go back to zero), after approximately 70 minutes. 

On 16 MHz Arduino boards, this function has a resolution of four microseconds (i.e. the value returned is always a multiple of four). 

On 8 MHz Arduino boards, this function has a resolution of eight microseconds  

<pre>
unsigned long time;

void setup()
{
Serial.begin(9600);
}

void loop()
{
Serial.print("Time: ");
time = micros();

Serial.println(time); //prints time since program started
delay(1000); // delay a second
}
</pre>


This is what I saw in the serial monitor

<pre>
Time: 56
Time: 1000224
Time: 2000620
Time: 3001020
Time: 4001416
Time: 5001808
Time: 6002204
Time: 7002596
Time: 8002988
</pre>

### millis()

Returns the number of milliseconds passed since the Arduino board began running the current program. 

This number will overflow (go back to zero), after approximately 50 days. 

<pre>
unsigned long time;
void setup()
{
Serial.begin(9600);
}

void loop()
{
Serial.print("Time:");
time = millis();
//prints time since program started
Serial.println(time);
// wait a second so as not to send massive amounts of data
delay(1000);
}
</pre>

Open the serial monitor and you will see something like this

<pre>
Time:0
Time:999
Time:1999
Time:3000
Time:4000
Time:5000
Time:6000
Time:7001
</pre>
