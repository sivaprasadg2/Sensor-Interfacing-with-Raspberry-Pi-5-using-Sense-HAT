# Sensor-Interfacing-with-Raspberry-Pi-5-using-Sense-HAT
 ## 1 Introduction:
This lab introduces students to embedded sensor interfacing using the Raspberry Pi 5
with the Sense HAT. The objective is to demonstrate reading sensor data (temperature,
humidity, and pressure) and displaying a message using the LED matrix. This provides
hands-on experience in Python-based embedded development relevant to IoT and smart
systems.
(display 1.JPEG)
*Figure 1: Executing the code and sensor data being displayed in terminal*
## 2 Methodology
The Raspberry Pi was configured in headless mode to allow SSH access. The Sense HAT
library was installed using apt. Two Python scripts were written: one for displaying
messages on the LED matrix, and one for reading and printing sensor values.

2.1 Software and Hardware Used
• Programming language: Python 3

• Libraries: sense-hat, time

• Hardware: Raspberry Pi 5, Sense HAT (attached via GPIO)
### 2.1 Software and Hardware Used
• Programming language: Python 3

• Libraries: sense-hat, time

• Hardware: Raspberry Pi 5, Sense HAT (attached via GPIO)

### 2.2 Algorithm Setup
Initial Setup for Raspberry Pi 5 and Sense HAT
1. Download and flash Raspberry Pi OS to the SD card using Raspberry Pi Imager.
2. Enable SSH and set hostname, username, and Wi-Fi credentials in the Imager set-
tings.
3. Insert the SD card into Raspberry Pi and power it on.
1
4. Use terminal to connect to the Pi via SSH (e.g., ssh pi@192.168.0.10).
5. Run the following commands to update the system and install Sense HAT library:
sudo apt update
sudo apt install sense - hat
Part 1: LED Matrix Message Display
1. Import the required libraries: sense_hat and time.
2. Create a SenseHat object to communicate with the Sense HAT hardware.
3. Call the show_message() function to scroll a text message on the LED matrix.
4. Customize the message appearance using optional parameters like text_colour and
scroll_speed.
Part 2: Environmental Sensor Data Reading
1. Import the necessary Python libraries: sense_hat and time.
2. Initialize the SenseHat object to access sensor data.
3. Start an infinite loop using while True.
4. Read sensor data using:
• get_temperature() for ambient temperature.
• get_humidity() for relative humidity.
• get_pressure() for barometric pressure.
5. Format the data output using Python string formatting.
6. Display the data in the terminal using the print() function.
7. Delay the next reading using time.sleep(2) to avoid flooding the output.
## 3 Result
Real-time environmental data was measured printed in the terminal at 2-second intervals.
The LED matrix displayed the message as expected.
