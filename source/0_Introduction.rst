Introduction
************

- UMBRELLA stands for The Urban Multi wireless BRoadband and IoT tEsting for LocaL authority and industrial Applications.
- It aims to be a centre of excellence for open research, innovation, and future industrial IoT and integrate many testbeds into a single system and address different use cases, including Smart City test beds for air quality monitoring, remote maintenance, and radio testing; Cybersecurity test beds; industrial 5g; and collaborative robotics. 
- Supported by the `West of England Local Enterprise Partnership <https://www.westofengland-ca.gov.uk/about-us/local-enterprise-partnership/>`_ in conjunction with `South Gloucestershire Council <https://www.southglos.gov.uk/>`_.


Here is a small video to provide a brief introduction.

.. video:: _static/Video/Umbrella_Video2.mp4
   :width: 500
   :height: 300

Testbeds
========

UMBRELLA consists of three testbeds

- Smart City Sensing and Wireless
- Robotics
- LoRa

Smart City Sensing and Wireless Testbed
---------------------------------------

- Deployed from the UWE Frenchay campus east to Bristol and Bath Science Park west, along the A4174 (a key thoroughfare in South Gloucestershire). 
- Provides a real-world platform for testing wireless algorithms, protocols, and smart city sensing. 
- Consists of
 
    - 230 UMBRELLA Nodes (mounted on lamp posts)
    - 1000+ Wireless radio nodes
    - 1500+ Sensors (temperature, air quality and ambient noise levels)
    - 100 Edge AI nodes
    - 1 Gbps Fibre backbone

Testbed features and Benefits
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

- Allows scheduling and monitoring of experiments running in the testbeds using Kubernetes/Docker-based upload and deployment of experiment software.
- Customised firmware binary upload for radios with radio simulators to emulate radios performance.
- Test AI and Machine Learning algorithms on over 100 edge-capable nodes.
- Container log file retrieval for offline analysis with push sensor data capabilities to external servers and data visualisation using Grafana.
- Single Sign-On (SSO) with role-based access control to securely access testbed resources through REST APIs.


Robotics Testbed
----------------

- The first testbed supporting both multi-radio customisable protocol and SWARM simulation and arena deployment.
- Situated in the Bristol Robotics Lab (BRL) consisting of a 5x5m arena, 20 robotic nodes, and several obstacles and platforms.

Testbed features and Benefits
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

- Dockerised container experimentation (Easy deployment and management of experiments)
- `ROS2 <https://www.ros.org/>`_ and `Data Distribution Service <https://opendds.org/>`_ (Secure and real-time pub/sub)
- Gazebo Digital Playground (Realistic validation and experimentation)
- Robot nodes (Lifter actuator + Many sensors/radios for flexibility)
- Ground truth telemetry (High resolution and accuracy for record + comparison/playback)
- Multi-wireless technology, including private 5G (Bluetooth, UWB, Wi-Fi, private 5G)
- The digital twin simulator allows running experiments virtually before taking to the robot arena.


Use-case key features
^^^^^^^^^^^^^^^^^^^^^

- Use the testbed to evaluate communications protocols and swarm AI algorithms for a robotic solution. 
- Simulation models (such as Gazebo) with customisable environments/worlds
- Evaluation of SWARM for Warehouse applications (fetch/carry) using:
  
  - Radio communication protocols optimised for collaborative robotics 
  - Rich set of sensors and actuators, and cameras
  
- Other applications that users can evaluate:
  
  - Surveying, environment mapping, remote operation assisted multi-robot systems and functional safety aspects of cooperative robotics
  - Large SWARM/environment scenarios (through simulation)
  - Wireless/minimal infrastructure localisation technologies
  
- Decentralised industrial IoT Bus support using DDS/ROS2
- Optitrack™ ground truth data with millimetre accuracy for tracking robots and performance evaluation


Users
=====

Hardware Developers
-------------------

Developers can test the sensors or radio hardware. The hardware can be connected to an UMBRELLA node using standard interfaces such as USB, I2C and SPI.


Software Developers
-------------------

The developers can evaluate software algorithms and wireless protocol on the existing hardware on the UMBRELLA network.

Data Users
----------

- Gain access to the data collected by over 1500 sensors across a large geographical area, both live and historic.
- Data types include temperature, humidity, pm2.5, pm10, ambient noise, oxidising gas, spectrum sensing and GPS localisation.

Platform Users
--------------

The umbrella platform allows software and application development with consultation with the team and project requirements.

Use cases
=========

Smart City Sensing and Wireless Testbed
---------------------------------------

The smart city sensing and wireless testbed have multiple use cases, such as air quality sensing, street light monitoring, and large-scale wireless radio testing.

Air Quality Sensing
^^^^^^^^^^^^^^^^^^^

