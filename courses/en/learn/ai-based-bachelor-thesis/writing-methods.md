---
title: "Writing: Methods"
lastUpdate: 2023-06-08T09:06:21.773Z
description: Quickstart Your Bachelor's Thesis with AI-powered Tools
metaOptions: [Learn, Quickstart Your Bachelor's Thesis with AI-powered Tools]
defaultName: Quickstart Your Bachelor's Thesis with AI-powered Tools
---

<RoboAcademyText fWeight="500">
We are starting to write the main section of the entire bachelor's thesis, in which the students should demonstrate their skills and completed work.
</RoboAcademyText>

It is expected that this section cannot be completely entrusted to the AI assistant, at least for the reason that these tools (currently) cannot configure and launch different physical devices (primarily sensors and smart devices). Nevertheless, we will consider several tactics that can make the preparation of this section easier.

## Generating text for Methods section

Firstly, an attempt was made to obtain at least some text for this section. As previously mentioned, the bachelor's thesis is based on the course **"Sovereign Smart Home with Robonomics and Home Assistant"**, so it is desirable to feed the entire course to the AI assistant to form the correct context. Once again, we encountered the problem of context limitations:

- Auto-GPT was not able to adequately check the course website on its own, constantly switching to sub-tasks or losing context. Attempting to feed the course text as a file also encountered the problem of too big context.
- Bing Chat has a limit of 2000-4000 characters, and the request to check the online course website was limited to a superficial overview.
- ChatGPT also did not accept a too large text.

As a result, the tactic of feeding the course text by lessons was chosen, while specifying the necessity of memorizing the context of the lessons. If no additional requests are made, AI assistants immediately suggest a plan for writing the Methods section. Here are a few examples:

<RoboAcademyDialog>

Methods

This section presents the methods employed to achieve the objectives of the study, which involved building a sovereign smart home with enhanced security and privacy features. The study was conducted as part of an online course titled "Smart Home Sovereign." The methods encompassed the setup of an IoT hub on a Raspberry Pi, connection of various smart devices to the hub using a Zigbee adapter and the MQTT protocol, integration of the hub with Home Assistant software, and the establishment of a connection between the hub and a decentralized cloud based on Polkadot web3 technology. These steps were taken to enable secure data transfer to the network and facilitate remote home management.

1\. Online Course: "Smart Home Sovereign"
The initial phase of the study involved the completion of the online course "Smart Home Sovereign." This course provided comprehensive guidance on building a sovereign smart home, emphasizing the importance of user data security and privacy. The bachelor successfully completed all the course modules, gaining a thorough understanding of the fundamental concepts and practical aspects related to the construction of a sovereign smart home.

2\. Setting up the IoT Hub
To establish a centralized control system for the smart home devices, an IoT hub was set up on a Raspberry Pi. The Raspberry Pi was selected due to its versatility, low cost, and compatibility with the desired functionalities. The IoT hub acted as the central communication point, facilitating the interaction between the smart devices and the user.

3\. Connecting Smart Devices
Various smart devices were integrated into the sovereign smart home system. These devices included a temperature/humidity sensor, a door sensor, a smart bulb, and a motion sensor, among others. A Zigbee adapter was utilized to connect these devices to the IoT hub, enabling seamless communication. The MQTT (Message Queuing Telemetry Transport) protocol was employed to establish a reliable and efficient communication channel between the hub and the connected devices.

4\. Integration with Home Assistant
The IoT hub was integrated with Home Assistant, an open-source home automation platform. Home Assistant provided a user-friendly interface for managing and controlling the connected smart devices. This integration allowed the bachelor to monitor and control the devices remotely, enhancing the convenience and functionality of the sovereign smart home system.

5\. Connection to Decentralized Cloud
To ensure secure data transfer without relying on a centralized cloud service provider, a decentralized cloud based on Polkadot web3 technology was employed. This connection facilitated the secure transfer of device data to the network, protecting user privacy and enabling remote home management. The bachelor established a connection between the IoT hub and the decentralized cloud, enabling seamless data transfer and access.

6\. Data Security and Privacy Measures
Throughout the implementation process, stringent data security and privacy measures were implemented. The bachelor ensured the adoption of industry-standard encryption protocols and authentication mechanisms to safeguard the integrity and confidentiality of the user's personal and device data. Additionally, measures such as secure network configurations and regular software updates were implemented to mitigate potential vulnerabilities and security risks.

</RoboAcademyDialog>

<RoboAcademyDialog>

1\. Description of the Smart Home System Design using web3 technology, including hardware and software components:

\- Describe the overall architecture of the smart home system.

\- Explain the hardware components involved, such as the Raspberry Pi, sensors, actuators, and communication modules.

\- Discuss the software components, including the operating system, middleware, and applications used to control and manage the smart home system.

\- Highlight the role of web3 technology, such as blockchain, decentralized networks, and protocols, in enhancing the security and privacy of the system.


2\. Implementation details and justification for design choices:

\- Provide a step-by-step account of how the smart home system was implemented, including the installation and configuration processes.

\- Justify the selection of specific hardware and software components based on their compatibility, reliability, security features, and suitability for the project's objectives.

\- Discuss any modifications or customization made to the hardware or software components to meet the specific requirements of the smart home system.

\- Explain how the chosen web3 technology (e.g., blockchain, decentralized networks) addresses security and privacy concerns compared to traditional approaches.

3\. Evaluation plan for assessing the security and privacy of the system:

\- Outline the goals and objectives of the security and privacy evaluation.

\- Identify the specific security and privacy aspects to be evaluated, such as data encryption, access control, authentication, and data integrity.

\- Describe the evaluation methods and techniques to be used, such as penetration testing, vulnerability assessments, or simulations.

\- Explain how data will be collected, analyzed, and interpreted to assess the effectiveness of the implemented security and privacy measures.

\- Discuss any ethical considerations and potential risks associated with the evaluation process.

</RoboAcademyDialog>

As a result, the best tactic was manual selection of items from different plans for the section, and feeding them sequentially and in parts. It is important not to forget the context, reminding that the AI assistant should perform its task based on the source material.

## Generating illustrations

Good thesis is able to present material in a graphical form, so it is necessary to at least try to do it with the help of AI. There is a lot written about the capabilities of different models, such as MidJourney, DALL-E, Stable Diffusion, and other services, but they are primarily designed for generating art, not strict diagrams and charts. Very often, they cannot insert the correct text, and in general, the illustrations obtained are often too clumsy.

As an example, let's try to create a diagram of the following content in Bing Chat, which will redirect the request to Bing Image Creator:

<RoboAcademyDialog>

Make image with diagram based on this description:

There are 4 main blocks: Raspberry Pi, Smart Devices, Zigbee Adapter and Web3 Decentalized Cloud. Zigbee Adapter is connected by a double-ended arrow to Smart Devices, the arrow has the name "Zigbee".

Inside Raspberry Pi there are 4 more internal blocks: Zigbee2MQTT, MQTT Broker, Home Assistant and "robonomics-interface". Zigbee2MQTT is connected by a double-ended arrow to MQTT Broker, the arrow has the name "MQTT". MQTT Broker is connected by a double-ended arrow to Home Assistant, the arrow has the name "MQTT". Home Assistant is connected by a double-ended arrow to "robonomics-interface", the arrow has the name "Robonomics Data".

Also, internal block Zigbee2MQTT is connected by a double-ended arrow to Zigbee Adapter, the arrow has the name "Zigbee". Internal block "robonomics-interface" is connected by a double-ended arrow to Web3 Decentalized Cloud, the arrow has the name "data & events".

</RoboAcademyDialog>

Results:

<robo-academy-grid :columns="3" textAlign="center">
    <robo-academy-grid-element>
      <LessonImages src="ai-based-bachelor-thesis/bad-diagram1.jpeg" alt="Diagram example from Bing"/>
    </robo-academy-grid-element>
    <robo-academy-grid-element>
      <LessonImages src="ai-based-bachelor-thesis/bad-diagram2.jpeg" alt="Diagram example from Bing"/>
    </robo-academy-grid-element/>
    <robo-academy-grid-element>
      <LessonImages src="ai-based-bachelor-thesis/bad-diagram3.jpeg" alt="Diagram example from Bing"/>
    </robo-academy-grid-element/>
</robo-academy-grid>

It is better to ask to create code for a diagram, for example in UML, and then generate an illustration in a diagram editor. For example, a similar request in ChatGPT with the addition of `Make UML diagram code based on this description`, after several attempts, produced the following result:

<robo-academy-grid :columns="2" textAlign="center">
    <robo-academy-grid-element>
<LessonCodeWrapper language="uml" noCopyIcon noLines codeClass="big-code">
        @startuml
        package "Raspberry Pi" {
            [Zigbee2MQTT]
            [MQTT Broker]
            [Home Assistant]
            [robonomics-interface]
        }
        Zigbee2MQTT o--o "MQTT Broker" : MQTT
        "MQTT Broker" o--o "Home Assistant" : MQTT
        "Home Assistant" o--o "robonomics-interface" : "Robonomics Data"
        rectangle "Smart Devices"
        rectangle "Zigbee Adapter"
        "Zigbee Adapter" o--o "Smart Devices" : Zigbee
        "robonomics-interface" o--o "Web3 Decentalized Cloud" : "data & events"
        Zigbee2MQTT o--o "Zigbee Adapter" : Zigbee
        @enduml

</LessonCodeWrapper>
    </robo-academy-grid-element>
    <robo-academy-grid-element>
      <LessonImages src="ai-based-bachelor-thesis/system-diagram.png" alt="Diagram after producing UML code"/>
    </robo-academy-grid-element/>
</robo-academy-grid>

## Generating Code

Although an AI assistant cannot set up a device on its own, it can be asked to help write software for it. For our bachelor's thesis, to test the functionality of the installed smart home software, we decided to create an automation for Home Assistant based on a scenario. The following request was sent to AutoGPT:

<RoboAcademyTerminal title="AutoGPT Terminal">

AI Name: Hass-GPT 

Hass-GPT is: an AI that creates automation scripts for Home Assistant based on the text description

Goal 1: Open https://www.home-assistant.io/examples/ and analyze script codes of automations

Goal 2: Create automation script code with following scenario: turn on the bulb when motion sensor detects someone; while motion is present, keep the bulb turned on; when the motion stops, turn the bulb off

Goal 3: Write this code to the file and return it back

</RoboAcademyTerminal>

As a result of AutoGPT, the following script was generated:

<LessonCodeWrapper language="yaml" noCopyIcon codeClass="big-code">
    - alias: "Motion Sensor Bulb Control"
      trigger:
        platform: state
        entity_id: binary_sensor.motion_sensor
        to: "on"
      action:
        service: light.turn_on
        entity_id: light.bulb
    - alias: "Motion Sensor Bulb Keep On"
      trigger:
        platform: state
        entity_id: binary_sensor.motion_sensor
        to: "on"
      action:
        service: light.turn_on
        entity_id: light.bulb
    - alias: "Motion Sensor Bulb Off"
      trigger:
        platform: state
        entity_id: binary_sensor.motion_sensor
        to: "off"
        for:
          minutes: 1
      action:
        service: light.turn_off
        entity_id: light.bulb
</LessonCodeWrapper>

Of course, the script required additional adjustment for specific sensors and devices entities, but overall the request was processed correctly.

<RoboAcademyText>

So, practice has shown that despite the fact that AI cannot handle this section completely on its own, it can at least greatly assist with some tasks or provide ideas for their solutions. In the next section, we will explore how AI tools can help analyze the obtained results and format the corresponding section.

</RoboAcademyText>