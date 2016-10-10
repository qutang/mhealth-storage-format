# `sensor`

Used to store raw numerical sensor data in high or low sampling frequency.

## File format

In csv format, separated by `,`, no white space. The file may be gzipped.

```
HEADER_TIME_STAMP,COL1,COL2,COL3,...
2015-01-05 15:23:00.244,2.456,3.123,4.321,2.331,...
```

{% method %}

### Column name

1. `HEADER_TIME_STAMP` is **required** to be the first column.
2. Other column names are in UPPERCASE style, separated by `_`, allowed characters: *alphabets* and *digits*.

#### Examples

For inertial sensors, column names could be `X_IN_G`, `Y_IN_G`, `Z_IN_G`, where `IN_XXX` is used to specify the unit of the measurement.

{% endmethod %}