# File format

Store **formatted** annotations from a predefined or user defined annotation set.

## File format

In csv format, separated by `,`, no white space.

```text
HEADER_TIME_STAMP,START_TIME,STOP_TIME,LABEL_NAME
2015-01-05 15:23:00.244,2015-01-05 15:20:00.244,2015-01-05 15:21:00.244,Walking
```

### Columns

| COLUMN\_NAME | POSITION | Value type | Values | Required |
| :--- | :--- | :--- | :--- | :--- |
| HEADER\_TIME\_STAMP | 1 | String | e.g. `2015-01-05 15:23:00.244` | Yes |
| START\_TIME | 2 | String | e.g. `2015-01-05 15:23:00.244` | Yes |
| STOP\_TIME | 3 | String | e.g. `2015-01-05 15:23:00.244` | Yes |
| LABEL\_NAME | 4 | String | e.g. Walking | Yes |
| CONFIDENCE | 5 | 0-1 | e.g. 0.5 | No |
| PARTICIPANT\_ID | last | String | e.g. SPADES\_1 | No |

 Should be locally unique among the annotation set.

 0 means random guess, 1 means for sure.

### `HEADER_TIME_STAMP`, `START_TIME`, `STOP_TIME` format

1. In local time zone, meaning the time zone where event happens. Time zone can be identified through [filename convention](file-format.md).
2. `YYYY-MM-DD HH:mm:ss.SSS`

### Other columns' format

1. No white space.
2. If value is not available, use `""` empty string instead.

