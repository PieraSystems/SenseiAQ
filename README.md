# SenseiAQ
SenseiAQ App for connecting with Piera-7100 and Canāree sensors

## Package Downloads
**[Windows 10 Installer](https://github.com/PieraSystems/SenseiAQ/releases/download/0.9.0/SenseiAQ-0.9.0.Setup.exe)**

**[MacOS Installer](https://github.com/PieraSystems/SenseiAQ/releases/download/0.9.0/SenseiAQ-darwin-x64-0.9.0.zip)**

## Installation Notes
**Windows 10** - If Microsoft Defender blocks the app, select "More info" and then "Run anyway". A driver may be required also if Windows 10 fails to commincate with the device. You can download the [Windows 10 driver here](http://www.prolific.com.tw/UserFiles/files/PL23XX_Prolific_DriverInstaller_v203(2).zip). 

**MacOS** - Control-click the app icon, then choose "Open" from the shortcut menu.

## Usage

Attach the sensor via USB and start SenseiAQ. Wait at least 1 minute for SenseiAQ to collect enough readings to calculate AQI.

Data can be viewed within SenseiAQ, saved to a log file, or sent to Azure's IoT Hub. Logs are stored at "%appdata%\SenseiAQ\sensor-logs" on Windows 10 and "~/Library/Application Support/SenseiAQ/sensor-logs" on MacOS.

## Troubleshooting

In some cases the device may be working but fails to communcate with SenseiAQ. If there's any other programs running that may be using communication ports, such as serial monitoring or logging software, it can prevent SenseiAQ from communicating with the device. Certain USB devices, such as IoT development boards, can also intefere with SenseiAQ's detection of the Piera/Canaree device.

Try shutting down any programs and unplugging USB devices that could potentially be interfering, then unplug the Piera/Canaree device and restart SenseiAQ. With SenseiAQ running, plug the device in again and wait up to a minute for it to start communicating.
