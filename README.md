# Smart-Parking
An IoT Based Smart Parking System Using LoRa

# Overview

The LoRaWAN smart-parking solution used an Arduino based sensor node, a single-tech LoRa Gateway, TTN to host the Parking application server. The following are the detailed steps of how the application works:

1- The Arduino board detects the status of the parking spot by using an HC-SR04 ultrasonic sensors.

2- The status data is sent to the Single-Tech LoRa gateway via a RF95 Transceiver LoRa module connected to the Arduino board via serial connection.

3- The LoRa gateway is connected to a LoRa server on thethingsnetwork.org and forwards all packets it receives there

4- The TTN server forwards the received packages to a channel that the Application server is listening on

5- The Application Server also hosted on TTN listens to the PubNub channel and detects the status data of each parking spot.

6- After comparing the parking spot status data with the stored value, the parking application makes the decision of whether or not to send a notice message to the mobile app to update the status of a parking spot

# Architecture
The LoRa network utilises a telecommunications network called LoRaWAN that provides the routing of the data from the end node via a LoRaWAN gateway to the required entities. LoRaWAN also defiens the way in which data is sent around the network, detailing the responses of the LoRaWAN gateways, and the LoRa network server.

A LoRa network consists of several elements:


* End Device, Node, Mote - an object with an embedded low-power communication device. 
* Gateway - antennas that receive broadcasts from End Devices and send data back to End Devices. 
* Network Server - servers that route messages from End Devices to the right Application, and back. 
* Application - a piece of software, running on a server.
![Image of LoRa](https://github.com/MAmirS/Smart-Parking/blob/master/image/LoRaWAN-Overview.png)

# Gateway:
Hardware used
- Raspberry Pi 3 model B with pin diagram

![Image of LoRa](https://github.com/MAmirS/Smart-Parking/blob/master/image/raspberry.png)

# LoRa 
The  RFM95W transceivers  feature  the  LoRaTM  long range modem that provides ultra-long range spread spectrum communication and high interference immunity whilst minimising current consumption.

Using Hope RF’s patented LoRaTM modulation technique RFM95W can achieve a sensitivity of over -148dBm using a low cost crystal and bill of materials. The high sensitivity combined with the integrated +20 dBm power amplifier yields  industry  leading  link  budget  making  it optimal for any application requiring range or robustness. LoRaTM also provides significant advantages in both blocking and selectivity over conventional modulation techniques, solving the traditional design compromise between range, interference immunity and energy consumption.

These devices also support high performance (G)FSK modes for systems including WMBus, IEEE802.15.4g. The RFM95W deliver exceptional phase noise, selectivity, receiver linearity  and  IIP3  for  significantly lower  current consumption than competing devices.

![Image of LoRa](https://github.com/MAmirS/Smart-Parking/blob/master/image/2.png)


