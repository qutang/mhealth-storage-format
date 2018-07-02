# Event types

## `EMA`

| COLUMN\_NAME | Value type | Values |
| --- | --- | --- |
|  |  |  |

## `PhoneCall`

| COLUMN\_NAME | Value type | Values | Required |
| --- | --- | --- | --- |
| DIRECTION | Categorical | `In`, `Out` | Yes |
| NUMBER | Encrypted String | e.g. `xxxxxxxxxx` | Yes |
| DURATION\_IN\_\[UNIT\] | numeric | e.g. 5 | Yes |

 UNIT could be `HOURS`, `MINUTES`, `SECONDS`

## `PhoneSMS`

| COLUMN\_NAME | Value type | Values | Required |
| --- | --- | --- | --- |
| DIRECTION | Categorical | `In`, `Out` | Yes |
| NUMBER | Encrypted String | e.g. `xxxxxxxxxxxxxx` | Yes |
| LENGTH | Numerical | e.g. 100 | No |

 Number of words in the message.

## `NearbyPlace`

| COLUMN\_NAME | Value type | Values | Required |
| --- | --- | --- | --- |
| NAME | String | e.g. CVS | Yes |
| DISTANCE\_IN\_\[UNIT\] | Numerical | e.g. 1.4 | No |

 UNIT could be `MILES`, `METERS`.

