# Prevent Shaders

Misc Condition Type

Checks the current date.

Type ID: `lunali:check_date`

| Field      | Type                                                                        | Default | Description                                                          |
| ---------- | --------------------------------------------------------------------------- | ------- | -------------------------------------------------------------------- |
| `timezone` | [String](https://origins.readthedocs.io/en/latest/types/data_types/String/) | null    | Sets the timezone. If not set, it uses the servers timezone.         |
| `weekday`  | [String](https://origins.readthedocs.io/en/latest/types/data_types/String/) | \*      | The weekday. Accepts MON, TUE, ect, 1 - 7, and MONDAY, TUESDAY, ect. |
| `second`   | [String](https://origins.readthedocs.io/en/latest/types/data_types/String/) | \*      | The second                                                           |
| `minute`   | [String](https://origins.readthedocs.io/en/latest/types/data_types/String/) | \*      | The minute                                                           |
| `hour`     | [String](https://origins.readthedocs.io/en/latest/types/data_types/String/) | \*      | The hour                                                             |
| `day`      | [String](https://origins.readthedocs.io/en/latest/types/data_types/String/) | \*      | The day                                                              |
| `month`    | [String](https://origins.readthedocs.io/en/latest/types/data_types/String/) | \*      | The month                                                            |
| `year`     | [String](https://origins.readthedocs.io/en/latest/types/data_types/String/) | \*      | The year                                                             |

!!! note

    "*" is used as a wildcard, meaning for example "year": "*" will be true no matter what year it is, very useful for repeating events, such as april fools.

## Examples

```JSON
"merry_christmas": {
    "type": "origins:action_over_time",
    "interval": 5,
    "entity_action": {
      "type": "origins:execute_command",
      "command": "give @s diamond"
    },
    "condition": {
      "type": "lunali:check_date",
      "timezone": "EST",
      "second": "*",
      "minute": "*",
      "hour": "*",
      "day": "25",
      "month": "12",
      "year": "*"
    }
  }
```

This example will give the player a diamond every 5 ticks on christmas day in when EST hits December 25th on any year.

Here is a list of timezones that can be inputted. This list CANNOT be modified.

EST - -05:00
HST - -10:00
MST - -07:00
ACT - Australia/Darwin
AET - Australia/Sydney
AGT - America/Argentina/Buenos Aires
ART - Africa/Cairo
AST - America/Anchorage
BET - America/Sao Paulo
BST - Asia/Dhaka
CAT - Africa/Harare
CNT - America/St_Johns
CST - America/Chicago
CTT - Asia/Shanghai
EAT - Africa/Addis Ababa
ECT - Europe/Paris
IET - America/Indiana/Indianapolis
IST - Asia/Kolkata
JST - Asia/Tokyo
MIT - Pacific/Apia
NET - Asia/Yerevan
NST - Pacific/Auckland
PLT - Asia/Karachi
PNT - America/Phoenix
PRT - America/Puerto_Rico
PST - America/Los Angeles
SST - Pacific/Guadalcanal
VST - Asia/Ho Chi Minh
