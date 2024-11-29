1.

Data
wireless communication
QR code for each trucks
radar

Signal
detection
anti-collision
lateral control technology
GPS localization
LIDAR Sensor to see the distance and not go wrong

Events
Coupling and Decoupling
No signal

2. How can the distance to the precedence truck be guaranteed ?

The distance can be guaranteed via the LIDAR sensor in order to measure the car which has gone. If the truck has gone it will be detected by the sensor . The LIDAR will send some signal to the previous truck and with the signal repelled . The information getted by the sensor will permit to know the distance.

What happen in cases of a e.g. communication failure - > is your
system robust / still stable?

If the communication has failed , the system will locate via the gps localization of the primary truck . It permits to know in real time the localization of the truck.The
LIDAR sensor will use the signal to see with the precedent truck .
I should dp the state machine yet for both tasks
