In this tutorial, we download the software and connect your Arduino and get your development started. 

Lets go.

### Download software

The first step is to download the software required, you can get the IDE from https://www.arduino.cc/en/Main/Software 

There are versions for Windows, Mac OS, and Linux. I always choose the Windows ZIP file for non-admin install which is a 192mB download in size, so depending on your internet connection speed may take some time. 

At the time of writing the Arduino IDE, version is 1.8.13

### Install Software

Now locate the zip file on your computer and unzip it. I usually choose a folder like D:\\Arduino. 

After the zip file extraction is complete you should open the folder that has been created and you should see a collection of folders and files. 

At this stage I create a portable folder - this is optional. 

You should see something like this 

![arduino folder structure](http://www.aboutmicros.com/wp-content/uploads/2020/09/arduino-folder-structure.jpg "arduino folder structure")

Now click on the arduino.exe to start the IDE.

#### Power Up and connect your board

Now I would recommend you connect your board to your PC depending on what you have purchased you will need a USB cable from the board to the PC, the types of these vary. 

This is why I would recommend buying an Arduino that already comes with a cable. 

When you connect the board to the operating system of your computer will look for drivers, it should find the right drivers since you installed the IDE software. 

If you have bought a clone board you may have to install another USB to serial driver but that should work OK. 

I have never had an issue with the above and common USB to serial chips on cheap clone boards are CH340 and CP2102s

### Load an example and setup your board

The typical beginner's part is to load one of the built-in examples that flash the led on the board. 

Click on File -> Examples -> 01.Basics -> This is what you should see 

![](http://www.aboutmicros.com/wp-content/uploads/2020/09/blink-example.jpg) 

The blink example will appear in the code window.  

<pre>
// the setup function runs once when you press reset or power the board
void setup() {
  // initialize digital pin LED_BUILTIN as an output.
  pinMode(LED_BUILTIN, OUTPUT);
}

// the loop function runs over and over again forever
void loop() {
  digitalWrite(LED_BUILTIN, HIGH);   // turn the LED on (HIGH is the voltage level)
  delay(1000);                       // wait for a second
  digitalWrite(LED_BUILTIN, LOW);    // turn the LED off by making the voltage LOW
  delay(1000);                       // wait for a second
}
</pre>

  Now let's select the board and com port. 
  
  In the example below I have an Arduino Mega connected - always select the correct board or you will get errors. 
  
  Go to Tools and then click on Board and depending on the IDE version you will see a menu like this - older versions have a list. 
  
 ![board selection](http://www.aboutmicros.com/wp-content/uploads/2020/09/board-selection.jpg "board selection")
  
  Now select the USB port of your board, in Windows, you can use the device manager to confirm the port like this 
  
  ![device manager](http://www.aboutmicros.com/wp-content/uploads/2020/09/device-manager.jpg "device manager")
  
  In the screenshot, you can see that this is a clone board so it is USB-SERIAL CH340 (COM10). So set the com port to 10 
  
  ![usb port selection](http://www.aboutmicros.com/wp-content/uploads/2020/09/usb-port.jpg "usb port selection")

#### **Upload your sketch**

Click on the upload button and the sketch will compile and all going well be uploaded to your board. 

You should see the led on the board switching on and offIn this tutorial, we download the software and connect your Arduino and get your development started. 

Lets go.

### Download software

The first step is to download the software required, you can get the IDE from https://www.arduino.cc/en/Main/Software 

There are versions for Windows, Mac OS, and Linux. I always choose the Windows ZIP file for non-admin install which is a 192mB download in size, so depending on your internet connection speed may take some time. 

At the time of writing the Arduino IDE, version is 1.8.13

### Install Software

Now locate the zip file on your computer and unzip it. I usually choose a folder like D:\\Arduino. 

After the zip file extraction is complete you should open the folder that has been created and you should see a collection of folders and files. 

At this stage I create a portable folder - this is optional. 

You should see something like this 

![arduino folder structure](http://www.aboutmicros.com/wp-content/uploads/2020/09/arduino-folder-structure.jpg "arduino folder structure")

Now click on the arduino.exe to start the IDE.

#### Power Up and connect your board

Now I would recommend you connect your board to your PC depending on what you have purchased you will need a USB cable from the board to the PC, the types of these vary. 

This is why I would recommend buying an Arduino that already comes with a cable. 

When you connect the board to the operating system of your computer will look for drivers, it should find the right drivers since you installed the IDE software. 

If you have bought a clone board you may have to install another USB to serial driver but that should work OK. 

I have never had an issue with the above and common USB to serial chips on cheap clone boards are CH340 and CP2102s

### Load an example and setup your board

The typical beginner's part is to load one of the built-in examples that flash the led on the board. 

Click on File -> Examples -> 01.Basics -> This is what you should see 

![](http://www.aboutmicros.com/wp-content/uploads/2020/09/blink-example.jpg) 

The blink example will appear in the code window.  

<pre>
// the setup function runs once when you press reset or power the board
void setup() {
  // initialize digital pin LED_BUILTIN as an output.
  pinMode(LED_BUILTIN, OUTPUT);
}

// the loop function runs over and over again forever
void loop() {
  digitalWrite(LED_BUILTIN, HIGH);   // turn the LED on (HIGH is the voltage level)
  delay(1000);                       // wait for a second
  digitalWrite(LED_BUILTIN, LOW);    // turn the LED off by making the voltage LOW
  delay(1000);                       // wait for a second
}
</pre>

  Now let's select the board and com port. 
  
  In the example below I have an Arduino Mega connected - always select the correct board or you will get errors. 
  
  Go to Tools and then click on Board and depending on the IDE version you will see a menu like this - older versions have a list. 
  
  ![board selection](http://www.aboutmicros.com/wp-content/uploads/2020/09/board-selection.jpg "board selection")
  
  Now select the USB port of your board, in Windows, you can use the device manager to confirm the port like this 
  
  ![device manager](http://www.aboutmicros.com/wp-content/uploads/2020/09/device-manager.jpg "device manager")
  
  In the screenshot, you can see that this is a clone board so it is USB-SERIAL CH340 (COM10). So set the com port to 10 
  
  ![usb port selection](http://www.aboutmicros.com/wp-content/uploads/2020/09/usb-port.jpg "usb port selection")

#### **Upload your sketch**

Click on the upload button and the sketch will compile and all going well be uploaded to your board. 

You should see the led on the board switching on and off
