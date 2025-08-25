# Lagged Hitbox

[Power Type](https://lunali-wiki.readthedocs.io/en/latest/types/power_types/)

Causes entitys to glow like glow squids.

Type ID: `lunali:glowing`

| Field  | Type                                                                          | Default | Description                    |
| ------ | ----------------------------------------------------------------------------- | ------- | ------------------------------ |
| `glow` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/) |         | How brightly the entity glows. |

!!! note

Dynamic lighting will come in the future.

## Examples

```JSON
"glowing": {
   "type": "lunali:glowing",
   "glow": 15
  }
```

This example will cause the entity to glow at light level 15.
