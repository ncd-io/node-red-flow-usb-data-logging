# node-red-flow-usb-data-logging
A Node-RED flow to implement sensor data logging to a USB drive connected to the Enterprise IIoT Gateway

Flow to check for a connected FAT32-formatted USB drive to the Enterprise IIoT Gateway's USB port
<img width="708" height="114" alt="check-usb-path" src="https://github.com/user-attachments/assets/680cb5a6-7b01-4d74-bdc6-15f770e4478f" />

Flow to receive, filter and format the sensor data and saves it into CSV files
<img width="1671" height="274" alt="save-into-csv" src="https://github.com/user-attachments/assets/22e1e975-8179-4732-a876-717efee8dc00" />

NCD Sensors Metadata:
- **Time**: The time at which the data was received and processed, in the format: HH:MM:ss
- **Fimrware Version**: The current firmware version on the sensor
- **Transmission Counter**: Represents the count of data transmissions emitted by the sensor (1-255).
- **Battery Percentage**: Represents the battery percentage of the sensor at the time the data transmission was made.
- **RSSI (Optional)**: The received signal strength indicator measures the amount of power present in a radio signal. It is an approximate value for signal strength received

CSV Sensor Data Example (type 108):
<img width="1793" height="211" alt="csv-format-example" src="https://github.com/user-attachments/assets/916050c5-edbc-4c38-af48-02eeb180e240" />

**msg.payload.sensor_data**: Contains the field variables (depending on the type of sensor; pressure, temperature, humidity, vibration, current, etc.) emitted by the sensor.

