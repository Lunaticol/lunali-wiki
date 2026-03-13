# Mobs Ignore
[Power Type](https://lunali-wiki.readthedocs.io/en/latest/types/power_types/)

Causes mobs that pass the given condition to ignore the power holder, preventing them from targeting or attacking them.

Type ID: `lunali:mobs_ignore`

| Field | Type | Default | Description |
| --- | --- | --- | --- |
| `mob_condition` | [Entity Condition](https://origins.readthedocs.io/en/latest/types/entity_condition_types/) | `null` | Condition checked on the mob. Only mobs that pass this condition will ignore the holder. If `null`, no mobs will be ignored. |

!!! note

    A `mob_condition` must be provided for this power to have any effect. Without it, no mobs will be affected.

## Examples
```json
{
  "type": "lunali:mobs_ignore",
  "mob_condition": {
    "type": "origins:entity_type",
    "entity_type": "minecraft:zombie"
  }
}
```
This example causes all zombies to ignore the holder completely.