Challenge
"""""""""

Air quality is affected by several factors relating to traffic:

- Whether the traffic is flowing or standing. 
- Traffic composition: the ratio of old to new vehicles, fuel types, and engine start/stop technology prevalence.
- The speed of the vehicles: the slower, the higher the concentration of pollution particles.
- Location: pollutants concentration quickly deteriorates as we move away from the carriageway.
- Street layout and adjacent building height (e.g. canyon effects)

The air quality is often measured using sample tubes placed at monitoring locations and collected over a few months making limited observation points for effective policy-making around pollution risk mitigation.

Approach
""""""""

- The UMBRELLA node allows the real-time measurement and collection of data on Volatile Organic Compunds (VOC) Index, RED, Ozone, Ammonia, PM 2.5, PM 10, air temperature, air humidity, air quality index, and NO2.
- UMBRELLA nodes can be placed roadside on lampposts every few tens of meters on either side of the road to ensure appropriate coverage. 

Street Light monitoring
^^^^^^^^^^^^^^^^^^^^^^^

Challenge
"""""""""
- Street lighting's primary function is to extend the number of light hours to allow activities to continue past sunset, especially in the darker winter months. In addition, street lights promote security in urban areas and generally make the use of roads and pathways safer. The City council must resolve issues with street lights as soon as possible to prevent a potential accident.
- The city council often turn on the street lights 15 minutes before sunset and turns them off 15 minutes after sunrise. Street teams run periodic manual checks (roughly every four weeks) by driving along stretches of road to check if street lights are showing normal behaviour, turning off and on when they are supposed to.

Approach
""""""""
- UMBRELLA nodes monitor the street light working with camera nodes attached to the top, pointing upwards towards the street light and sky. 
- The camera collects images of the street lights at various times to train a machine-learning model that determines if a streetlight is on and off at the appropriate times. 
- Once the machine learning algorithm detects that a street light is not working as intended, an alert is sent to the street care team, meaning they can monitor streetlights passively whilst undertaking other tasks.
- The service allows the street care team to check the street lights' status in real-time without travelling to the street lights themselves.

Benefits
""""""""
- Reduction in person hours, vehicle maintenance and fuel will translate into cost reductions for the street care team.
- Monitor the real-time status of any connected street light without needing to visit it.

Large Scale Wireless Testbed
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Challenge
"""""""""

- The Internet of Things (IoT) enables sensors to collect and share data about their environments via the internet and make them “smart”. It is crucial to design, develop and rigorously test the wireless protocol (e.g. Wi-Fi, 5G, Bluetooth) used for network connectivity.

Approach
""""""""

- UMBRELLA's node includes multiple wireless technologies, including short-range, long-range, cellular, non-cellular, licensed and unlicensed technologies.
- The nodes are placed in indoor and outdoor locations, with the majority located in real-world locations across the South Gloucestershire region.
- Radios include IEEE 802.15.4, Bluetooth Low Energy, Ultrawideband, LTE/5G, NB-IoT, LoRa, 
- The UMBRELLA platform includes various tools that allow running network diagnostics, visualising wireless networks, collecting performance metrics and evaluating them against one another.

Benefits
""""""""

- The presence of multiple radios in one testbed allows users to test their applications and protocols with various wireless technologies and evaluate them on one platform.

Robotics Testbed
----------------

SWARM Robotics
^^^^^^^^^^^^^^

Challenge
"""""""""

- In warehouse environments, robots move objects of various shapes and sizes without colliding and misjudging the objects. Without swarm robotic technology, the robots use centralised methods to collaborate and coordinate their movements requiring centralised processing and communication (expensive in terms of infrastructure required).
- The Collaborative warehouse storage solution uses swarm robotic technology, which exploits multiple robots collectively moving pallets containing objects. It improves performance, measured in terms of the time taken to store/retrieve the pallets and the resources, including battery energy. 
- Existing testbeds (`Robotarium <https://arxiv.org/abs/1609.04730>`_ and `IRIS <https://www.fed4fire.eu/testbeds/iris/>`_) support collaborative robotics experimentation and are primarily used for general swarm algorithm research and evaluation rather than being use-case specific.

Approach
""""""""

- Swarm robots coordinate their activities in an autonomous self-configuring manner requiring no reliance on the infrastructure being deployed. 
- The Swarm robots use various sensors, including distance, camera, and radios, to obtain environmental information. Robots process this information, and it forms the basis of their actions. The robots also contain radios to communicate with each other. 
- Digital twins are used to evaluate and optimise or evolve the algorithms. Algorithms are created and deployed to the digital twin simulator environment and the robots. The algorithms set goals and tasks for the robots to achieve. Performance is measured by how they collectively tackle these challenges.
- Objects or pallets to be moved by the robots and obstacles hinder the robot's movements. Users can involve up to 20 swarm robots in each experiment. Ground truth data is collected to validate and evaluate the performance of the robots in fulfilling their tasks.

Benefits
""""""""

- Algorithms can be optimised and evaluated for performing particular tasks and environments without prior knowledge of the environment or infrastructure.
- Digital twin environments permit accurate representation and comparison with the real arena environment for validating, evolving, or optimising the algorithms.
- Zero initial configuration and infrastructure required.


Private 5G Use-case for Warehousing and Logistics
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Challenge
"""""""""
- 5G provides an unprecedented capability of a unified wireless interface for diverse IIoT applications. 
- Private 5G networks provide customised service with dedicated coverage, capacity, and intrinsic network control. 
- Most existing testbeds lack 5G capabilities as an end-to-end IIoT system.

Approach
""""""""

- The UMBRELLA offers the capability to test, evaluate, and trial private 5G technology and support different use cases, such as versatile warehousing and logistics scenarios, as part of an end-to-end IIoT system. 
- Private 5G connectivity is provided through a 5G network-in-a-box solution which includes a radio access network (RAN) and a core network and supports commercial off-the-shelf (COTS) devices like handsets and dongles.
- The private 5G network is based on non-standalone (NSA) mode and can operate in several sub-6 GHz frequency bands, including those opened explicitly for private deployments.
