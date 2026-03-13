# Screen Shake

[Entity Action](https://lunali-wiki.readthedocs.io/en/latest/types/entity_action_types/)

Causes the users screen to shake.

Type ID: `lunali:screen_shake`

| Field      | Type                                                                          | Default | Description                                |
| ---------- | ----------------------------------------------------------------------------- | ------- | ------------------------------------------ |
| `ticks`    | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/) | 0.0     | How long the shaking should last in ticks. |
| `strength` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/) | 0.0     | The strength of the screen shake.          |

## Examples

```JSON
"shake": {
   "type": "origins:active_self",
    "key": "key.origins.primary_active",
    "cooldown": 0,
    "entity_action": {
      "type": "lunali:screen_shake",
      "ticks": 20,
      "strength": 1
    }
  }
```

This example will shake the users screen for 20 ticks (1 second) at a strength of 1
