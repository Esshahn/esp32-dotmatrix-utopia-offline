# Framed Utopia - Offline version

A tiny window into a better world – one whimsical utopia at a time.

## About

Framed Utopia is an art prototype that displays bright glimpses of impossible happiness on a 64x64 LED matrix display. In a world often dominated by negative news, this digital picture frame offers a moment of respite through playful, uplifting messages about imaginary utopias.

Examples of messages you might see:
- "Ewiger Sommer niemals zu heiss"
- "Laechelnde Baeume sprechende Blumen"
- "Pizza ist gesund"
- "Weltfrieden garantiert"

The display shows messages in random colors, creating a constantly changing kaleidoscope of positive possibilities.

## Hardware

- 64x64 RGB LED Matrix Display (HUB75 interface)
- ESP32 microcontroller
- Power supply (5V)
- Boot button (GPIO0) for time setup

## Features

- Displays messages in random colors for visual variety
- Changes message every 30 seconds
- Completely offline operation
- Built-in collection of whimsical utopian messages
- Low memory footprint
- Simple and reliable operation
- Power-saving sleep mode (22:00-07:00)

## Technical Details

### Dependencies

- ESP32-HUB75-MatrixPanel-I2S-DMA

### Display Configuration

- Resolution: 64x64 pixels
- Interface: HUB75
- Driver: FM6124
- Brightness: 100/255 (configurable)
- Update Interval: 30 seconds

## Setup Instructions

1. Install the required libraries in your Arduino IDE:
   - ESP32-HUB75-MatrixPanel-I2S-DMA
2. Connect the ESP32 to your LED matrix following HUB75 pinout
3. Upload the code to your ESP32
4. On first boot, use the boot button to set the time:
   - Short press: Increment hour (0-23)
   - Long press (2 seconds): Confirm time
5. The device will now run automatically, sleeping between 22:00 and 07:00

## Customization

To add or modify messages, edit the `utopias` array in the main `.ino` file. Each message should be a string that fits comfortably on the display. The system automatically handles word wrapping and display formatting.

## Background

In a world where news feeds and social media often amplify negative events, Framed Utopia aims to create tiny moments of joy through absurd and delightful possibilities. It's not about ignoring reality – it's about remembering that imagination and whimsy have their place in making our day a little brighter.

## License

This project is open source and available under the MIT License.