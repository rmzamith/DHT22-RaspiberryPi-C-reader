# DHT22-RaspiberryPi-C-reader
Program that reads the data from an DHT22 sensor on a Raspberry Pi using C language with the [WiringPi](http://wiringpi.com/) library.

## Dependencies
For this project you will need:
* One RaspberryPi of any model.
* One DHT22 sensor: [Datasheet1](https://cdn-shop.adafruit.com/datasheets/Digital+humidity+and+temperature+sensor+AM2302.pdf), [Datasheet2](https://www.sparkfun.com/datasheets/Sensors/Temperature/DHT22.pdf)
* GCC installed for code compilation.
* WiringPi installed on your raspberry. Details on how install it [here](http://wiringpi.com/download-and-install/).

## Hardware Installation
In the default configuration of the project, you should connect the sensor pins to Raspberry like this:  
![alt tag](https://raw.githubusercontent.com/rmzamith/DHT22-RaspiberryPi-C-reader/master/dht22.png)  

The resistor is a 10KΩ with +-5% tolerance.  
You can change the data pin, but make sure you change it on the code too.  
Use the WiringPi pin numeration. See the pin numbers by executing this command in shell `gpio readall`.  On the default code, we are using GPIO 12, that is equivalent to the WiringPi pin number 26.

## Software Compilation
To compile, execute the folowing:  
`sudo gcc -odht22.out DHT22.c -lwiringPi`

## Software Execution
After compiled, you should run the compiled artifact this way:  
`sudo ./dht22.out`


There`s a know issue for negative temperatures. I`m looking forward to fix it.
