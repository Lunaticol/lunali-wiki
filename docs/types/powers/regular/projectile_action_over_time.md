# Projectile Action Over Time

[Power Type](https://lunali-wiki.readthedocs.io/en/latest/types/power_types/)

Repeatedly executes a bi-entity action between the holder and their active projectiles at a set interval.

Type ID: `lunali:projectile_action_over_time`

| Field                | Type                                                                                            | Default | Description                                                                                                                   |
| -------------------- | ----------------------------------------------------------------------------------------------- | ------- | ----------------------------------------------------------------------------------------------------------------------------- |
| `interval`           | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/)                   | `20`    | How many ticks between each execution of `bientity_action`. Minimum value of `1`.                                             |
| `bientity_action`    | [Bi-Entity Action](https://origins.readthedocs.io/en/latest/types/bientity_action_types/)       | `null`  | Action executed repeatedly on the owner-projectile pair at every interval while the power is active.                          |
| `rising_action`      | [Bi-Entity Action](https://origins.readthedocs.io/en/latest/types/bientity_action_types/)       | `null`  | Action executed once the first time a projectile is ticked, when its age matches its offset. Acts as a "on first tick" event. |
| `falling_action`     | [Bi-Entity Action](https://origins.readthedocs.io/en/latest/types/bientity_action_types/)       | `null`  | Action executed instead of `bientity_action` when the power is inactive but a tracked projectile still exists.                |
| `bientity_condition` | [Bi-Entity Condition](https://origins.readthedocs.io/en/latest/types/bientity_condition_types/) | `null`  | Condition checked on the owner-projectile pair each tick. The projectile is only tracked and acted on if this passes.         |

!!! note

Only projectiles within 64 blocks of the holder are tracked. Projectiles are automatically untracked when removed from the world. This is to reduce lag. Projectiles will also stop ticking when the holder leaves the game.

## Examples

```json
{
  "smoke": {
    "type": "lunali:projectile_action_over_time",
    "interval": 5,
    "bientity_action": {
      "type": "origins:target_action",
      "action": {
        "type": "origins:execute_command",
        "command": "particle minecraft:smoke ~ ~ ~ 0.1 0.1 0.1 .1 20 force"
      }
    }
  }
}
```

This example spawns smoke particles on projectiles shot by the holder.
