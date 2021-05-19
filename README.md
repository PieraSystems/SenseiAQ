# SenseiAQ
SenseiAQ App for connecting with Piera-7100 and Canāree sensors

## Package Downloads
**[Windows 10 Installer](https://github.com/PieraSystems/SenseiAQ/releases/download/v0.9.5/SenseiAQ-095-Win10.exe)**

**[MacOS Installer (10.15+ required)](https://github.com/PieraSystems/SenseiAQ/releases/download/v0.9.5/SenseiAQ-095-macOS-x64.zip)**

## Installation Notes
**Windows 10** - If Microsoft Defender blocks the app, select "More info" and then "Run anyway". In some environments, manual installation of the [Silicon Labs driver](https://www.silabs.com/documents/public/software/CP210x_Universal_Windows_Driver.zip) is required. 

**MacOS** - Secondary-click the app icon, then choose "Open" from the shortcut menu (currently awaiting Mac App Store approval).

## Updates
May 11, 2021 - Version 0.9.5 released ([view release notes](https://github.com/PieraSystems/SenseiAQ/releases/tag/v0.9.5)).

## Usage

Attach the sensor via USB and start SenseiAQ. Wait at least 1 minute for SenseiAQ to collect enough readings to calculate AQI.

Data can be viewed within SenseiAQ, saved to a log file, or sent to Azure's IoT Hub. Logs are stored in the SenseiAQ folder, inside the user's Documents folder.

## Troubleshooting

In some cases the device may be working but fails to communcate with SenseiAQ. If there's any other programs running that may be using communication ports, such as serial monitoring or logging software, it can prevent SenseiAQ from communicating with the device. Certain USB devices, such as IoT development boards, can also intefere with SenseiAQ's detection of the Piera/Canaree device.

Try shutting down any programs and unplugging USB devices that could potentially be interfering, then unplug the Piera/Canaree device and restart SenseiAQ. With SenseiAQ running, plug the device in again and wait up to a minute for it to start communicating.

## Driver Installation (Windows 10)

1. Download the [Universal Windows Driver](https://www.silabs.com/documents/public/software/CP210x_Universal_Windows_Driver.zip) from SiLabs.com.
1. Right-click on *CP210x_Universal_Windows_Driver.zip*, choose "Extract All..." and then "Extract".
1. Enter the *CP210x_Universal_Windows_Driver* folder and run *CP210xVCPInstaller_x64.exe*.
1. Follow instruction in Installation Wizard.
