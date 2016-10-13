# `annotation`

Store **formatted** annotations from a predefined or user defined annotation set.

## File format

In csv format, separated by `,`, no white space.

```
HEADER_TIME_STAMP,START_TIME,STOP_TIME,LABEL_NAME
2015-01-05 15:23:00.244,2015-01-05 15:20:00.244,2015-01-05 15:21:00.244,Walking
```

{% method %}

### Column name
1. `HEADER_TIME_STAMP` is **required** to be the first column, indicating the annotating time. (It's possible user annotates something after it has happened for a while)
2. `START_TIME` is **required** to be the second column, indicating the start time of the annotation.
2. `STOP_TIME` is **required** to be the third column, indicating the stop time of the annotation.
3. 
4. If containing multiple participants, `PARTICIPANT_ID` should be appended as the last column.

{% endmethod %}

### `HEADER_TIME_STAMP` format

1. In local time zone, meaning the time zone where event happens. Time zone can be identified through [filename convention](#).

2. `YYYY-MM-DD HH:mm:ss.SSS`

### Data format

3. No white space.
4. If value is not available, use `""` empty string instead.