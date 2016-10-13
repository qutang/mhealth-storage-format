# `annotation`

Store **formatted** annotations from a predefined or user defined annotation set.

## File format

In csv format, separated by `,`, no white space.

```
HEADER_TIME_STAMP,START_TIME,STOP_TIME,LABEL_NAME
2015-01-05 15:23:00.244,2015-01-05 15:20:00.244,2015-01-05 15:21:00.244,Walking
```

{% method %}

### Columns

| COLUMN_NAME | POSITION | Value type | Values | Required |
| --- | --- | --- | --- | --- |
| HEADER_TIME_STAMP | 1 | String | e.g. `2015-01-05 15:23:00.244` | Yes |
| START_TIME | 2| String | e.g. `2015-01-05 15:23:00.244` | Yes |
| STOP_TIME | 3 | String | e.g. `2015-01-05 15:23:00.244` | Yes |
| LABEL_NAME[^1] | 4 | String | e.g. Walking | Yes |

[^1] Should be locally unique among the annotation set
5. Optional columns after `LABEL_NAME`
     * `CONFIDENCE`, numerical value indicating the 

**Note that if containing multiple participants, `PARTICIPANT_ID` should be appended as the last column.**

{% endmethod %}

### `HEADER_TIME_STAMP`, `START_TIME`, `STOP_TIME` format

1. In local time zone, meaning the time zone where event happens. Time zone can be identified through [filename convention](#).

2. `YYYY-MM-DD HH:mm:ss.SSS`

### Other columns' format

3. No white space.
4. If value is not available, use `""` empty string instead.