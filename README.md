# IoT vehicle tracking - Report
A simple project demonstrating an IoT approach to vehicle tracking. The project has 3 software
components: node devices, the edge device, and the web client. Node devices notify the edge device
of new data via BLE GATT, which is then fetched by the edge device and cached locally in a redis
database. Data is then pushed to the cloud (AWS) via MQTT. When AWS receives data via MQTT, it is
stored in a dynamodb for later retreival. Finally, this data is pulled by the web client and presented
as both a table of values and a path on google maps (for GPS data).

This repository contains the final report, and extra components required to build the report. For
software components of the project, please see their corresponding repositories (in the
[Other repositories](#other-repositories) section below).

# The report
In this repository is the report for the IoT vehicle tracking proof of concept. The report itself is
constructed in LaTeX, but there is a pre-compiled version of the report that lives in
[the build directory](build/Report.pdf). Fritzing designs for the IoT nodes may be found in
[the extras directory](extras)

There is also an accompanying video that can be found [here on youtube](https://youtu.be/y33Iyd1M9NY).

# Other repositories
- [Node firmware](https://github.com/Aloz1/iot-nodes)
- [Edge application](https://github.com/Aloz1/iot-raspi)
- [Web client](https://github.com/Aloz1/iot-website)
