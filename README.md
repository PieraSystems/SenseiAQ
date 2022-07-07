# SenseiAQ 2.0.1
***Real-Time Air Quality Monitoring App for Piera Sensors & Canāree Air Quality Monitors***

*Release Notes - Version 2.0.1 Updated 6/23/2022*

## Package Downloads
**[Windows 10 Installer](https://github.com/PieraSystems/SenseiAQ/releases/download/v2.0.1/SenseiAQ-2.0.1-win10-x64.msi)**

**[MacOS Installer (10.14+ required)](https://github.com/PieraSystems/SenseiAQ/releases/download/v2.0.1/SenseiAQ-2.0.1-macOS-x64.zip)**

SenseiAQ software for Piera Systems enables real time Air Quality Monitoring using data from Piera’s family of Intelligent Particle Sensors (IPS) and Canāree Air Quality Monitors. It collects particle count / mass concentration data via a USB connected Piera sensor, and stores data locally on the connected device for logging and analysis. It is available as a download at no charge and supports the IPS Evaluation Kit and all Canāree series AQM’s. 

In addition to data analysis, it displays an Air Quality Index (AQI) and events (Vape and Smoke Detection) on a dashboard, the status of the sensor and its connectivity. The SenseiAQ App can also Cloud-Enable a locally connected device providing a IoT Gateway functionality enabling the collected data to be stored, viewed and analyzed remotely through Piera’s Cloud Subscription on the Sensei Website (https://sensei.pierasystems.com) - allowing multiple devices to be monitored remotely. 

SenseiAQ Software displays real-time data on a dashboard including Particle Counts for PM10, 2.5 and 1.0 sizes which are displayed in ug/m3 (micrograms per cubic meter) The Air-Quality-Index (AQI) Score is updated every minute based on previous minutes averages of particle counts. These standards were developed to monitor outdoor Air Quality and serve as a baseline for measuring Indoor Air Quality (IAQ) 

Canaree I-5 Devices support additional environmental monitors including: Temperature, Relative Humidity, Atmospheric Pressure and Volatile Organic Compounds (VOC) for which an equivalent AQI Score is generated. The VOC AQI score is based on Bosch’s definition of IAQ and ranges from 0-500 with lower numbers indicating less TVOCs in the environment. Trends of VOCs and CO2 estimates are displayed as Increasing, Decreasing or Stable for the selected timeframe. Increasing levels overtime can indicate the need to ventilate the environment. 

This software is provided with all Piera sensors while the Cloud-reporting functionality is included free for 90 days after which a customer must purchase yearly subscription to continue to use Piera’s Air Quality Monitoring Service (AQMS)

## Installation Notes
**Windows 10** - If Microsoft Defender blocks the app, select "More info" and then "Run anyway". In some environments, manual installation of the [Silicon Labs driver](#driver-installation-windows-10) is required. 

**MacOS** - Secondary-click the app icon, then choose "Open" from the shortcut menu (currently awaiting Mac App Store approval). For 10.14 (Mojave), [a driver update](https://www.silabs.com/documents/public/software/Mac_OSX_VCP_Driver.zip) needs to be installed for Canaree I-series, A-series and IPS sensors. 

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

## Operating Systems Supported :
* Windows 10 / Windows 7 (x64 Platforms) 
* MacOS 10.14+  (x64 and ARM/M1 platforms) 

## Piera devices Supported in this release :
* Original IPS-S Series running Firmware Version 1.8 (Serial# ending in V18) 
* IPS-7100 Series running Firmware Version 1.9.12 or newer
* IPS-5100 Series running Firmware Version 1.9.12 or newer
* IPS-3100 Series running Firmware Version 1.9.12 or newer
* Canaree A-Series running Version 1.9.12 or newer firmware
* Canaree I-Series running Version 1.9.12 or newer firmware


## Updates
* Jun 7, 2022 - Version 2.0.1 released ([view release notes](https://github.com/PieraSystems/SenseiAQ/releases/tag/v2.0.1)).
* Mar 7, 2022 - Version 1.6.1 released ([view release notes](https://github.com/PieraSystems/SenseiAQ/releases/tag/v1.6.1)).
* Dec 17, 2021 - Version 1.5.3 released ([view release notes](https://github.com/PieraSystems/SenseiAQ/releases/tag/v1.5.3)). 
* Oct 7, 2021 - Version 1.2.3 released ([view release notes](https://github.com/PieraSystems/SenseiAQ/releases/tag/v1.2.3)).
* Jul 26, 2021 - Version 1.1.0 released ([view release notes](https://github.com/PieraSystems/SenseiAQ/releases/tag/v1.1.0)).
* Jun 6, 2021 - Version 1.0.0 released ([view release notes](https://github.com/PieraSystems/SenseiAQ/releases/tag/v1.0.0)).
* May 11, 2021 - Version 0.9.5 released ([view release notes](https://github.com/PieraSystems/SenseiAQ/releases/tag/v0.9.5)).

## Usage

SenseiAQ App supports a single Piera device connected via USB. Devices can be swapped without restarting the SenseiAQ App. Connecting multiple Piera devices simultaneously is not supported. For that use-case we offer Python scripts to log data from multiple sensors.

Local Logging of USB-connected devices is supported via CSV Log File.  Future releases of SenseiAQ will store local device historical logs and allow viewing in custom time-frames 

Cloud Logging of devices registered to your account is supported with updates every 60-seconds for all products under a current AQMS Contract with Piera. 

The full user-guide for SenseiAQ 2.0.1 is available from our support site:
https://pierasystems.com/download-attachment/4210

## Troubleshooting

In some cases the device may be working but fails to communcate with SenseiAQ. If there's any other programs running that may be using communication ports, such as serial monitoring or logging software, it can prevent SenseiAQ from communicating with the device. Certain USB devices, such as IoT development boards, can also intefere with SenseiAQ's detection of the Piera/Canaree device.

Try shutting down any programs and unplugging USB devices that could potentially be interfering, then unplug the Piera/Canaree device and restart SenseiAQ. With SenseiAQ running, plug the device in again and wait up to a minute for it to start communicating.

If you're using an IPS sensor with SenseiAQ and data isn't showing up in the cloud, please check your firewall settings. SenseiAQ uses port 8883 (MQTT) to send data to Azure IoT Hub, and may need to be whitelisted in some cases.

Known Issues:
* **62222-2** SenseiAQ App only supports a single Piera sensor connected via USB on each PC. Multiple Piera devices are not currently supported in SenseiAQ App. 
* **62222-5** If running other USB Devices using the same CP2102 chipset, SenseiAQ may fail to detect your device. Try removing other USB devices that may be conflicting and restarting the SenseiAQ App with only your Piera device connected to USB.
* **62222-6** Device Registration popup may take up to 60 seconds to complete and disappear and requires Internet access from the PC to successfully register 
* **62222-3** When updating Wifi settings the message “Unable to Connect to Wifi” is briefly displayed prior to “device rebooting” message. If the device successfully connects to Wifi after rebooting this message will no longer be displayed after the device reboots. 
* **62222-4** Canaree R-Series is not supported in this release, a subsequent maintenance release will include support for R1/R5 running the latest firmware. R-Series users can continue to use SenseiAQ 1.6.1 
* **62222-7** If Firmware Updates fail on Canaree I-Series, the device may take up to 2 minutes to reappear on the SenseiAQ App. Wifi must be configured and operating on your Canaree I-Series device to successfully update firmware. 


**Copyright© 2022, by PIERA SYSTEMS.**

**SenseiAQ® is a product trademark of PIERA SYSTEMS. All rights reserved.**

*Piera Systems Inc. reserves the right to make corrections, modifications, enhancements, improvements and other changes to its products and services at any time and to discontinue any product or service without notice. Please contact Piera Systems anytime to obtain the latest relevant information.*
