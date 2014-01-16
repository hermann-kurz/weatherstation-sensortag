weatherstation-sensortag
========================

Use the TI Sensor Tag as weather station on a Raspberry Pi. Data is stored in Tempo-DB.

Requirements:

- Bluetooth Low Energy (BLE) USB dongle. I am using the Plugable USB-BT4LE
- Raspberry Pi (or other linux computer)
- TI Sensor Tag: http://www.ti.com/ww/en/wireless_connectivity/sensortag/index.shtml
- BLE driver: http://mike.saunby.net/2013/04/raspberry-pi-and-ti-cc2541-sensortag.html
- bluepy library from Ian Harvey https://github.com/IanHarvey/bluepy
- Tempo-DB account (https://tempo-db.com/)

Steps to get this going:
- install BLE driver and bluepy library
- Put your Tempo-DB credentials into sensortag-tempodb.py.
- Put your Tag-UUID into btle.py
- do a "sudo hcitool lescan" and press the button on the sensor tag. You should see the Sensor Tags UUID
- start the script with "sudo nohup  python sensortag-tempodb.py &"
- Look at the output ("nohup.out") for errors.
- go to https://tempo-db.com and enjoy your data
