# `event`

Store **formatted** event information (numerical or categorical) happens at a time point, such as EMA prompt questions and responses.

## File format

In csv format, separated by `,`, no white space.

```
HEADER_TIME_STAMP,...
2015-01-05 15:23:00.244,...
```

{% method %}

### Column name

1. `HEADER_TIME_STAMP` is **required** to be the first column.

2. Other column names are in UPPERCASE style, separated by `_`, allowed characters: *alphabets* and *digits*.

3. Column names should be predefined for a specific event type, including its name and value type.

4. If containing multiple participants, the second column should be `PARTICIPANT_ID`.

{% common %}

#### Examples

For inertial sensors, column names could be `X_IN_G`, `Y_IN_G`, `Z_IN_G`, where `IN_XXX` is used to specify the unit of the measurement, but it is optional.

For heart rate monitor, column names could be `HR_IN_BPM`.

For GPS monitor, column names could be `LATITUDE_IN_DEGREE` or `LONGITUIDE_IN_RADIUS`.

See a complete [list](#) of recommended column names for different data types.

{% endmethod %}

### `HEADER_TIME_STAMP` format
1. In local time zone, meaning the time zone where data was collected. Time zone can be identified through [filename convention](#).

2. `YYYY-MM-DD HH:mm:ss.SSS`

### Data format

3. No white space.

4. If value is not available, use `""` empty string instead.




