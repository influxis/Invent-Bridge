Bridge Setup
(Video Tutorial Coming Soon)

Requirements:

Arduino Uno Board

Arduino UI (http://www.arduino.cc/ - See Download Section)

USB Cable from Arduino to Computer

iotbridge-mac-v0.1.zip ( Available to download within the "release" tab )

Instructions:

Log into your Influxis account, navigate to the IOT section, and create a project; you must create a password for your project and write it down, YOU WILL NEED IT.  Click the Manage arrow icon on the project to go into the admin panel.  If a device item has not already been created for you, within that project create a new device which represents your Arduino.

The rest of the setup assumes you know a bit about the Arduino Environment. To learn about the Arduino Environment refer to the Learning section of the Arduino Website (http://arduino.cc/en/Guide/Environment)

If you haven't done so, Connect the USB wire to your computer and run the arduino UI software.  Run the Arduino Software interface, navigate to the Tools menu, find the item Board and select Arduino Uno. Navigate to Tools and Serial Port and select the usb port that your arduino is connected to, usually it starts with a dev/tty.usbmodem or dev/cu.usbmodem either one should work.  This path will be needed to configure the bridge so be sure to note it down somewhere.

arduinoPort

Now find the InfluxisIoTUnoR3.ino file that came with the iotbridge.zip download within a folder labeled “arduino” and upload it to your board using the Arduino ui Interface.inoScript

Download the iotbridge.zip file from Influxis and unpackage the zip file, then navigate to the iotBridge folder.

Navigate into a folder called “data” within the iotBridge folder root and open the config.json file in a text editor like Sublime Text 2.

Enter the details of your account and project in the config files respective tags.

- your_user_name = Invent Platform username

- your_project_name = Name of the project created on the IoT page

- your_device_password = The password you set for the project

- your_device_name = The device name by default is “arduino”

- port = The serial USB port the Arduino is connected to

Open Terminal and navigate to the iotBridge directory.

Run the file named iotbridge by typing:  ./iotbridge --debug (if you dont want to see the connection logs just leave out --debug from the command)

Now you are ready to build a project.

If it does not work:

Check your config file make sure that you added the data correctly. Copy and paste to ensure the spelling has no mistakes.
Check your password and server path.
