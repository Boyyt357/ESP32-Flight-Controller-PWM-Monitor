ESP32 Flight Controller PWM Monitor
This project uses an ESP32 to act as a Wi-Fi Access Point and read PWM signals from a flight controller. It hosts a simple web page that displays these signal values in real-time, allowing you to monitor your flight controller's output wirelessly with a phone or computer.

Features
Wireless Monitoring: The ESP32 creates its own Wi-Fi network, so you don't need a USB cable to view the data.

Real-time Updates: The web interface automatically fetches and updates the PWM values every half-second.

Simple Setup: With just a few lines of code and a single library, you can get this project up and running.

Clear Web Interface: The web page is designed to be easy to read, with individual cards for each PWM channel.

Installation
1. Prerequisites
An ESP32 development board.

Jumper wires for connecting your flight controller's PWM outputs to the ESP32.

The Arduino IDE with the ESP32 board package installed.

The ArduinoJson library.

2. Wiring
Connect the PWM output pins from your flight controller to the corresponding GPIO pins on the ESP32. It is critical to also connect the Ground (GND) pins of both the flight controller and the ESP32.

The pins used in this code are: GPIO25, GPIO26, GPIO27, and GPIO14.

⚠️ Warning: The ESP32 operates on 3.3V logic. Do not connect any signal pins that operate at a higher voltage (e.g., 5V) directly to the ESP32, as this can permanently damage the board.

3. Software Setup
Install the ArduinoJson Library:

In the Arduino IDE, navigate to Sketch > Include Library > Manage Libraries....

Search for "ArduinoJson".

Click on the library by Benoit Blanchon and install the latest version.

Configure the Code:

Open the .ino file in your Arduino IDE.

WiFi Credentials: You can change the ssid and password for your Wi-Fi network. While the code uses 123password as a default, it's highly recommended to use a strong, unique password.

PWM Pins: If you are using different pins, update the PWM_PINS array to match your wiring.

Upload the Code:

Select your ESP32 board from the Tools menu.

Choose the correct COM port.

Click the Upload button in the Arduino IDE.

Usage
1.Power On: Ensure both your ESP32 and flight controller are powered on.

2.Connect to Wi-Fi: On your phone, laptop, or any Wi-Fi-enabled device, connect to the network named "ESP32-PWM-Monitor" using the password 123password (or your custom password).

3.Open the Web Page: Open a web browser and go to the address http://192.168.4.1.

4.Monitor: You will see the PWM values displayed and updating in real-time.
