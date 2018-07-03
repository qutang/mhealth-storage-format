---
description: >-
  A quick review of the supported file types in mhealth-storage compatible
  dataset
---

# Quick view of supported file types

File types are identified in the suffix before file extension, separated by symbol \`.\`. Current format reserves identifiers for six file types: sensor, event, annotation, feature, class and log. You may extend with your own file type identifier.

* xxx.xxxxxx.2016-01-01-08-00-00-000-\[M/P\]HHmm.**sensor**.csv
* xxx.xxxxxx.2016-01-01-09-00-00-110-\[M/P\]HHmm.**event**.csv
* xxx.xxxxxx.2016-01-01-09-00-00-110-\[M/P\]HHmm.**annotation**.csv
* xxx.xxxxxx.2016-01-01-09-00-00-110-\[M/P\]HHmm.**feature**.csv
* xxx.xxxxxx.2016-01-01-09-00-00-110-\[M/P\]HHmm.**class**.csv
* xxx.xxxxxx.2016-01-01-09-00-00-110-\[M/P\]HHmm.**log**.csv

## File types to store raw information

### sensor data

> Store raw sensor data in high or low sampling frequency.
>
> User can add their own `sensor type` to define new `senosr` data file format.

#### Filename convention

```text
DeviceType-DataType-VersionCode.DEVICEID-SENSORTYPE.YYYY-MM-DD-HH-mm-ss-SSS-[M/P]HHmm.sensor.csv(.gz)
```

```text
ActigraphGT9X-AccelerometerCalibrated-0x0x0.TASXXXXXXX-ACCEL.2018-01-01-11-00-00-000-P0000.sensor.csv
```

#### File format

```text
HEADER_TIME_STAMP,X,Y,Z,[GROUP_1],[GROUP_2],...
2015-01-05 15:23:00.244,2.456,3.123,4.321,2.331,P1,TASXXXX,...
2015-01-05 15:23:00.244,2.456,3.123,4.321,2.331,P2,TASXXXX,...
2015-01-05 15:23:00.244,2.456,3.123,4.321,2.331,P3,TASXXXX,...
```

### event data

> Store **formatted** event information \(numerical or categorical\) happens at a time point, such as EMA prompt questions and responses.

#### Filename Convention

```text
DeviceType-EventType-VersionCode.DEVICEID-EVENTTYPE.YYYY-MM-DD-HH-mm-ss-SSS-[M/P]HHmm.event.csv
```

```text
Nexus5-EMAResponses-0x0x0.0123456789-EMARESPONSES.2018-01-01-11-00-00-000-P0000.event.csv
```

#### File format

{% code-tabs %}
{% code-tabs-item title="PhoneCall" %}
```text
HEADER_TIME_STAMP,DIRECTION,NUMBER,DURATION_IN_SECONDS
2015-01-05 15:23:00.244,Out,617-xxx-xxxx,300
```
{% endcode-tabs-item %}
{% endcode-tabs %}

{% code-tabs %}
{% code-tabs-item title="EMAResponses" %}
```text
HEADER_TIME_STAMP,PROMPT_TIME,RESPONSE_TIME,QUESTION,ANSWER
2015-01-05 15:23:00.244,2015-01-05 15:22:00.244,2015-01-05 15:22:03.244,"Where are you?","Home"
```
{% endcode-tabs-item %}
{% endcode-tabs %}

### annotation data

> Store annotation information by user or by annotator. Annotation set may be from user definition or predefined annotation set.

#### Filename Convention

```text
AnnotationSet.ANNOTATIONSETID-ANNOTATORID-VERSIONCODE.YYYY-MM-DD-HH-mm-ss-SSS-[M/P]HHmm.annotation.csv
```

#### File format

```text
HEADER_TIME_STAMP,START_TIME,STOP_TIME,LABEL_NAME
2015-01-05 15:23:00.244,2015-01-05 15:20:00.244,2015-01-05 15:21:00.244,Walking
```

## File types for data analysis

### `feature` file

> Store numerical or categorical feature data derived from `sensor` or `event` files.

#### Filename Convention

```text
FeatureType.FEATUREID-VERSIONCODE.YYYY-MM-DD-HH-mm-ss-SSS-[M/P]HHmm.feature.csv[.gz]
```

#### File format

```text
HEADER_TIME_STAMP,START_TIME,STOP_TIME,[FEATURE_NAME],...
2015-01-05 15:23:00.244,2015-01-05 15:20:00.244,2015-01-05 15:21:00.244,1.44,...
```

