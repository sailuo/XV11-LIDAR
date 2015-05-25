# XV11-LIDAR
Contains related source code of XV11-LIDAR

## Firmware
Firmware for XV Lidar Controller V1.2 to control the Neato XV Lidar with an Arduino compatible board
### Description
The XV Lidar Controller receives the serial data from the XV Lidar looking for the RPM data embedded in the stream and uses a PID controller to regulate the speed to 300RPMs. The data received from the Lidar is relayed to the USB connection for some upstream host device to process the data.
### Requirements
- XV Lidar Controller with USB interface
- Arduino IDE
  - To allow communication via a serial port (which should follow the format /dev/ttyACMx, where x is a number arbitrarily assigned by the system).
  `sudo usermod -aG dialout <username>`
- Teensyduino - Software add-on to run Arduino sketches on the [Teensy](http://www.pjrc.com/teensy/teensyduino.html) (v1.19 tested. Newer or older may work)

## Software
XV-11 Laser Driver of ROS Package. 
This driver works with XV-11 laser as to reading scans from USB port.
### Launch driver
`rosrun xv_11_laser_driver neato_laser_publisher`
