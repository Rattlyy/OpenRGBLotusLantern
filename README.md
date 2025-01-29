# LotusLantern LED Strips in OpenRGB

Very small Node.js app that adds support for LotusLantern LED strips to OpenRGB.

## Installation

1. Clone this repository
2. Run `npm install`
3. Run `npm start`

## Usage

1. Open OpenRGB
2. Go to Settings -> Serial Devices
3. Add a new device with the following settings:
   - Port: `udp:127.0.0.1` (very counterintuitive, I know)
   - Baud: `1920` (also very counterintuitive)
   - Protocol: `Keyboard Visualizer`
4. Scan for devices 

Once the device is added, you can control the LED strip from OpenRGB.

## Notes

The script works by simply parsing the UDP packets sent by OpenRGB and forwarding them to the LED strip.
Credits to [homebridge-ledstrip-bledom](https://github.com/bjclopes/homebridge-ledstrip-bledom) for implementing the BLE part and all the hard work.
