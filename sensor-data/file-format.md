# File format

Used to store raw numerical sensor data in high or low sampling frequency.

## File format

In csv format, separated by `,`, no white space. The file may be gzipped.

```text
HEADER_TIME_STAMP,[PARTICIPANT_ID],COL1,COL2,COL3,...
2015-01-05 15:23:00.244,[P1],2.456,3.123,4.321,2.331,...
```

### Column name

1. `HEADER_TIME_STAMP` is **required** to be the first column.
2. Other column names are in UPPERCASE style, separated by `_`, allowed characters: _alphabets_ and _digits_.
3. Although column name is completely customized, it is recommended to use style `[MEASUREMENT]_IN_[UNIT]`, where `MEASUREMENT` is the name of measurement, and `UNIT` is the unit of measurement, which is optional.
4. If containing multiple participants, the second column should be `PARTICIPANT_ID`.

#### Examples

For inertial sensors, column names could be `X_IN_G`, `Y_IN_G`, `Z_IN_G`, where `IN_XXX` is used to specify the unit of the measurement, but it is optional.

For heart rate monitor, column names could be `HR_IN_BPM`.

For GPS monitor, column names could be `LATITUDE_IN_DEGREE` or `LONGITUIDE_IN_RADIUS`.

See a complete [list](file-format.md) of recommended column names for different data types.

### `HEADER_TIME_STAMP` format

1. In local time zone, meaning the time zone where data was collected. Time zone can be identified through [filename convention](file-format.md).
2. `YYYY-MM-DD HH:mm:ss.SSS`

### Data format

1. **Only numerical values are allowed**.
2. To control file size, it is recommended to not use higher float value precision than necessary.
3. No white space.
4. If value is not available, use `""` empty string instead.

