# Offset Action

[Power Type](https://lunali-wiki.readthedocs.io/en/latest/types/power_types/)

Causes entity actions to become offset, origin point being the player.

Type ID: `lunali:offset_action`

| Field           | Type                                                                                 | Default | Description                         |
| --------------- | ------------------------------------------------------------------------------------ | ------- | ----------------------------------- |
| `x`             | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/)            | 0.0     | How far it should be offset from x. |
| `y`             | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/)            | 0.0     | How far it should be offset from y. |
| `z`             | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/)            | 0.0     | How far it should be offset from z. |
| `offset_action` | [Entity Action](https://origins.readthedocs.io/en/latest/types/entity_action_types/) |         | The action to offset.               |

## Examples

```JSON
"offset": {
   "type": "origins:active_self",
    "key": "key.origins.primary_active",
    "cooldown": 0,
    "entity_action": {
      "type": "lunali:offset_action",
      "x": 0,
      "y": 5,
      "z": 0,
      "offset_action": {
        "type": "origins:fire_projectile",
        "count": 1,
        "entity_type": "minecraft:arrow"
      }
    }
  }
```

This example will cause an entity to fire an arrow 5 blocks above them.
