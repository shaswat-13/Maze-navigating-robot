This repository consists the code for a maze navigating robot named "penelope"
It has been coded in arduino ide as a final project to the fellowship we attended on hardwares and microcontrollers.
Our team (pratik, raman, sitish and me) constructed a maze navigating robot using 3 IR sensors, a L293D motor driver and an arduino uno
which also managed to get second position in the competition with a time of 34 seconds.

# Maze Navigating Robot

This Arduino-based maze-navigating robot autonomously moves through a maze by detecting obstacles with infrared (IR) sensors. The robot adjusts its direction based on the feedback from three IR sensors placed at the front, left, and right sides. It uses an L239D motor driver for motor control, enabling it to move forward, turn left or right, and stop when obstacles are detected.

## Hardware Components
- Arduino (compatible with Uno or similar boards)
- L239D Motor Driver
- IR Sensors (x3)
- DC Motors (x2 for left and right wheels)
- Chassis for mounting components
- Jumper wires and other necessary hardware

## Pin Configuration
| Component      | Arduino Pin | Description           |
|----------------|-------------|-----------------------|
| Forward IR     | 8           | Detects front obstacles |
| Left IR        | 12          | Detects left obstacles |
| Right IR       | 13          | Detects right obstacles |
| Right Motor 1  | 2           | Motor control pin     |
| Right Motor 2  | 3           | Motor control pin     |
| Left Motor 1   | 4           | Motor control pin     |
| Left Motor 2   | 5           | Motor control pin     |
| Motor Enabler A| 10 (PWM)    | Controls right motor speed |
| Motor Enabler B| 9 (PWM)     | Controls left motor speed |

## Software Overview
The code reads the IR sensor values to detect obstacles, then directs the robot as follows:
- **Move Forward**: If no obstacle is detected in front.
- **Turn Left**: If there’s an obstacle in front but none on the left.
- **Turn Right**: If there’s an obstacle in front but none on the right.
- **Stop**: If obstacles are detected in all directions.

## Motor Control Functions
The code includes motor control functions:
- `forward()`: Moves the robot forward.
- `left()`: Turns the robot left.
- `right()`: Turns the robot right.
- `halt()`: Stops the robot.

## Installation
1. Install the Arduino IDE if you haven't already.
2. Connect the Arduino board to your computer.
3. Upload the code from this repository to the Arduino board.

## Usage
- Power on the robot, and it will start navigating autonomously based on the sensor readings.
- Use the serial monitor (set to 9600 baud rate) to debug or track the sensor readings and motor actions.

## Code
The main components of the code include:
1. **IR Sensor Reading**: Reads values from the IR sensors to detect obstacles.
2. **Motor Control**: Controls motor actions to adjust movement based on the IR sensor input.
3. **Looping Logic**: Continuously checks for obstacles and adjusts the movement accordingly.

---

Enjoy navigating mazes with your autonomous robot!
