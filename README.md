# CONTROLLING LIGHTS USING ESP32
PROJECT OVERVIEW
This project uses an ESP32 DevKit board programmed via the Arduino IDE to control lights over Wi-Fi through the Blynk mobile app. You create a Blynk project, select “ESP32 Dev Board” and “Wi-Fi,” then receive an AuthToken to link your hardware and app. The ESP32 hosts a Blynk client that listens for widget commands, enabling remote light control from anywhere with internet access.

KEY COMPONENTS
ESP32 DevKit board
Blynk mobile app (iOS/Android)
Arduino IDE with Blynk library
Light source (LED or mains lamp via relay module)
Breadboard, resistors, jumper wires
Wi-Fi network credentials

HOW IT WORKS
Configure the Blynk project: drag a Button widget, assign it to a GPIO pin (e.g., GPIO2), and set its mode to “Switch.”
Copy the AuthToken emailed by Blynk into your Arduino sketch alongside your SSID and password.
Include the Blynk and Wi-Fi libraries (<WiFi.h>, <BlynkSimpleEsp32.h>), then call Blynk.begin(auth, ssid, pass).
Upload to the ESP32; once connected, tapping the button in the app sends commands via the Blynk server to toggle the GPIO pin, energizing or de-energizing the relay (or LED) accordingly.

BENEFITS
No custom backend required—Blynk hosts the server.
Drag-and-drop dashboard design.
Two-way communication allows OTA updates and real-time status.
Secure token-based authentication.
