# Sleep Action

[Power Type](https://lunali-wiki.readthedocs.io/en/latest/types/power_types/)

Causes the player to sleep, skipping the night or day if specified.

Type ID: `lunali:sleep`

| Field                | Type                                                                          | Default                    | Description                                       |
| -------------------- | ----------------------------------------------------------------------------- | -------------------------- | ------------------------------------------------- |
| `sleep_during_day`   | [String](https://origins.readthedocs.io/en/latest/types/data_types/boolean/)  | false                      | If the player is allowed to sleep during the day. |
| `sleep_during_night` | [Boolean](https://origins.readthedocs.io/en/latest/types/data_types/boolean/) | true                       | If the player is allowed to sleep at night.       |
| `fail_message`       | [Boolean](https://origins.readthedocs.io/en/latest/types/data_types/string/)  | You can't sleep right now. | The fail message to send to the player.           |
| `set_spawnpoint`     | [Boolean](https://origins.readthedocs.io/en/latest/types/data_types/boolean/) | true                       | If sleeping sets your spawnpoint.                 |

!!! note

You should probably use [`origins:prevent_sleep`](https://origins.readthedocs.io/en/latest/types/power_types/prevent_sleep/) if you want to prevent the player from sleeping with beds. Do also note that beds do not work for daytime, even if `sleep_during_day` is true.

## Examples

```JSON
"sleep": {
   "type": "origins:active_self",
    "key": "key.origins.primary_active",
    "cooldown": 0,
    "entity_action": {
      "type": "lunali:sleep",
      "sleep_during_day": true,
      "sleep_during_night": false,
      "fail_message": "You are not tired.",
      "set_spawnpoint": true
    }
  }
```

This example will cause the player to fall asleep without a bed during the daytime. If the player attempts to sleep at night the message "You are not tired." will appear. also sets the player spawnpoint.
