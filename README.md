# Servo Control Project using Adafruit PWM Servo Driver

This project demonstrates how to control multiple servos using the Adafruit PWM Servo Driver (`Adafruit_PWMServoDriver.h`). The code allows precise control of servo positions through the I2C communication protocol, enabling smooth movement sequences for various applications like robotics or automation.

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Hardware Requirements](#hardware-requirements)
- [Software Requirements](#software-requirements)
- [Circuit Diagram](#circuit-diagram)
- [Installation and Setup](#installation-and-setup)
- [Usage](#usage)
- [Code Explanation](#code-explanation)
- [License](#license)

## Overview

The project uses the Adafruit 16-channel PWM/Servo driver to control four servos. The servo positions are adjusted using defined sequences in the loop function, allowing smooth, coordinated movements.

## Features

- Control up to 16 servos using a single Adafruit PWM Servo Driver.
- Smooth transition of servo positions with customizable speed and range.
- Simple setup with I2C communication for reliable servo control.

## Hardware Requirements

- Arduino board (e.g., Uno, Mega, or compatible).
- Adafruit 16-channel PWM Servo Driver board.
- 4 x Servos.
- Jumper wires for connections.
- External power supply for servos if needed.

## Software Requirements

- [Arduino IDE](https://www.arduino.cc/en/software)
- [Adafruit PWM Servo Driver Library](https://github.com/adafruit/Adafruit-PWM-Servo-Driver-Library)

## Circuit Diagram

The Adafruit PWM Servo Driver is connected to the Arduino via I2C (SDA and SCL pins). Each servo is connected to the corresponding output channels on the driver board.

## Installation and Setup

1. Connect your hardware according to the circuit diagram.
2. Install the Adafruit PWM Servo Driver library from the Arduino Library Manager.
3. Upload the code to your Arduino board.

## Usage

1. Power up your Arduino and servo driver.
2. The servos will execute predefined movement sequences as specified in the loop function.
3. Modify the delay values and PWM settings in the code to adjust servo speed and position.

## Code Explanation

### Servo Control Setup

- The Adafruit PWM Servo Driver is initialized with a frequency of 60 Hz, suitable for most servos.
- Four servos are connected to channels 0 through 3 of the PWM driver.

### Movement Sequences

- The `setup()` function initializes the servos to specific positions.
- The `loop()` function executes a series of movements for each servo, adjusting positions smoothly by incrementing or decrementing the PWM values.
- Each servo movement is controlled within a defined range, allowing for smooth and coordinated transitions.

### Functions

- `srituhobby.setPWM(servo, 0, position)`: Sets the PWM signal for a given servo to control its position.
- The movement ranges and delays can be adjusted to change the servo's behavior.

## License

This project is open-source and available under the MIT License.
