# `sensor`

Used to store raw numerical sensor data in high or low sampling frequency.

## Filename convention

    SensorType-DataType-VersionCode.SENSORID.YYYY-MM-DD-HH-mm-ss-SSS-[M/P]HHmm.sensor.csv(.gz)

{% method -%}

### SensorType

1. Used to specify the type of sensor (or device, if multiple sensors are on the same device, such as phone, IMU device or smart watch).

2. Camel Style, allowed characters: *alphabets* and *digits*.

3. Required

### DataType

1. Used to specify the type of data this file refers to. The same device can support collecting multiple types of data, such as smart phone can be used to collect acceleration, orientation, light and sound.

2. Camel Style, allowed characters: *alphabets*.

3. Required

### VersionCode

1. Used to specify the version for the specific sensor, as firmware or software may be upgraded. This is used to distinguish data collected from the same sensor but with different firmware or software version.

2. CamelStyle, allowed characters: *alphabets* and *digits*.

3. Optional. If omitted, use `NA` as default.

### SENSORID

1. Used to uniquely 
