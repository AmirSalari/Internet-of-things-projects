# Smart-Parking
Internet of Things (IoT) has the potential to revolutionize health monitoring by connecting various devices to collect and transmit data in real-time. IoT can be used in a variety of health monitoring applications. The Internet of Things (IoT) has revolutionized health monitoring by enabling real-time monitoring of patients' health status, vital signs and medical conditions. This has improved the accuracy and efficiency of healthcare delivery and allowed for remote patient monitoring. IoT devices such as wearable devices, smart pills, and smart medical devices can collect, store, and transmit data to healthcare providers, helping them to make informed decisions. This has led to better patient outcomes and reduced healthcare costs. For example, wearable devices can monitor heart rate, sleep patterns, and physical activity levels, while smart pills can track medication adherence and even monitor the digestive system. IoT is also being used in hospitals to improve the efficiency of medical equipment and to reduce the risk of medical errors.


![Image of LoRa](https://github.com/AmirSalari/Internet-of-things-projects/blob/7f79768922e3f24ddad52041e38a2c1dfbd4e9cc/image/iothealth.png)

# Smart-Parking
The Internet of Things (IoT) plays a significant role in smart parking systems. IoT-enabled sensors and devices are used to monitor the availability of parking spots in real-time and provide drivers with information about the location of available spots, as well as the estimated time to find a spot. This helps to reduce traffic congestion and air pollution caused by drivers searching for parking. IoT-based smart parking systems also allow for dynamic pricing based on demand, which can help to optimize the utilization of parking resources.

Smart parking systems using IoT can also enable real-time payment and enforcement through connected devices, reducing the need for physical payment and enforcement systems. Additionally, IoT-enabled data analytics can provide valuable insights into parking usage patterns and trends, helping cities to optimize their parking infrastructure and improve overall transportation efficiency. Overall, the use of IoT in smart parking systems has the potential to significantly improve the parking experience for drivers and cities alike.

![Image of LoRa](https://github.com/AmirSalari/Internet-of-things-projects/blob/c7d0545d99a474a9e0f0c454d36ef97783ce67b9/image/iot-parking.jpg)


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

![Image of LoRa](https://github.com/MAmirS/Smart-Parking/blob/master/image/2.jpg)


