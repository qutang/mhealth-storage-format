# `sensor`

Used to store raw numerical sensor data in high or low sampling frequency.

## Filename convention

    SensorType-DataType-VersionCode.DEVICEID-SENSORID.YYYY-MM-DD-HH-mm-ss-SSS-[M/P]HHmm.sensor.csv(.gz)

{% method %}

### SensorType {#SensorType}

1. Used to specify the type of sensor (or device, if multiple sensors are on the same device, such as phone, IMU device or smart watch).

2. Camel Style, allowed characters: *alphabets* and *digits*.

3. Required

{% common %} 

#### Examples
`AndroidPhone`, `AndroidWear`,`GT3X`,`GT9X`

See a [complete list](#) of predefined sensor types.

{% endmethod %}

{% method %}

### DataType

1. Used to specify the type of data this file refers to. The same device can support collecting multiple types of data, such as smart phone can be used to collect acceleration, orientation, light and sound.

2. Camel Style, allowed characters: *alphabets*.

3. Required

{% common %}
#### Examples
`AccelerometerCalibrated`, `GPSLocation`, `Light`, `Sound`, `HeartRate`

See a [complete list](#) of predefined sensor data types.

{% endmethod %}

{% method %}

### VersionCode

1. Used to specify the version for the specific sensor, as firmware or software may be upgraded. This is used to distinguish data collected from the same sensor but with different firmware or software version.

2. CamelStyle, allowed characters: *alphabets* and *digits*.

3. Optional. If omitted, use `NA` as default.

{% common %}
#### Examples
`V1`, `V2`, `FW10`, `SW23`

{% endmethod %}

### SENSORID

1. A global unique identifier for a specific device. For most devices, it could be the serial number. For phone, it could also be the IMEI number.

2. Required.
