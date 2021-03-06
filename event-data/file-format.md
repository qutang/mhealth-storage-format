# File format

Store **formatted** event information \(numerical or categorical\) happens at a time point, such as EMA prompt questions and responses.

## File format

In csv format, separated by `,`, no white space.

```text
HEADER_TIME_STAMP,...
2015-01-05 15:23:00.244,...
```

### Column name

1. `HEADER_TIME_STAMP` is **required** to be the first column.
2. Other column names are in UPPERCASE style, separated by `_`, allowed characters: _alphabets_ and _digits_.
3. Column names should be predefined for a specific event type, including its name and value type.
4. If containing multiple participants, the second column should be `PARTICIPANT_ID`.

#### Examples

For EMA, column names may include `RESPONSE_TIME`, `PROMPT_TIME`, `REPROMPT_INTERVAL`, `PROMPT_METHOD`, `QUESTION`, `ANSWER`, `PROMPT_INDEX`, `SURVEY_INDEX`.

For `PhoneCall`, it may include `DIRECTION`, `NUMBER`, `DURATION`

For `ObjectMove`, it may include `NODE_NAME`, `NODE_ID`

For `NearbyPlace`, it may include `DISTANCE`, `PLACE_NAME`, `CATEGORY_NAME`.

See a predefined [list](file-format.md) of event id and corresponding event types.

### `HEADER_TIME_STAMP` format

1. In local time zone, meaning the time zone where event happens. Time zone can be identified through [filename convention](file-format.md).
2. `YYYY-MM-DD HH:mm:ss.SSS`

### Data format

1. No white space.
2. If value is not available, use `""` empty string instead.

