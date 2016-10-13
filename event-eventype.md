# Important predefined event types

## `EMA`

| COLUMN_NAME | Value type | Values |
| --- | --- | --- |
| | |

## `PhoneCall`

| COLUMN_NAME | Value type | Values | Required |
| --- | --- | --- | --- |
| DIRECTION | Categorical | `In`, `Out` | Yes |
| NUMBER | Encrypted String | e.g. `xxxxxxxxxx` | Yes |
| DURATION\_IN\_[UNIT][^1] | numeric | e.g. 5 | Yes |

[^1] UNIT could be `HOURS`, `MINUTES`, `SECONDS`

## `PhoneSMS`

| COLUMN_NAME | Value type | Values | Required |
| --- | --- | --- | --- |
| DIRECTION | Categorical | `In`, `Out` | Yes |
| NUMBER | Encrypted String | e.g. `xxxxxxxxxxxxxx` | Yes |
| LENGTH[^2] | Numerical | e.g. 100 | No |

[^2] Number of words in the message.

## `NearbyPlace`

| COLUMN_NAME | Value type | Values | Required |
| --- | --- | --- | --- |
| NAME | String | e.g. CVS | Yes |
| DISTANCE\_IN\_[UNIT][^3] | Numerical | e.g. 1.4 | No |

[^3] UNIT could be `MILES`, `METERS`.
