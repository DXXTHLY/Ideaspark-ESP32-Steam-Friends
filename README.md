# Ideaspark-ESP32-Steam-Friends

# Steam Friends List Display

##  NEW PROJECT UPDATE (V2.0)

I have just released a major update to both the **Generator Tool** and the **Source Code**! Here is what's new:

### 🛠️ Generator Tool Update (Easy Setup)
If you aren't a coder or don't want to manually edit the script, use the **Generator Update**. 
*   **What it does:** It provides a simple window where you can type in your WiFi and Steam info and select any image. It automatically resizes your image and builds the entire code file for you. No setup or manual editing required!
*   👉 [**Download Generator Update here**](https://github.com/DXXTHLY/Ideaspark-ESP32-Steam-Friends/releases/tag/ideaspark-esp32-wroom-no-setup)

---

###  Full Program & Source File Update
For those who want to see the code or edit it manually, the main project file has been completely overhauled.
*   **New Features:**
    *   **New Boot Sequence:** Added an Intro and a Privacy Notice screen.
    *   **"Establishing Uplink" Screen:** A new, cooler WiFi connection screen with a functional progress bar.
    *   **Improved Status:** Friends set to "Away" now specifically show as **Away** in yellow (instead of just Online).
    *   **Code Optimization:** Smoother scrolling for long names and game titles.
*   👉 [**Download Full Program/File Update here**](https://github.com/DXXTHLY/Ideaspark-ESP32-Steam-Friends/releases/tag/ideaspark-esp32-wroom-steam-friends-tracker)

---

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

## Required Libraries

Install via Arduino Library Manager (Sketch -> Include Library -> Manage Libraries...):
- `WiFi` - For handling Wi-Fi connectivity on ESP32 devices.
- `HTTPClient` - For making HTTP requests to the Steam API.
- `ArduinoJson` - For parsing JSON responses from the Steam API. (Install version 6.x or later)
- `TFT_eSPI` - For handling graphics and displaying content on TFT displays.
Note: You will need to configure this library for your specific TFT screen. Follow the documentation provided on the library’s GitHub page.

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

## Board
https://www.amazon.com/dp/B0D6QXC813?ref=ppx_yo2ov_dt_b_fed_asin_title&th=1

## Background Image
- If you would like the change the background, here are the settings I used as well as the website: https://notisrac.github.io/FileToCArray/
- If you want to make it even easier on yourself before uploading the image into `FileToCArray` rename the picture to `Screenshot 2025-03-10 135855.png`.
- Simply copy to clipboard, find the exact code in `.ino` file and replace it.

![ss](https://github.com/user-attachments/assets/ab899da0-03d5-4966-9e68-2d128b7ff793)


Still a work in progress..
