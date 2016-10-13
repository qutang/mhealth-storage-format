# `sensor`

Used to store raw numerical sensor data in high or low sampling frequency.

## Filename convention

    SensorType-DataType.SENSORID-DATATYPE-VERSIONCODE.YYYY-MM-DD-HH-mm-ss-SSS-[M/P]HHmm.sensor.csv(.gz)

{% method %}

### SensorType {#SensorType}

1. Used to specify the type of sensor (or device, if multiple sensors are on the same device, such as phone, IMU device or smart watch).

2. Locally unique.

3. Camel Style, allowed characters: *alphabets* and *digits*.

4. Required.

{% common %} 

#### Examples
`AndroidPhone`, `AndroidWear`,`GT3X`,`GT9X`

See a [complete list](#) of predefined sensor types.

{% endmethod %}

{% method %}

### DataType

1. Used to specify the type of data this file refers to. The same device can support collecting multiple types of data, such as smart phone can be used to collect acceleration, orientation, light and sound. 

2. Locally unique.

3. Camel Style, allowed characters: *alphabets*.

4. Required.

{% common %}
#### Examples
`AccelerometerCalibrated`, `GPSLocation`, `Light`, `Sound`, `HeartRate`

See a [complete list](#) of predefined sensor data types.

{% endmethod %}

{% method %}

### SENSORID

1. A global unique identifier for a specific device. For most devices, it could be the serial number. For phone, it could also be the IMEI number.

2. UPPERCASE, allowed characters: *alphabets* and *digits*.

3. Required.

{% common %}
#### Examples
``, ``

See the predefined [list](#) for recommended sensor id sources for different sensor types.

{% endmethod %}

{% method %}
### DATATYPE

1. A local unique identifier for a specific sensor on a device. For single sensor device, it could be omitted. For IMU devices, it could be a descriptive string.

2. UPPERCASE, allowed characters: *alphabets* and *digits*.

3. Optional, if omitted, don't put `-` after `DEVICEID`.

{% common %}

#### Examples

`ACCEL`, `GYRO`

See a predefined [list](#) for recommended data id sources for different data types.

{% endmethod %}

{% method %}



### VERSIONCODE
1. Used to specify the version for the specific sensor, as firmware or software may be upgraded. This is used to distinguish data collected from the same sensor but with different firmware or software version.

2. CamelStyle, allowed characters: *alphabets* and *digits*.

3. Optional. If omitted, use `NA` as default.

{% common %}

#### Examples

`V1`, `V2`, `FW10`, `SW23`

{% endmethod %}

{% method %}
### Timestamp

1. Represent the start time or the first row's timestamp of current sensor data file.

2. `YYYY-MM-DD-HH-mm-ss-SSS-[M/P]HHmm`

3. In local time zone.

{% common %}

#### Examples

`M0500` means `UTC-5h` which is the United States Eastern Standard Time. See [wikipedia](https://en.wikipedia.org/wiki/List_of_tz_database_time_zones) for a complete map between time zone offset and time zone region code.

{% endmethod %}
