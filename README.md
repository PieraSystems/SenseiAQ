# SenseiAQ
SenseiAQ app for connecting with Piera Systems IPS and Canāree sensors.

## Package Downloads
**[Windows 10 Installer](https://github.com/PieraSystems/SenseiAQ/releases/download/v1.6.1/SenseiAQ-1.6.1-Setup-Win.exe)**

**[MacOS Installer (10.15+ required)](https://github.com/PieraSystems/SenseiAQ/releases/download/v1.6.1/SenseiAQ-1.6.1-macOS.zip)**

## Installation Notes
**Windows 10** - If Microsoft Defender blocks the app, select "More info" and then "Run anyway". In some environments, manual installation of the [Silicon Labs driver](#driver-installation-windows-10) is required. 

**MacOS** - Secondary-click the app icon, then choose "Open" from the shortcut menu (currently awaiting Mac App Store approval). For 10.14 (Mojave), [a driver update](https://www.silabs.com/documents/public/software/Mac_OSX_VCP_Driver.zip) needs to be installed for Canaree I-series, A-series and IPS sensors. 

## User Guide
* [SenseiAQ User Guide (PDF)](https://pierasystems.com/download-attachment/3871)
* [R-Series Config Guide (PDF)](https://pierasystems.com/download-attachment/3921)


## Driver Installation (Windows 10)

### IPS Series, Canāree A1, Canāree I1/I5

1. Download the [Universal Windows Driver](https://www.silabs.com/documents/public/software/CP210x_Universal_Windows_Driver.zip) from SiLabs.com.
1. Right-click on *CP210x_Universal_Windows_Driver.zip*, choose "Extract All..." and then "Extract".
1. In the directory Right click on the silabser.inf file and select Install
1. Follow instructions in Installation Wizard to complete installation.

### Canāree R-Series 

1. Download the [USB Windows Driver](https://www.olimex.com/Products/Breadboarding/BB-CH340T/resources/CH341SER.zip) from Olimex.com.
1. Right-click on *CH341SER.zip*, choose "Extract All..." and then "Extract".
1. Enter the *CH341SER* folder and run *CH341SER.EXE*.
1. Click Install button.


## Updates
* Mar 7, 2022 - Version 1.6.1 released ([view release notes](https://github.com/PieraSystems/SenseiAQ/releases/tag/v1.6.1)).
* Dec 17, 2021 - Version 1.5.3 released ([view release notes](https://github.com/PieraSystems/SenseiAQ/releases/tag/v1.5.3)). 
* Oct 7, 2021 - Version 1.2.3 released ([view release notes](https://github.com/PieraSystems/SenseiAQ/releases/tag/v1.2.3)).
* Jul 26, 2021 - Version 1.1.0 released ([view release notes](https://github.com/PieraSystems/SenseiAQ/releases/tag/v1.1.0)).
* Jun 6, 2021 - Version 1.0.0 released ([view release notes](https://github.com/PieraSystems/SenseiAQ/releases/tag/v1.0.0)).
* May 11, 2021 - Version 0.9.5 released ([view release notes](https://github.com/PieraSystems/SenseiAQ/releases/tag/v0.9.5)).

## Usage

Attach the sensor via USB and start SenseiAQ. Wait at least 1 minute for SenseiAQ to collect enough readings to calculate AQI.

Data can be viewed within SenseiAQ, saved to a log file, or sent to Azure's IoT Hub. Logs are stored in the SenseiAQ folder, inside the user's Documents folder.

## Troubleshooting

In some cases the device may be working but fails to communcate with SenseiAQ. If there's any other programs running that may be using communication ports, such as serial monitoring or logging software, it can prevent SenseiAQ from communicating with the device. Certain USB devices, such as IoT development boards, can also intefere with SenseiAQ's detection of the Piera/Canaree device.

Try shutting down any programs and unplugging USB devices that could potentially be interfering, then unplug the Piera/Canaree device and restart SenseiAQ. With SenseiAQ running, plug the device in again and wait up to a minute for it to start communicating.
