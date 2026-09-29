# Tamagotchi_Book_Nook
Embedded systems project with pixel animations, touch sensors, and various functions

## Key Features:
* Uses state machine to create the illusion of the bottom animation interacting with the top
* The duck animation reacts to inputs from touch sensors
* Animations stored in arrays are included (please credit if using the artwork)
* A total of 6 food animations are stored and can be randomly switched with the GPIO 3 button
* NOT YET IMPLEMENTED: the oled display will be used as a menu with a pomodoro timer with sensors to put your phone down

## Materials List:
* Raspberry Pi Pico 2W microcontroller and wire
* 0.96in OLED display (this can be left off for now, but new functionality will be added soon)
* Two ST7789 LCD TFT Displays 240*320 (these will function as the upper and lower windows of the book nook)
* Two capacitive touch sensors (one beside each LCD display)
* 2+ push buttons
* Jump wires and breadboard OR soldering materials

## How to Use:
* In the Arduino IDE, download the relevant Adafruit graphics libraries listed at the top of the code
* Wire the components according to 3.3V, ground, and the pin numbers listed at the top of the code (additional wiring schematic for ease will be added soon)
* Upload code onto the microcontroller
* Enable LCD displays by clicking the GPIO 2 button
* Randomly switch between food animations by clicking the GPIO 3 button

## Additional:
* If you would like to create and upload your own pixel animations from Aseprite, consider this Lua script to convert it to a usable C array:
  * [Aseprite to C Array Converter](https://github.com/qingxin-xia/Aseprite_C_Array_Converter)
  * NOTE: currently the animation size for a single display is 52 * 39 and is enlarged by a factor of 6 in the code
    * If you would like to customize with personal animations, keep in mind to change the scale argument in drawIndexedFrame(), the height/width constants, Display_Backround_Color, and state machine logic detailed in the code comments

