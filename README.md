# **💻 ESP32 Flight Controller PWM Monitor**

|

| Project Type | Tool | Board | ESP32 | Wireless | WiFi Hotspot |  
| Purpose | PWM Signal Monitoring | Platform | Standalone | Interface | Web Browser |

## **This project provides a simple, wireless tool for monitoring PWM signals from a flight controller using an ESP32. The ESP32 creates its own WiFi Access Point (hotspot) and hosts a web page that displays the real-time PWM values. This allows you to easily check the output from your flight controller's ESC channels using a phone, tablet, or computer.**

## **✨ Key Features**

* **Wireless Monitoring:** Access the live PWM data from any device with a web browser.  
* **Real-time Updates:** Values are updated every 0.5 seconds, providing a responsive view of your signals.  
* **Simple Setup:** Requires minimal code and only one additional library.  
* **Clear Web Interface:** A clean, easy-to-read web page with individual cards for each PWM channel.

## **🛠️ Hardware Required**

| Component | Notes |  
| ESP32 Board | Any ESP32 development board with an integrated WiFi module. |  
| Jumper Wires | For connecting the ESP32 to the flight controller. |

## **⬇️ Installation and Setup**

### **Prerequisites**

1. **Install Arduino IDE.**  
2. Install the **ESP32 board package** in the Arduino IDE.  
3. Install the **ArduinoJson** library via the Arduino Library Manager.

### **Wiring**

Connect the ground pin of the ESP32 to the ground pin of your flight controller. Then, connect the PWM output pins from your flight controller to the desired input pins on the ESP32.

### **Code Configuration**

1. Open the project code in the Arduino IDE.  
2. **Configure PWM Pins:** In the code, specify which ESP32 pins you are using to read the PWM signals.  
3. **Set WiFi Credentials:** You can optionally configure a password for your ESP32's WiFi hotspot.

### **Uploading the Code**

1. Select the correct board and COM port in the Arduino IDE.  
2. Upload the code to your ESP32.

## **⚙️ Usage**

1. **Power On:** Power up both your flight controller and the ESP32.  
2. **Connect to WiFi:** On your computer or phone, connect to the WiFi network created by the ESP32.  
3. **Open the Web Interface:** Open a web browser and navigate to the IP address (http://192.168.4.1) displayed in the Arduino Serial Monitor.  
4. You will now see the live PWM values from your flight controller displayed on the web page. This is useful for troubleshooting throttle calibration, signal jitter, or other ESC-related issues.
