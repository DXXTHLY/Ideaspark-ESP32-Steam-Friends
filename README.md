# Ideaspark-ESP32-Steam-Friends

# Steam Friends List Display

## Overview
This project is an ESP32-based application that connects to the Steam Web API to retrieve and display a user's Steam friends list and their online status. The information is displayed on a TFT screen connected to the ESP32.

## Features
- Connects to Wi-Fi for API requests.
- Retrieves a Steam user's friends list and their online status.
- Displays friends on a TFT screen with pagination.
- Shows an image as a background on the screen.

## Hardware Requirements
- **ESP32 Board** (e.g., NodeMCU-32S, Wemos D1 Mini ESP32)
- **TFT Display** (Compatible with TFT_eSPI library)

## Software Requirements
- **Arduino IDE** or PlatformIO
- **TFT_eSPI Library** (Install via Arduino Library Manager)
- **ArduinoJson Library** (Install via Arduino Library Manager)

## Setup
1. **Install required libraries:**
   - Open Arduino IDE, go to `Sketch > Include Library > Manage Libraries`.
   - Search for and install `TFT_eSPI` and `ArduinoJson`.

2. **Configure TFT_eSPI:**
   - Edit the `User_Setup.h` file inside the TFT_eSPI library to match your specific display.

3. **Connect TFT Display to ESP32:**
   - Follow wiring instructions for your specific display model.

## Usage
1. Replace the following placeholder values in your code:
   ```cpp
   #define SSID "Your_SSID"
   #define PASSWORD "Your_Password"
   #define API_KEY "Your_Steam_API_Key"
   #define STEAM_ID "Your_Steam_ID"
   ```

2. Upload the code to your ESP32 board.

3. Open the Serial Monitor to view connection status and debugging information.

## Display Controls
- **EN Button (GPIO 0):** Used for paginating through the friends list.

## License
This project is licensed under the MIT License. See the LICENSE file for more details.

## Acknowledgments
- Thanks to the developers of `TFT_eSPI` and `ArduinoJson` libraries for making this project possible.

