# Introduction

UMBRELLA provides an open, real world platform for the testing and evaluation of innovation in the fields of robotics, wireless communication, smart city and general Internet of Things applications. UMBRELLA is a three-tier architecture consisting of Backend (servers), Edge (Small board computers) deploy on the street lamps/citizen houses/buildings and Endpoints (on-board sensors). It is a open, programmable IoT testbed connecting key innovation areas of South Gloucestershire. It is made up of two smaller testbeds: smart city sensing and robotics.

## TestBeds

### Smart City Sensing and Wireless Testbed

Stretching from UWE Frenchay campus in the east to Bristol and Bath Science Park in the west, along the A4174 – a key thoroughfare in South Gloucestershire. These provide a real world platform for not only testing wireless algorithms and protocols but also smart city sensing. It consists of 

- 230 UMBRELLA Nodes (mounted on lamp posts)
- 1000+ Wireless Radio Nodes
- 1500+ Sensors (temperature, air quality and ambient noise levels)
- 100 Edge AI Nodes
- 1 Gbps Fibre Backbone

### Robotics Testbed

Situated in the Bristol Robotics Lab, the robotic testbed consists of an 5x5m arena, 20 robotic nodes, and a number of obstacles and platforms. Use the testbed to evaluate which communications protocols and swarm AI algorithms work best for your robotic solution. 

#### Advancing collaborative robotic AI

Each robot is 25cm in diameter and can lift up to 4kg individually, but can collaborate to tackle larger and heavier payloads.

- Communication and Management Stack
  - Bluetooth 5.0
  - Wi-Fi (802.11ac)
  - Ultra-wide Band
  - DDS
  - Support for custom protocol stacks
- Actuation
  - 3 x Omnidirectional wheels
  - Lifter
- GPU
  - RockPi with 4 onboard cameras

#### State of the art digital twin

The digital twin simulator allows you to run your experiments virtually before taking to the robot arena. Access the digital twin from anywhere with an internet connection through the UMBRELLA Platform.

## Who can use UMBRELLA?

### Hardware Developers

Test your sensor or radio hardware using UMBRELLA. Connect your hardware to an UMBRELLA node using common interfaces such as USB, I2C and SPI

Log in from anywhere with an internet connection to check on the status of your hardware experiments.

Test how your hardware interacts with other IoT sensors and devices.

Develop your hardware further by connecting it to the UMBRELLA platform to take advantage of:

- Scheduling and monitoring of experiments running in the testbeds
- Result log file retrieval for offline analysis
- Simulation models (such as Gazebo) with customisable environments / worlds
- Radio simulators – to emulate performance of radios

### Software Developers

Evaluate your software algorithms and wireless protocols on the UMBRELLA network.

How Can UMBRELLA Help You?
Get access to existing hardware to test your algorithms on.
Access the UMBRELLA platform and run experiments from anywhere in the world with an internet connection.
No Software licenses required.
Supports Contiki-NG.
Take advantage of the features of the UMBRELLA Platform:

- Kubernetes / Docker based upload and deployment of experiment software
- Scheduling and monitoring of experiments running in the testbeds
- Result log file retrieval for offline analysis
- Customised Firmware binary upload for radios
- Simulation models (such as Gazebo) with customisable environments / worlds
- Radio simulators – to emulate performance of radios
- External application access to REST API

### Data Users

Gain access to the data collected by over 1500 sensors across a large geographical area, both live and historic.

Data types include temperature, humidity, pm2.5, pm10, ambient noise, oxidising gas, spectrum sensing and GPS localisation.

- Test your AI and Machine Learning algorithms on over 100 edge capable nodes.
- Upload and deploy your experiment code using Kubernetes / Docker.
- Schedule and monitor of experiments running in the testbeds.
- Download your experimental results for use offline.
- Push sensor data to external servers.
- Bring your data to life using Grafana

### Platform Users

Develop your application further by connecting it to the UMBRELLA platform to take advantage of:

- Single Sign-On (SSO) with role-based access control to securely access testbed resources through REST APIs
- Kubernetes / Docker based upload and deployment of experiment software
- Scheduling and monitoring of experiments running in the testbeds
- Result log file retrieval for offline analysis
- Customised Firmware binary upload for radios
- Simulation models (such as Gazebo) with customisable environments / worlds
- Radio simulators – to emulate performance of radios
- External application access to REST APIs
- Ground truth data with millimetre accuracy for tracking robots
- Pushing sensor data to external servers

## UMBRELLA Three-Tier Architecture

### Backend Tier

### Edge Tier

The technological backbone that powers the UMBRELLA network. Provides an IoT access point that can house a variety of radios and sensors in stylish, interchangeable modules based on your needs.

- Computing Power
    - All nodes are powered by a Raspberry Pi 3+.
    - Edge capable nodes are powered further by a Jetson Nano
- Radios
    - Nordic Semiconductor nRF52840 with Power Amplifier – capable of both BLE and 802.15.4 using Contiki-NG
    - Texas Instruments CC1310 – 868MHz long-range radio supported by Contiki-NG
    - HopeRF RFM95W LoRa transceiver
    - RAKwireless RAK2247 LoRaWAN gateway (on selected nodes)
    - GPS receiver for time synchronisation
    - Wi-Fi radio for backbone connectivity
    - 4G cellular dongle for backup connectivity


Equipment is housed in 3 large and 3 small diamond shaped plastic modules. For new projects, different hardware can be plugged in to the modules using USB 2.0. UMBRELLA nodes can be mounted on posts or walls in many settings, whether it is roadside on lamp posts, on a factory wall, or in a shopping venue.

### Endpoint Tier

- Sensors
    - Air Quality – VOC Index, Temperature, Humidity, Air Quality Index.
    - Multi-gas – RED, OX, NH3.
    - Particulate – PM2.5, PM10.
    - NO2
    - OX – Oxidising gas for ozone and nitrogen dioxide.
    - Noise – for measuring ambient noise levels.
- Other
    - Sky-facing camera – for use with street light monitoring use case





