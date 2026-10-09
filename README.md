# IoT-Based Weather Monitoring System

A low-cost system that measures temperature, humidity and air quality and shows the readings live on a cloud dashboard that can be opened from any phone or computer.

*Mini Project (SE Semester 3, A. P. Shah Institute of Technology, University of Mumbai, 2023-24), team of 4. Published at SmartCom 2024 (Springer).*

## How it works

1. The **DHT11** sensor reads temperature and humidity (data pin on D4 of the NodeMCU).
2. The **MQ-135** sensor measures air quality, giving an analog voltage (connected to pin A0). It needs 3 to 5 minutes to warm up before readings are reliable.
3. The **NodeMCU ESP8266** reads both sensors and sends the values over Wi-Fi to the **Arduino IoT Cloud**.
4. The cloud dashboard shows live gauges and charts for temperature, humidity and air quality, and stores the data for later analysis.

## Components

| Part | Purpose |
|---|---|
| NodeMCU ESP8266 | Microcontroller with built-in Wi-Fi |
| DHT11 | Temperature (0-50 °C, about ±2 °C) and humidity (20-80%, about ±5%) |
| MQ-135 | Air quality / gas sensor (smoke, CO2, NH3 and others) |
| Arduino IoT Cloud | Dashboard and data storage |

## Files

- `weather-monitoring-presentation.pptx`: project presentation with the block diagram, circuit diagram, algorithm and dashboard screenshots

## Setup outline

1. Connect the sensors to the NodeMCU as described above and plug it into your computer by USB.
2. Create a free Arduino IoT Cloud account and add the NodeMCU as a device. Save the secret key it gives you.
3. Create a Thing with variables for temperature, humidity and air quality, then enter your Wi-Fi name, Wi-Fi password and the secret key in the Thing's settings (never share these publicly).
4. Upload the sketch and open the dashboard to see live values.

## Team

Maitreyi Phadke, Rutuja Pawar, Gauri Ramekar, Pratiksha Pathak. Guided by Prof. Monali Korde.
