# `event`

Store **formatted** event information (numerical or categorical) happens at a time point, such as EMA prompt questions and responses.

## Filename convention

```
EventType.SENSORID-EVENTID.YYYY-MM-DD-HH-mm-ss-SSS-[M/P]HHmm.event.csv
```

{% method %}
### EventType

1. Used to describe the type of event.

2. CamelStyle, allowed characters: *alphabets* and *digits*.

3. Required.

{% common %}

#### Examples

Smart phone events: `PhoneEMA`, `PhoneCall`, `PhoneSMS`, `Network`, `Battery`, `Bluetooth`, `CPU`, `Memory`, `ExternalStorage`, `InternalStorage`[^1]

{% endmethod %}

[^1] Some of the events have the same name as sensor type, but are used for different purpose, mainly to record abnormal or change of status. Such as low battery, charging, bluetooth connect/disconnect, cpu wakeup/sleep, low storage, and low memory. 