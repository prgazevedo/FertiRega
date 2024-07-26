# FertiRega
## WisBlock RAK 4631 Starter
### Setup Lora connectivity to Gateway
- https://docs.rakwireless.com/Product-Categories/WisBlock/RAK4631/Datasheet/#overview
- Start Code from https://github.com/RAKWireless/WisBlock/blob/master/examples/RAK4630/solutions/Intelligent_Agriculture/Intelligent_Agriculture.ino
- Install UNO Lib modules (tool->manage libs->install Sx126x): https://github.com/beegee-tokyo/SX126x-Arduino/
- Boards Manager (preferences->additional boards manager URL): https://raw.githubusercontent.com/RAKwireless/RAKwireless-Arduino-BSP-Index/main/package_rakwireless_index.json

- Connect PC to device via USB AND Use the Serial Monitor to connect to device (before any code)

Should return the following:

 **  
 >DR 3
 >  Class 0
 >  Subband 1
 >  Fport 2
 >  Unconfirmed Message
 >  Region AU915
 >LoRa P2P status:
 >  P2P frequency 916000000
 >  P2P TX Power 22
 >  P2P BW 125
 >  P2P SF 7
 >  P2P CR 1
 >  P2P Preamble length 8
 >  P2P Symbol Timeout 0
 >============================**
  
 - Add EUI, App EUI, App Key: https://eu1.cloud.thethings.network/console/applications/m5-ttn-test/devices
 - Create the codes and add to device .ino code
