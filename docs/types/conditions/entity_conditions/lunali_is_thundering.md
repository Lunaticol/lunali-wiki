# Prevent Shaders

[Entity Condition Type](https://lunali-wiki.readthedocs.io/en/latest/types/entity_condition_types/)

Checks if it is currently snowing. Only works if you are exposed to the sky.

Type ID: `lunali:is_thundering`

## Examples

```JSON
"thunder": {
    "type": "origins:action_over_time",
    "interval": 5,
    "entity_action": {
      "type": "origins:execute_command",
      "command": "particle dust 1.000 1.000 1.000 2 ~ ~ ~ 0 0 0 1 10 normal"
    },
    "condition": {
      "type": "lunali:is_thundering"
    }
  }
```

This example will cause dust particles to spawn under the player if it is currently thundering.
