# Issue: the WiMod Lorawan gateway stopped working

 - Old Lorawan gateway:
 -- https://lora-alliance.org/wp-content/uploads/2019/09/WiMOD_LiteGateway_QuickStartGuide_V1_1.pdf
 -- https://shop.imst.de/media/pdf/f5/68/7f/WiMOD_LiteGateway_QuickStartGuide_V1_5.pdf
 -- https://shop.imst.de/wireless-solutions/lora-products/8/ic880a-spi-lorawan-concentrator-868-mhz
 -- https://shop.imst.de/wireless-solutions/lora-products/36/lite-gateway-demonstration-platform-for-lora-technology?c=7
 -- The wimod gateway Basically uses the ic880a radio concentrator that connects to the raspberry pi via a 3rd connector board to SPI
 - Actions:
 -- Replace raspberry pi B+ with raspberry pi 3
 -- Follow https://neoaggelos.github.io/blog/005-ic880a-gateway-basicstation/#part-5-derive-gateway-eui
 -- Use SX1301_RESET_BCM_PIN=5 instead of 25 in /opt/ttn-station/bin/start.sh
 -- Use the Fix https://www.thethingsnetwork.org/forum/t/ic880a-raspi-3b-v1-2-concentrator-start-failed-lgw-start-issue/68044/6
 -- Created a call_start_fix.sh that then calls the following:
 ‘’’
 sudo RADIODEV=/dev/spidev0.0 LORAGW_SPI_SPEED=2000000 /opt/ttn-station/bin/start.sh
 ‘’’
 which sets the Pi SPI speed to 2MHz.
 -- Update the debian script at /lib/systemd/system/ttn-station.service to call "call_start_fix.sh" instead of "start.sh"

