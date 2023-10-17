---
title: Pixel Magic Tool ( Pixel Magic Tool)
hide:
  # - navigation
  # - toc
---

## Attention! Pixel Magic Tool is now enabled by default

The Pixel Magic Tool will convert any image or gif to 2D pixel art and send it to the WLED device. The file types PNG, JPG, WEBP and GIF have been tested to work with the tool.

## Installation Approaches

There are three ways to install the Pixel Magic Tool:

1. WLED editor mode. Upload  pxmagic.htm from  [PixelMagicTool](https://github.com/ajotanc/PixelMagicTool/)   to your WLED device while it is running 
2. Local web browser. a web page will run on the local machine connecting to the WLED device but will require fetching an extra file. Supported from WLED release [v0.14.0-b1](https://github.com/Aircoookie/WLED/blob/main/CHANGELOG.md#wled-release-0140-b1) or later
3. Include the Pixel Magic Tool in the binary and compile it from the source code. Allows access to the Pixel Magic Tool on any device that has a connection to the WLED device. Supported from WLED release [v0.14.0-b2](https://github.com/Aircoookie/WLED/blob/main/CHANGELOG.md#build-2301240) (PR [#3042](https://github.com/Aircoookie/WLED/pull/3042))

### Approach 1: WLED Editor Mode

1. Download the `pxmagic.htm` file from the [PixelMagicTool](https://github.com/ajotanc/PixelMagicTool/)  repository
2. Go to the URL `http://[device_ip_address]/edit`
3. Upload the `pxmagic.htm` file using the UI
4. Go to `http://[device_ip_address]/pxmagic.htm`
5. Now head to the [Setup 2D Matrix](#setup-2d-matrix) point

### Approach 2: Local Browser

1. Download the `pxmagic.htm` from the [PixelMagicTool](https://github.com/ajotanc/PixelMagicTool/) repository
2. Open `pxmagic.htm` in a browser
3. Head over to the [Setup 2D Matrix](#setup-2d-matrix) point

### Approach 3: Warning! Include Pixel Magic Converter In Build Files (Compilation required)
Compiling WLED from the source code is required. Follow the instructions on [compiling WLED](../../advanced/compiling-wled) to do this.

1. Follow the instructions under [Making a custom environment](../../advanced/compiling-wled/#making-a-custom-environment) and set the flag `-D WLED_DISABLE_PXMAGIC` under the line that starts with `build_flags =` in `platformio_override.ini`
2. Compile and flash the binary to the ESP board
3. Power on board and connect via WiFi using the [default login](../../basics/getting-started/)
4. It is now time to [Setup the 2D Matrix](#setup-2d-matrix)

### Approach 4: Enable Pixel Magic Tool in Settings
1. Go to `Config` > `User Interface` and `Enable Pixel Magic Tool`
2. It is now time to [Setup the 2D Matrix](#setup-2d-matrix)

## Setup 2D Matrix
2D LED panels are natively supported by WLED but need some configuration for the software to show the 2D grid correctly.

1. Head into the `2D Configuration` settings menu in WLED
2. Set the option "Strip or panel" to `2D Matrix`
3. Setup rest of the LED panel layout according to the specifics of your LED panel

### Serpentine option
Setting the serpentine LED panel option incorrectly can lead to very confusing results that look almost correct but not quite. Enabling or Disabling the option depends on the characteristics of the 2D matrix

## Usage
### Approach 1, 2, 3:
The Pixel Magic Generator  have a link in the WLED front-end, therefore head over to the web page: `http://[device_ip_address]/pxmagic.htm` (default DHCP IP-address [link](http://4.3.2.1/pxmagic.htm)).

### Aproach 4:
[Pixel Magic Tool](../assets/images/content/pxm_1.png)

On the web page:
Follow the instruction listed on this site https://user-images.githubusercontent.com/47322034/242754481-20ad60d1-3b01-42b6-9937-4dda3862a3a4.mp4
