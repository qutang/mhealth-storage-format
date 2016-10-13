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
| DURATION\_IN\_[HOURS/MINUTES/SECONDS] | numeric | e.g. 5 | 

## `PhoneSMS`

| COLUMN_NAME | Value type | Values |
| --- | --- | --- |
| DIRECTION | Categorical | `In`, `Out` |
| NUMBER | String | e.g. `6170000000` |
| LENGTH[^1] | Numerical | e.g. 100 |

[^1] Number of words

## `NearbyPlace`

| COLUMN_NAME | Value type |
| --- | --- |
| | |

