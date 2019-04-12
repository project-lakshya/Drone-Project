# REPORT
*Name  : Rishitha*

*Reg no. 180903004*

**Raspberry pi**

Differently used versions of raspberry pi are R-pi zero,
raspberry pi 3+,raspberry pi 3B+ which is the presently used.

It has a broadcom microcontroller which is a ARM based processor i.e. ARM Cortex A7 the latest one.

ARM is a company which designs the chip but doesn't manufacture.

It has 40 input output pins, 4 USB ports(one for the power i.e to charge).
It has an audio port,camera connector,HDMI (a mutlimedia interface between board and monitor) for monitor.
It has a micro SD slot which is seen on the backside of the board
to install the operating system using the NOOBS(new out of box software) which is 
the major difference between between arduino and R-pi.

**Comparision between Raspberry pi and Arduino**

**Raspberry pi**                                                      
1. Its processor is faster with a speed of almost 1.2GHz                
2. 64 bit processor implying that it can be used                        
   for ver accurate outputs.
3. More memory because of difference in SRAM and mainly                 
   because of micro SD slot.
4. Power sensitive.If too much power drawn it will reboot               
5. It has an operating system beacuse of which multiple programs can be run at the same 
   time which means it keeps on swapping among different programs very fast.

**Arduino**
1.The speed of its processor is 16MHz only.

 2. 8 bit processor.Not very accurate.  
 
 3.Less memory.
 
 4.Major advantage is it is not sensitive to all this.
 
 5.Single program can be run.

**Benifits of Operating system**
R-pi gives a user interface which is not the case with arduino.

We can interact and make changes without writing code everytime to carryout an operation.

Text user and graphic user interface are the 2 types.

In text interface after the prompt on the screen we just have to write our commands for the desired output.

And there are device drivers which act as translator between hardware device and operating system that use it.

**Overclocking**

Different parts of the chip run at different frequency.
Overclocking is the process of increasing the clock frequency i.e time taken to reach the next clock edge is reduced.

# Linux

***Text user interface***
Shell-It reads the user input and displays on the screen.

BASH-default shell for Raspian.

man pwd gives the information about a command like how to use it.

Linux filesystem is a hierarchy of directories(it simply means folder).

**Commands**

pwd-current directory location

cd-change directory

Ls-contents of the directory

ls-l -details about all the directories under a current directory

mkdir-creates a directory

rmdir-removes a directory

sudo-root permission to a command

ps-gives all the processes being performed

kill-kills the process

shutdown

**Creating and accesing a file**

Using text editor and nano helps to access a file

cat-to print contents in file

head,body-to print the first and last 10 lines of the file

cp-copy(takes 2 arguments)

mv-move

**File permissions**

R,W,X-read ,write ,execute

Permissions for user refers to owner

group refers to group of people

others refers to everyone else

***Graphical user interface***

startx-to start the GUI window system

***General purpose input output pins***
On the R-pi board it has 
several input output pins for general purposes or they can be multifunctional 
Ex: UART_(TX)/(RX)D 
It has several ground pins,two 3.3V pins and two 5V pins
Pins 3(SDL) and 5(SCL) used for I2C communication

SPI i.e. Serial Parallel Interface is also communication protocol which requires 4 pins atleast

MOSI-Master Out Slave In(pin 19)
MISO-Master In Slave Out(pin 21)
2 chip enabled pins to indicate the slave that master is communicating with it (ins 24 and 26)

**Accessing GPIO pins using python**

Import the GPIO library i.e. Rpi.GPIO.
To use the pin number in program it can be done in 2 ways:
1. Numbering according to the pin number on board.
   GPIO.BOARD
   
2. Using Broadcom SoC .(SoC-System on chip)
   GPIO.BCM
   Numbers assigned based on the number in pin name
   
GPIO.setup(pin_number,GPIO.IN/OUT)

GPIO.output(pin_number,true/false)

GPIO.input(pin_number)

Creating an object for generating a square wave

pwm_obj=GPIO.PWM(pin_number,frequency)

pwm_obj.start(duty_cycle)

the signal remains low or high from 0 to that argument depending on duty cycle.

To change the duty cycle 

pwm_obj.ChangeDutyCycle(argument)

**Using GUI interface**

All the classes have to be imported from Tkinter library.

from Tkinter import *

An object of Tk() function should be created.

Then ceate a canvas and any desired shapes can be drawn.

