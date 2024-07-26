# FertiRega
## WisBlock RAK 4631 Starter
### Setup Lora connectivity to Gateway
- https://docs.rakwireless.com/Product-Categories/WisBlock/RAK4631/Datasheet/#overview
- Start Code from https://github.com/RAKWireless/WisBlock/blob/master/examples/RAK4630/solutions/Intelligent_Agriculture/Intelligent_Agriculture.ino
- Install UNO Lib modules (tool->manage libs->install Sx126x): https://github.com/beegee-tokyo/SX126x-Arduino/
- Boards Manager (preferences->additional boards manager URL): https://raw.githubusercontent.com/RAKwireless/RAKwireless-Arduino-BSP-Index/main/package_rakwireless_index.json

- Connect PC to device via USB AND Use the Serial Monitor to connect to device (before any code)

Should return the following:
```
============================
LPWAN WisBlock Node
Built with RAK's WisBlock
SW Version 2.0.0
LoRa(R) is a registered trademark or service mark of Semtech Corporation or its affiliates.
LoRaWAN(R) is a licensed mark.
============================
Device status:
   RAK4631
   Auto join disabled
   Mode LPWAN
   Network not joined
   Send Frequency 0
LPWAN status:
   Dev EUI 000D75E6564DC1F3
   App EUI 70B3D57ED00201E1
   App Key 2B84E0B09B68E5CB42176FE753DCEE79
   Dev Addr 26021FB4
   NWS Key 323D155A000DF335307A16DA0C9DF53F
   Apps Key 3F6A66459D5EDCA63CBC4619CD61A11E
   OTAA enabled
   ADR disabled
   Public Network
   Dutycycle disabled
   Join trials 5
   TX Power 0
   DR 3
   Class 0
   Subband 1
   Fport 2
   Unconfirmed Message
   Region AU915
LoRa P2P status:
   P2P frequency 916000000
   P2P TX Power 22
   P2P BW 125
   P2P SF 7
   P2P CR 1
   P2P Preamble length 8
   P2P Symbol Timeout 0
============================
  ```
 - Add EUI, App EUI, App Key: https://eu1.cloud.thethings.network/console/applications/m5-ttn-test/devices
 - Create the codes and add to device .ino code
 - Download the correct board support for nrf chip: https://github.com/adafruit/Adafruit_nRF52_Arduino/files/15325649/adafruit-nrfutil.zip
 - unzip and replace the IDE default board support:
  ```
mv ~/Library/Arduino15/packages/rakwireless/hardware/nrf52/1.3.3/tools/adafruit-nrfutil/macos/adafruit-nrfutil ~/Library/Arduino15/packages/rakwireless/hardware/nrf52/1.3.3/tools/adafruit-nrfutil/macos/adafruit-nrfutil.bak
cp ~/Downloads/adafruit-nrfutil/macos/adafruit-nrfutil ~/Library/Arduino15/packages/rakwireless/hardware/nrf52/1.3.3/tools/adafruit-nrfutil/macos/
  ```
 - compile
   
