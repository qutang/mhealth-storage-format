# `feature`
Store numerical or categorical feature data derived from `sensor` or `event` files.

## File format
In csv format, separated by `,`, no white space.

```
HEADER_TIME_STAMP,START_TIME,STOP_TIME,[FEATURE_NAME],...
2015-01-05 15:23:00.244,2015-01-05 15:20:00.244,2015-01-05 15:21:00.244,1.44,...
```
### Columns

| COLUMN_NAME | POSITION | Value type | Values | Required |
| --- | --- | --- | --- | --- |
| HEADER_TIME_STAMP | 1 | String | e.g. `2015-01-05 15:23:00.244` | Yes |
| START_TIME | 2| String | e.g. `2015-01-05 15:23:00.244` | Yes |
| STOP_TIME | 3 | String | e.g. `2015-01-05 15:23:00.244` | Yes |
| [FEATURE_NAME][^1] | 4-? | String | e.g. Walking | Yes |
| CONFIDENCE[^2] | 5 | 0-1 | e.g. 0.5 | No |
| PARTICIPANT_ID | last | String | e.g. SPADES_1 | No |

[^1] actual feature name, there may be multiple ones for each axis.


[^2] 0 means random guess, 1 means for sure.



### `HEADER_TIME_STAMP`, `START_TIME`, `STOP_TIME` format



1. In local time zone, meaning the time zone where event happens. Time zone can be identified through [filename convention](#).



2. `YYYY-MM-DD HH:mm:ss.SSS`



### Other columns' format



3. No white space.

4. If value is not available, use `""` empty string instead.
