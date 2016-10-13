# Important predefined event types

| EventType | EVENTID |
| --- | --- |
| `EMA` | `EMA` |
| `PhoneCall` | `CALL` |
| `PhoneSMS` | `SMS` |
| `Network` | `NETWORK` |
| `Battery` | `CHARGING` |
| `Bluetooth` | `BTSTATUS` |
| `CPU` | `CPUSTATUS` |
| `RAM` | `RAMSTATUS` |
| `ExternalStorage` | `EXSTORAGESTATUS` |
| `InternalStorage` | `INSTORAGESTATUS` |
| `ObjectMove` | `OBJMOVE` |
| `ObjectStatus` | `OBJSTATUS` |
| `NearbyPlace` | `NEARBY` |


## `EMA`

| COLUMN_NAME | Value type | Values |
| --- | --- | --- |
| | |

## `PhoneCall`

| COLUMN_NAME | Value type | Values |
| --- | --- | --- |
| DIRECTION | Categorical | `In`, `Out` |
| NUMBER | String | e.g. `6170000000` |
| DURATION\_IN\_[UNIT][^1] | numeric | e.g. 5 | 

[^1] UNIT could be `HOURS`, `MINUTES`, `SECONDS`

## `PhoneSMS`

| COLUMN_NAME | Value type | Values |
| --- | --- | --- |
| DIRECTION | Categorical | `In`, `Out` |
| NUMBER | String | e.g. `6170000000` |
| LENGTH[^2] | Numerical | e.g. 100 |

[^2] Number of words in the message. Optional.

## `NearbyPlace`

| COLUMN_NAME | Value type | Values |
| --- | --- | --- |
| NAME | String | e.g. CVS |
| DISTANCE\_IN\_[UNIT][^3] | Numerical | e.g. 1.4 |

[^3] UNIT could be `MILES`, `METERS`
