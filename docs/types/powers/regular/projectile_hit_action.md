# Projectile Hit Action

[Power Type](https://lunali-wiki.readthedocs.io/en/latest/types/power_types/)

Executes bi-entity actions when a projectile owned by the power holder hits a living entity. Supports separate actions on the projectile-target pair and the owner-target pair, each with optional conditions.

Type ID: `lunali:projectile_hit_action`

| Field                      | Type                                                                                            | Default | Description                                                                                                                   |
| -------------------------- | ----------------------------------------------------------------------------------------------- | ------- | ----------------------------------------------------------------------------------------------------------------------------- |
| `cooldown`                 | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/)                   | `1`     | Number of ticks before the same projectile owner can trigger the action again. Minimum value of `1`.                          |
| `hud_render`               | [Hud Render](https://origins.readthedocs.io/en/latest/types/data_types/hud_render/)             | `none`  | Determines how the cooldown is displayed on the HUD.                                                                          |
| `bientity_action`          | [Bi-Entity Action](https://origins.readthedocs.io/en/latest/types/bientity_action_types/)       | `null`  | Action executed with the **projectile** as the actor and the **hit entity** as the target.                                    |
| `bientity_condition`       | [Bi-Entity Condition](https://origins.readthedocs.io/en/latest/types/bientity_condition_types/) | `null`  | Condition that must pass on the projectile-target pair for `bientity_action` to execute. If omitted, the action always runs.  |
| `owner_bientity_action`    | [Bi-Entity Action](https://origins.readthedocs.io/en/latest/types/bientity_action_types/)       | `null`  | Action executed with the **owner** as the actor and the **hit entity** as the target.                                         |
| `owner_bientity_condition` | [Bi-Entity Condition](https://origins.readthedocs.io/en/latest/types/bientity_condition_types/) | `null`  | Condition that must pass on the owner-target pair for `owner_bientity_action` to execute. If omitted, the action always runs. |

## Examples

```json
 "explosive_trident": {
    "type": "lunali:action_on_projectile_hit",
    "cooldown": 100,
    "hud_render": {
      "should_render": true,
      "sprite_location": "origins:textures/gui/community/huang/resource_bar_01.png",
      "bar_index": 2
    },
    "bientity_action": {
      "type": "origins:actor_action",
      "action": {
        "type": "origins:and",
        "actions": [
          {
            "type": "origins:explode",
            "create_fire": false,
            "damage_self": false,
            "destruction_type": "KEEP",
            "power": 3
          },
          {
            "type": "origins:execute_command",
            "command": "particle minecraft:explosion ~ ~1 ~ 1 1 1 1 10"
          },
          {
            "type": "origins:play_sound",
            "sound": "minecraft:entity.generic.explode",
            "category": "master",
            "pitch": 1,
            "volume": 1
          }
        ]
      }
    },
    "owner_bientity_action": {
      "type": "origins:actor_action",
      "action": {
        "type": "origins:exhaust",
        "amount": 25
      }
    },
    "bientity_condition": {
      "type": "origins:actor_condition",
      "condition": {
        "type": "origins:entity_type",
        "entity_type": "minecraft:trident"
      }
    }
  }
```

This example causes the owners tridents to explode upon hitting an entity.
