# Riptide Action

[Entity Action](https://lunali-wiki.readthedocs.io/en/latest/types/entity_action_types/)

Causes the user to riptide regardless of rain. Also puts the user into riptide animation with a riptide hitbox.

Type ID: `lunali:riptide`

| Field      | Type                                                                          | Default | Description                                                 |
| ---------- | ----------------------------------------------------------------------------- | ------- | ----------------------------------------------------------- |
| `strength` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/) | 1       | How strong the riptide should be. Works like `add_velocity` |

## Examples

```JSON
"riptide": {
    "type": "origins:active_self",
    "key": "key.origins.quaternary_active",
    "entity_action": {
      "type": "lunali:riptide",
      "strength": 1
    }
  }
```

This example will cause the user to riptide with a strength of 1.
