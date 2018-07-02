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

### `sensor` file

> Store raw numerical sensor data in high or low sampling frequency.
>
> User can add their own `sensor type` to define new `senosr` data file format.

#### Filename

```text
SensorType-DataType.SENSORID-DATATYPE-VERSIONCODE.YYYY-MM-DD-HH-mm-ss-SSS-[M/P]HHmm.sensor.csv(.gz)
```

#### File format

```text
HEADER_TIME_STAMP,[PARTICIPANT_ID],COL1,COL2,COL3,...
2015-01-05 15:23:00.244,[P1],2.456,3.123,4.321,2.331,...
```

### `event` file

> Store **formatted** event information \(numerical or categorical\) happens at a time point, such as EMA prompt questions and responses.

#### Filename Convention

```text
SensorType-EventType.SENSORID-EVENTTYPE-VERSIONCODE.YYYY-MM-DD-HH-mm-ss-SSS-[M/P]HHmm.event.csv
```

#### File format

```text
HEADER_TIME_STAMP,DIRECTION,NUMBER,DURATION_IN_SECONDS
2015-01-05 15:23:00.244,Out,617-xxx-xxxx,300
```

### `annotation` file

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

