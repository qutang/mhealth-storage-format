# `sensor`

Used to store raw numerical sensor data in high or low sampling frequency.

## Filename convention

    SensorType-DataType-VersionCode.SENSORID.YYYY-MM-DD-HH-mm-ss-SSS-[M/P]HHmm.sensor.csv(.gz)

### SensorType

1. Used to specify the type of sensor (or device, if multiple sensors are on the same device, such as phone, IMU device or smart watch)
2. Camel Style, allowed characters: alphabets and digits

### DataType

1. Used to specify the type of data this file refers to. The same device can support collecting multiple types of data, such as smart phone can be used to collect acceleration, orientation, light and sound.
