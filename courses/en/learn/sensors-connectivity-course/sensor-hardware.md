---
title: "Lesson #2, Sensor hardware"
lastUpdate: Thu May 04 2023 12:54:12 GMT+0400 (Samara Standard Time)
description: 'SENSOR HARDWARE'
lessonNumber: 2
metaOptions: [Learn, Sensors Connectivity & Decentralized Sensors Network]
defaultName: Sensors Connectivity & Decentralized Sensors Network
---

If you wish to participate in the air monitoring with Decentralized Sensors Network you need to obtain an air pollution board with sensors. There are two ways to do it:

<List>

<li>order all necessary parts and assemble the custom board by yourself.</li>
<li>order a ready-to-use board from Robonomics team.</li>

</List>

## Manual Board Assembly

To build your own board, you need to find the following components:

- Laser PM2.5 and PM10 Sensor [SDS011](https://www.amazon.com/SDS011-Quality-Detection-Conditioning-Monitor/dp/B07FSDMRR5)

- Serial wireless module [NodeMcu V3 CH340](https://www.amazon.com/ACEIRMC-Wireless-Development-Compatible-MicroPython/dp/B092ZCG2X2) based on ESP8266

- 5A DC-DC mini560 convertor [(example)](https://www.amazon.com/Alinan-Efficiency-Converter-Regulator-Stabilized/dp/B09W8P1QNM)

- DC connector [(example)](https://www.amazon.com/CenryKay-DC-099-Threaded-Connector-Adapter/dp/B08CMMQMP6?th=1)

- 12V/2А power adapter [(example)](https://www.amazon.com/TMEZON-Power-Adapter-Supply-2-1mm/dp/B00Q2E5IXW)

- mounting box [(example)](https://www.amazon.com/LeMotech-Dustproof-Waterproof-Electrical-300mmx250mmx120mm/dp/B075DHT7X2/ref=sxin_18_ac_d_mf_brs?ac_md=7-4-TGVNb3RlY2g%3D-ac_d_mf_brs_brs&content-id=amzn1.sym.1ad31f34-ba12-4dca-be4b-f62f7f5bb10d%3Aamzn1.sym.1ad31f34-ba12-4dca-be4b-f62f7f5bb10d&crid=2ZDX87O7MINYG&cv_ct_cx=junction+box+plastic&keywords=junction+box+plastic&pd_rd_i=B075DHT7X2&pd_rd_r=2bbd50d4-9ef9-4fa1-a1a2-e55c482bce49&pd_rd_w=EcHLy&pd_rd_wg=z42mC&pf_rd_p=1ad31f34-ba12-4dca-be4b-f62f7f5bb10d&pf_rd_r=WDAX58YZKG6YKZ70X5QE&qid=1676642125&sprefix=Junction+Box%2Caps%2C451&sr=1-4-8b2f235a-dddf-4202-bbb9-592393927392)

Also, you can install additional sensors:

<List  type="numbers">

<li>

With I2C interface:

<List>

<li>

[BMP180](https://cdn-shop.adafruit.com/datasheets/BST-BMP180-DS000-09.pdf) — temperature and humidity

</li>

<li>

[BME/P280](https://www.mouser.com/datasheet/2/783/BST-BME280-DS002-1509607.pdf) — temperature, humidity, atmospheric pressure

</li>

<li>

[HTU21D](https://eu.mouser.com/ProductDetail/Measurement-Specialties/HTU21D?qs=tx5doIiTu8oixw1WN5Uy8A%3D%3D) — temperature and humidity

</li>

<li>

[CCS811 VOC SENSOR](https://www.sciosense.com/wp-content/uploads/documents/Application-Note-Baseline-Save-and-Restore-on-CCS811.pdf) — volatile organic compounds, CO2 equivalent

</li>

</List>

</li>

<li>

With 1-Wire interface:

<List>

<li>

[DHT22(AM2302)](https://files.seeedstudio.com/wiki/Grove-Temperature_and_Humidity_Sensor_Pro/res/AM2302-EN.pdf) — temperature and humidity

</li>

<li>

[DS18B20](https://cdn.sparkfun.com/datasheets/Sensors/Temp/DS18B20.pdf) — temperature

</li>

</List>

</li>

</List>

You can find the assembly process in the video below. It also shows the flashing process, but we will talk about it later.

<RoboAcademyYoutube link="https://www.youtube.com/watch?v=OdTd1sacCso" />

## Request Robonomics Board

Alternatively, you can request Robonomics Board. To do so, send email to one of the following addresses:

- vm@multi-agent.io
- ping@airalab.org

Robonomics board is based on ESP8266 and is designed for 6-24V power supply, using DC-DC converter DC MINI560. This board allows you to connect SDS011 particle sensor and several additional sensors (check the list above). There is also a smaller MINI model with aa shortened list of connectable devices.

<LessonImages figure figureCaption="Full model of Robonomics board" src="sensors-connectivity-course/lesson-2-1.png" alt="Full model of Robonomics board"/>

<LessonImages  figure figureCaption="Mini model of Robonomics board" src="sensors-connectivity-course/lesson-2-2.png" alt="Mini model of Robonomics board"/>

The blueprints for both models can be found here: for [full model](https://oshwlab.com/ludovich88/aira_sensor_rev0-1) and for [mini model](https://oshwlab.com/ludovich88/aira_sensor_d1_mini).

Let's take a closer look at the board. It has several connector ports for connection (they are highlighted in blue and green).

<LessonImages imageClasses="mb" src="sensors-connectivity-course/lesson-2-3.png" alt="Full model of Robonomics board"/>

Blue terminal block, from left to right (all terminals are signed):

<List>
  <li class="flex">

  <code>12V</code> — terminal for connecting the power supply to the board; the recommended voltage is 12 volts.

  </li>

  <li class="flex">

  <code>GND</code> of ground (point of zero potential) — serves both for connection of zero potential of the power supply, and for connection of sensors.

  </li>

  <li class="flex">

  <code>POWER SENSOR</code> — configurable power output to which sensors are connected; the output can be set to 3.3 or 5 volts.

  </li>

  <li class="flex">

  <code>SDA</code> — serial data line, is used to connect sensors via the I2C interface.

  </li>

  <li class="flex">

  <code>SCL/1WIRE</code> — configurable terminal to which the serial clock line is connected; used to connect sensors via I2C or 1-Wire interface.

  </li>
</List>

Setting the power output for the sensor and selecting the interface is done by setting the jumpers, marked yellow in the image (`5V`, `3V`, `I2C`, `1WIRE`). The jumpers are installed horizontally, the places for installing the jumpers are signed.


<RoboAcademyNote type="warning" title="WARNING">
You can choose the voltage for the power supply by setting only one jumper to 3.3 volts or 5 volts. Setting two jumpers to 3.3 and 5 volts will damage the device. The same rule works when choosing an interface for sensors, install only one jumper in place of I2C or 1-Wire. Installing two jumpers may damage the device.
</RoboAcademyNote>

The board has additional block of inputs, marked green in the image (`GND`, `5V`, `SDA`, `SCL`).

On the left side of the blue box there is a power switch to force the board to reboot. It is in the `ON` position by default.

After setting up the sensor, all that remains is to flash and configure it.

