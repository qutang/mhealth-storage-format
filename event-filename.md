# `event`

Store **formatted** event information (numerical or categorical) happens at a time point, such as EMA prompt questions and responses.

## Filename convention

```
EventType.SENSORID-EVENTID.YYYY-MM-DD-HH-mm-ss-SSS-[M/P]HHmm.event.csv
```

Event files are divided into **daily** files, as hourly files will be too sparse to be insightful.

{% method %}
### EventType

1. Used to describe the type of event.

2. CamelStyle, allowed characters: *alphabets* and *digits*.

3. Required.

4. Some of the events have the same name as sensor type, but are used for different purpose, mainly to record abnormal or change of status. Such as low battery, charging, bluetooth connect/disconnect, cpu wakeup/sleep, low storage, and low memory.

{% common %}

#### Examples

Smart phone events: `PhoneEMA`, `PhoneCall`, `PhoneSMS`, `Network`, `Battery`, `Bluetooth`, `CPU`, `Memory`, `ExternalStorage`, `InternalStorage`.

Indoor events: `ObjectMove`, `ObjectStatus`.

Outdoor events: `NearbyPlace`.

See a predefined [list](#) of event id and corresponding event types.

{% endmethod %}

### SENSORID

Same as sensor id described in sensor data.

### EVENTID

1. local identifier for event types.

2. UPPERCASE style, allowed characters: *alphabets*.

3. Optional, only used when SENSORID is not enough to globally identify an event type.

See a predefined [list](#) of event id and corresponding event types.

{% method %}

### Timestamp

1. Timestamp has the same convention as that of sensor data. The time represents the first row of event.

2. Because it's a daily file, normally there will only be one file for a day. 

3. In case time zone is changed during the day, there will be multiple files for one day.

{% common %}

#### Examples

If time zone changes from M0500 to M0300 at 10am on a day, and an event happens at 12pm in the old time zone, then there will be two files, one would be



{% endmethod %}



