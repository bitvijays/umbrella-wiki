Introduction
************

- UMBRELLA provides an open, programmable, real-world platform for testing and evaluating innovation in robotics, wireless communication, smart city and general Internet of Things applications.
- It is a three-tier architecture consisting of a Backend (servers), an Edge (Small board computers) deployed on the street lamps/citizen houses/buildings and Endpoints (onboard sensors). 
- It consists of two smaller testbeds: smart city sensing and robotics.

TestBeds
========

Smart City Sensing and Wireless Testbed
---------------------------------------

It is deployed from the UWE Frenchay campus east to Bristol and Bath Science Park west, along the A4174 (a key thoroughfare in South Gloucestershire). It provide a real-world platform for testing wireless algorithms and protocols and smart city sensing. It consists of 

- 230 UMBRELLA Nodes (mounted on lamp posts)
- 1000+ Wireless Radio Nodes
- 1500+ Sensors (temperature, air quality and ambient noise levels)
- 100 Edge AI Nodes
- 1 Gbps Fibre Backbone

Capabilities
^^^^^^^^^^^^

- Scheduling and monitoring of experiments running in the testbeds
- Kubernetes/Docker-based upload and deployment of experiment software
- Test AI and Machine Learning algorithms on over 100 edge-capable nodes.
- Result log file retrieval for offline analysis
- Radio simulators to emulate the performance of radios
- Customised Firmware binary upload for radios
- External application access to REST API
- Push sensor data to external servers.
- Bring data to life using Grafana
- Single Sign-On (SSO) with role-based access control to securely access testbed resources through REST APIs

Robotics Testbed
----------------

Situated in the Bristol Robotics Lab, the robotic testbed consists of a 5x5m arena, 20 robotic nodes, and several obstacles and platforms. Use the testbed to evaluate which communications protocols and swarm AI algorithms work best for a robotic solution. 

Capabilites
^^^^^^^^^^^

- Simulation models (such as Gazebo) with customisable environments/worlds
- Ground truth data with millimetre accuracy for tracking robots

Advancing collaborative robotic AI
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Each robot is 25cm in diameter and can lift to 4kg individually but can collaborate to tackle larger and heavier payloads.

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
  - RockPi with four onboard cameras

State-of-the-art digital twin
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

The digital twin simulator allows running experiments virtually before taking to the robot arena. Access the digital twin from anywhere with an internet connection through the UMBRELLA Platform.

Who can use UMBRELLA?
=====================

Hardware Developers
-------------------

Developers can test the sensors or radio hardware using UMBRELLA. The hardware can be connected to an UMBRELLA node using standard interfaces such as USB, I2C and SPI. Developers can test hardware interaction with other IoT sensors and devices and further develop hardware by connecting it to the UMBRELLA platform.


Software Developers
-------------------

The developers can evaluate software algorithms and wireless protocol on the existing hardware on the UMBRELLA network.

Data Users
----------

Gain access to the data collected by over 1500 sensors across a large geographical area, both live and historic.

Data types include temperature, humidity, pm2.5, pm10, ambient noise, oxidising gas, spectrum sensing and GPS localisation.

Platform Users
--------------

The umbrella platform allows to 



Three-Tier Architecture
=======================

Backend Tier
------------

Edge Tier
---------

Edge node consists of small board computers (SBC) and an AI node that provides an IoT access point that can house a variety of radios and sensors in stylish, interchangeable modules based on your needs.

- Computing Power
    - All nodes are powered by a Raspberry Pi 3+.
    - Edge-capable nodes are powered further by a Jetson Nano
- Radios
    - Nordic Semiconductor nRF52840 with Power Amplifier – capable of both BLE and 802.15.4 using Contiki-NG
    - Texas Instruments CC1310 – 868MHz long-range radio supported by Contiki-NG
    - HopeRF RFM95W LoRa transceiver
    - RAKwireless RAK2247 LoRaWAN gateway (on selected nodes)
    - GPS receiver for time synchronisation
    - Wi-Fi radio for backbone connectivity
    - 4G cellular dongle for backup connectivity
- Enclosures
    - Equipment is housed in three large and three small diamond-shaped plastic modules. 
    - For new projects, different hardware can be plugged into the modules using USB 2.0. 
- Deployment
    - UMBRELLA nodes can be mounted on posts or walls in many settings, whether roadside on lamp posts, factory walls, or in shopping venues.

Endpoint Tier
-------------

- Sensors
    - Air Quality (VOC Index, Temperature, Humidity, Air Quality Index)
    - Multi-gas (RED, OX, NH3)
    - Particulate (PM2.5, PM10)
    - NO2
    - OX (Oxidising gas for ozone and nitrogen dioxide)
    - Noise (for measuring ambient noise levels)
- Other
    - Sky-facing camera (for use in street light monitoring)

Use cases
=========

Smart City Sensing and Wireless Testbed
---------------------------------------

Air Quality Sensing
^^^^^^^^^^^^^^^^^^^

