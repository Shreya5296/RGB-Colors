# RGB-Colors

RGB LED means red, blue, and green LEDs. RGB LED products combine these three colors to produce over 16 million hues of light except brown and pink.
Light-emitting diodes produce light by the movement of electrons between the two terminals of a diode, which occur by a process called electroluminescence. 
All these materials are made from semiconductors.

RGB LED:
RGB LEDs have four pins—one for each LED(RED, Green, Blue) and another for the common anode or cathode.
● R (red) pin: is to control the red color element
● G (green) pin: is to control the green color element
● B (blue) pin is to control the blue color elements
● Common Anode and Common Cathode RGB LEDs
● In a common cathode RGB LED, all three pins share a single negative connection (cathode).
● In a common anode RGB LED, the three pins share a common positive connection (anode)

Note: We are using common cathode RGB LED, so will connect with this GND

Step -1:Gather the material from the IoT kit:
● 1 x ESP32
● 1 x USB Cable
● 1 x Breadboard
● 4 x Jumper wires
● 1 x RGB LED
● 3 x 330 Ohm Resistors

Step -2: Let’s do connections:
● Insert RGB LED into a breadboard, insert four leg’s into breadboard
● The three positive leads of the LEDs (one red, one green, and one blue) are each connected to the 330-ohm resistors.
● The other end of the resistor will go to the ESP32 GPIO pins, D5, D18, D19 respectively.
● The common negative connection of the RGB LEDwhich is the second pin from the flat side of the LED package. It is also the longest of the four leads. 
This lead will be connected to ESP 32 GND pin

Step-3 Let’s write a code:
specify to which GPIO or GPIOs the signal will appear upon.
● define GPIO signal pins: LEDR pins 5, 18, 19
● define R_channel, G_channel, B_channel 0,1,2
● define pwm_Frequency 5000, PWM stands for Pulse Width Modulation which is used to check portion of the time the signal spends on versus the time that the signal spends off. PWM on-off pattern can simulate voltages in between the full Vcc of the board (e.g., 5 V/3.3 V on a and off (0 Volts) The duration of "on time" is called the pulse width.
● For an LED, PWM frequency is 5000 Hz
● defined as pwm_resolution 8,8-bit resolution, which means we can control the LED brightness using a value from 0 to 255.

Initialize using void setup() function
● ledcAttachPin function accepts two arguments. The first is the GPIO that will output the signal, and the second is the channel that will generate the signal.
● Set channel for all three colors and their, pwm frequency along with pwm_resolution.

To execute the main process write the void loop()
RGB (Red, Green, Blue) all colors have 8 bits each. The range for each individual color is 0-255 The combination range is 256*256*256.To display different colours we need to show variation between o to 255
● RGB_Color for RED (255,0,0)
● RGB_Color for Green(0.255,0)
● RGB_Color for Blue (0,0,255)
● RGB_Color for Yellow (255,255,0)
● RGB_Color for Cyan (0, 255,255)
● RGB_Color for magenta(255,0,255)
● RGB_Color for pink(255,0,147)
Make a loop pattern for all described colors using loops.
● ledCWrite function is used to control the LED brightness using PWM for R_channel, G_channel, B_channel

Output:
Compile and upload the program to ESP32 board using Arduino IDE
● Verify the program by clicking the Tick option
● Upload the program by clicking the arrow option

Note: If the port is not selected, insert the USB cable in Computer’s port and select the port

● You will see different colors on the LED
