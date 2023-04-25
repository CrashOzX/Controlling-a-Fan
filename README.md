# Microprocessors 2 - Lab 3: Controlling a Fan

This code is for the third lab assignment in the Microprocessors 2 course. It controls a fan using an Arduino board, and includes features such as changing the fan speed and direction, displaying the time on an LCD screen, and using a button to change the fan's direction.

## Getting Started

To use this code, you will need an Arduino board and the necessary components to set up the fan, LCD screen, and button as described in the lab instructions. You will also need to install the required libraries:

- `Wire.h`
- `RTClib.h`
- `LiquidCrystal.h`

## Usage

Once you have set up your Arduino board and the components, upload the code to the board using the Arduino IDE. The code will control the fan's speed and direction, display the time on the LCD screen, and allow you to change the fan's direction using the button.

## Code Explanation

The code includes several constants and variables that are used to control the fan and display the time on the LCD screen. Here is a brief explanation of some of the key parts of the code:

- `FAN_STRS` and `FAN_SPEEDS`: these arrays are used to define the different fan speeds and their corresponding values (in percentage of maximum speed).
- `speed_up`: a boolean variable that is used to determine whether the fan speed should be increased or decreased.
- `speed_index`: an integer variable that is used to track the current fan speed (as an index of `FAN_SPEEDS`).
- `state`: a boolean variable that is used to track the current direction of the fan.
- `update_display()`: a function that updates the LCD display with the current time and fan speed/direction.
- `set_speed()`: a function that sets the fan speed based on the `FAN_SPEEDS` array.
- `button_interupt()`: an interrupt service routine that is triggered when the button is pressed, and changes the direction of the fan.

The main loop of the code checks the current time and changes the fan speed/direction if necessary. The fan is also turned off for 30 seconds at the start of each minute.
