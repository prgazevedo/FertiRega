# FertiRega
## WisBlock RAK 4631 Starter
### Setup Lora connectivity to Gateway
- https://docs.rakwireless.com/Product-Categories/WisBlock/RAK4631/Datasheet/#overview
- Start Code from https://github.com/RAKWireless/WisBlock/blob/master/examples/RAK4630/solutions/Intelligent_Agriculture/Intelligent_Agriculture.ino
- Install UNO Lib modules (tool->manage libs->install Sx126x): https://github.com/beegee-tokyo/SX126x-Arduino/
- Boards Manager (tool->add board): https://raw.githubusercontent.com/RAKwireless/RAKwireless-Arduino-BSP-Index/main/package_rakwireless_index.json
- Add EUI, App EUI, App Key: https://eu1.cloud.thethings.network/console/applications/m5-ttn-test/devices
-- Create the codes and add to device .ino code
