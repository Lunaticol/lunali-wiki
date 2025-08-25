# Lagged Hitbox

[Power Type](https://lunali-wiki.readthedocs.io/en/latest/types/power_types/)

Causes the players hitbox to lag behind them, leaving a trail of hitboxes. If these hitboxes are hit they will apply damage to its owner.

Type ID: `lunali:lag_hitbox`

| Field      | Type                                                                          | Default | Description                                       |
| ---------- | ----------------------------------------------------------------------------- | ------- | ------------------------------------------------- |
| `interval` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/) |         | how often hitboxes should spawn.                  |
| `lifetime` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/) |         | How long hitboxes should last until they despawn. |

## Examples

```JSON
"lagged_hitbox": {
   "type": "lunali:lag_hitbox",
    "lifetime": 100,
    "interval": 1
  }
```

This example will cause a hitbox to spawn every tick with a lifetime of 100 ticks (5 seconds)
