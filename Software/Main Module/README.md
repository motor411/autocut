The software on the main module is separated into two parts.

Webserver
---------
The webserver hosts a html file and some javascript. This builds up the webinteface. Nginx is recommended as webserver, since its more lightweight than apache - which is a good thing on a weak emdedded platform.

Commandserver
-------------
This is a websocket-server written in Python3. It receives commands, processes them and sends information back. The webinterface uses the commandserver to control the robot.

RobotLibrary is a pile of functions for communicating with other modules (drive, mow, powersupply...) via I2C easily. The Commandserver uses them to process the commands.
