# Filename convention

Store **formatted** event information \(numerical or categorical\) happens at a time point, such as EMA prompt questions and responses.

## Filename convention

```text
SensorType-EventType.SENSORID-EVENTTYPE-VERSIONCODE.YYYY-MM-DD-HH-mm-ss-SSS-[M/P]HHmm.event.csv
```

Event files are divided into **daily** files, as hourly files will be too sparse to be insightful.

### SensorType

1. Same as what was described in `sensor`.
2. By default, most events are collected through the phone, so the value would be `AndroidPhone` or `iPhone`.
3. In case some of the events are collected by paper or questionnare, the value could be `Paper`, `Questionnare`, `ShortMessage`, `PhoneCall` or `Interview`.

### EventType

1. Used to describe the type of event, should be locally unique.
2. CamelStyle, allowed characters: _alphabets_ and _digits_.
3. Required.
4. Locally unique. To avoid confliction with `DataType`, add suffix `Event` if necessary.

#### Examples

Smart phone events: `EMA`, `PhoneCall`, `PhoneSMS`, `NetworkEvent`, `BatteryEvent`, `BluetoothEvent`, `CPUEvent`, `RAMEvent`, `ExternalStorageEvent`, `InternalStorageEvent`.

Indoor events: `ObjectMove`, `ObjectStatus`.

Outdoor events: `NearbyPlace`.

See a predefined [list](filename-convention.md) of event id and corresponding event types.

### EVENTTYPE

1. Same as EventType but in uppercase.
2. UPPERCASE style, allowed characters: _alphabets_ and _digits_.

### Timestamp

1. Timestamp has the same convention as that of sensor data. The time represents the first row of event.
2. Because it's a daily file, normally there will only be one file for a day.
3. In case time zone is changed during the day, there will be multiple files for one day.

#### Examples

If time zone changes from M0500 to M0300 at 10am on a day, and an event happens at 12pm in M0500 time zone, then the new file would have timestamp `YYYY-MM-DD-14-00-00-000-M0300` in the filename.