Challenge
"""""""""

Road traffic is the primary source of air pollution. Air quality is affected by several factors relating to traffic:

- Whether the traffic is flowing or standing. 
- Traffic composition: the ratio of old to new vehicles, fuel types, and engine start/stop technology prevalence.
- The speed of the vehicles: the slower, the higher the concentration of pollution particles.
- Location: pollutants concentration quickly deteriorates as we move away from the carriageway.
- Street layout and adjacent building height (e.g. canyon effects)

The air quality is often measured using sample tubes placed at monitoring locations and collected over a few months. Sample tubes do not allow real-time collection, because of which the observation points are limited for effective policy-making around pollution risk mitigation.

The Approach
""""""""""""

- The UMBRELLA node allows the real-time measurement and collection of data on VOC Index, RED, Ozone, Ammonia, PM 2.5, PM 10, Air Temperature, Air Humidity, Air Quality Index, and NO2.
- UMBRELLA nodes can be placed roadside on lampposts every few tens of meters on either side of the road to ensure appropriate coverage. 


Street Light monitoring
^^^^^^^^^^^^^^^^^^^^^^^

Challenge
"""""""""
- Street lighting's primary function is to extend the number of light hours to allow activities to continue past sunset, especially in the darker winter months. In addition, street lights promote security in urban areas and generally make the use of roads and pathways safer. Issues with street lights must be resolved as soon as possible to prevent a possible accident.
- The city council often turn on the street lights 15 minutes before sunset and turn them off 15 minutes after sunrise. Street teams run periodic manual checks – roughly every four weeks by driving along stretches of road to check if street lights are showing normal behaviour, turning off and on when they are supposed to.

Approach
""""""""
- UMBRELLA nodes monitor the street light working with camera nodes attached to the top, pointing upwards towards the streetlight and sky. 
- The camera collects images of the streetlights at various times to train a machine learning model that determines if a street light is on and off at the appropriate times. 
- Once the machine learning algorithm detects that a street light is not working as intended, an alert is sent to the street care team, meaning they can monitor street lights passively whilst undertaking other tasks.
- The service allows the street care team to check the street lights' status in real-time without travelling to the street lights themselves.

The Benefits
""""""""""""
- Reduction in man hours, vehicle maintenance and fuel will translate into cost reductions for the street care team.
- Monitor the real-time status of any connected street light without needing to visit it.

Large Scale Wireless Testbed
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

The Challenge
"""""""""""""

- The Internet of Things (IoT) enables sensors to collect and share data about their environments via the internet and make them “smart”. It is crucial to design, develop and rigorously test the wireless protocol (e.g. Wifi, 5G, Bluetooth) used for network connectivity.

The Approach
""""""""""""

- UMBRELLA’s node includes multiple wireless technologies, including short-range, long-range, cellular, non-cellular, licensed and unlicensed technologies.
- The nodes are placed in indoor and outdoor locations, with the majority located in real-world locations across the South Gloucestershire region.
- Radios include IEEE 802.15.4, Bluetooth Low Energy, Ultrawideband, LTE/5G, NB-IoT, LoRa, 
- The UMBRELLA platform includes various tools that allow running network diagnostics, visualising wireless networks, collecting performance metrics and evaluating them against one another.

The Benefits
""""""""""""

- The presence of multiple radios in one testbed allows users to test their applications and protocols with multiple wireless technologies and evaluate them all on one platform.

Robotics Testbed
----------------

SWARM Robotics
^^^^^^^^^^^^^^

The Challenge
"""""""""""""

- In warehouse environments, robots move objects of various shapes and sizes without colliding and misjudging the objects. Without swarm robotic technology, the robots use centralised methods to collaborate and coordinate their movements requiring centralised processing and communication (expensive in terms of infrastructure required).
- The Collaborative warehouse storage solution uses swarm robotic technology, which exploits multiple robots collectively moving pallets containing objects. It improves performance, measured in terms of the time taken to store/retrieve the pallets and the resources, including battery energy. 
- Existing testbeds (Robotarium and IRIS) support collaborative robotics experimentation and are largely used for general swarm algorithm research and evaluation rather than being use-case specific.

The Approach
""""""""""""

- Swarm robots coordinate their activities in an autonomous self-configuring manner requiring no reliance on the infrastructure being deployed. 
- The Swarm robots use various sensors, including distance, camera, and radios, to obtain information about the environment. Robots process this information, and it forms the basis of their actions. The robots also contain radios to communicate with each other. 
- Digital twins are used to evaluate and optimising or evolve the algorithms. Algorithms are created and deployed to the digital twin simulator environment and the robots. The algorithms set goals and tasks for the robots to achieve. Performance is measured by how they collectively tackle these challenges.
- Objects or pallets to be moved by the robots and obstacles hinder the robot's movements. Up to 20 swarm robots can be involved in each experiment. Ground truth data is collected to validate and evaluate the performance of the robots in fulfilling their tasks.

The Benefits
""""""""""""

- Algorithms can be optimised and evaluated for performing particular tasks and environments without prior knowledge of the environment or infrastructure.
- Digital twin environments permit accurate representation and comparison with the real arena environment for validating, evolving, or optimising the algorithms.
- Zero initial configuration and infrastructure required.
