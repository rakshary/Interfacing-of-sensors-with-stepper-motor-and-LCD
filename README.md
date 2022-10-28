# Interfacing-of-sensors-with-stepper-motor-and-LCD
BEHAVIOR 
Through the code we control the behavior of the stepper motor based on the temperature and humidity conditions and display the results using LCD. 
The library functions to use LCD, temperature and humidity sensor, and the stepper motor is called in the program. The temperature sensor pin is then defined and a dht variable is created. 
The library is initialized by associating LCD interface pin with the Arduino pin number it is connected with. 
The values to control steps per revolution is set to 200, and to control motorspeed is set to 10.
Stepper function is called and defined with a variable while specifying stepsperrevolution, and digital pins 10,7,9,13 of Arduino to set it up with the stepper motor.
6 variables are defined for the led and it is then connected to the Arduino with the digital pins.
In the setup section, the LCD’s number of columns and rows are setup. 
Serial.begin(9600) starts serial communication so that Arduino can send out commands through the USB connection, while 9600 is the baud rate, which determines how fast the data is to be sent. The motor speed is set. 
In the loop section, the LCD cursor is set to (0,0) and “Temp and Humid “message is printed. The LCD cursor is then set to (0,1) and “Detection” message is printed. A delay of 3 seconds is given and then the temperature sensor is read. The LCD is cleared and then set back to (0,0). The temperature value is then displayed on the LCD.  The cursor is then set to (0,1) and the humidity value is displayed. There is a delay of 3 seconds given, and then the display is cleared.
