# Spawn Point Action

[Entity Action](https://lunali-wiki.readthedocs.io/en/latest/types/entity_action_types/)

Teleports the user back to their spawnpoint.

Type ID: `lunali:return_to_spawnpoint`

| Field          | Type                                                                          | Default                           | Description                                                                          |
| -------------- | ----------------------------------------------------------------------------- | --------------------------------- | ------------------------------------------------------------------------------------ |
| `world_spawn`  | [Boolean](https://origins.readthedocs.io/en/latest/types/data_types/boolean/) | false                             | Wether you return to the worlds spawn point or if you return to your set spawnpoint. |
| `fail_message` | [String](https://origins.readthedocs.io/en/latest/types/data_types/string/)   | "block.minecraft.spawn.not_valid" | Allows inputting a custom message should the teleport back to your spawn fail.       |

## Examples

```JSON
"spawn": {
  "type": "origins:active_self",
    "key": "key.origins.secondary_active",
    "cooldown": 0,
    "entity_action": {
      "type": "lunali:return_to_spawnpoint",
      "world_spawn": false
    }
  }
```

This example will teleport the user to their spawn point.
