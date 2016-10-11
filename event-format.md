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

For EMA, column names may include `RESPONSE_TIME`, `PROMPT_TIME`, `REPROMPT_INTERVAL`, `PROMPT_METHOD`, `QUESTION`, `ANSWER`

{% endmethod %}

### `HEADER_TIME_STAMP` format

1. In local time zone, meaning the time zone where event happens. Time zone can be identified through [filename convention](#).

2. `YYYY-MM-DD HH:mm:ss.SSS`

### Data format

3. No white space.

4. If value is not available, use `""` empty string instead.




