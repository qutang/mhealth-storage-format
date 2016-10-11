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

Smart phone events: `PhoneEMA`, `PhoneCall`, `PhoneSMS`, `Network`, `Battery`[^1], `Bluetooth`, `CPU`, `PhoneRAM`, `PhoneExternalStorage`, `PhoneInternalStorage`

{% endmethod %}

[^1] This battery event is used to record charging status change, which is different from battery sensor data used to record battery level change at a regular sampling rate.