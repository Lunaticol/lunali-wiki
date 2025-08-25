# Modify Key Press

[Power Type](https://lunali-wiki.readthedocs.io/en/latest/types/power_types/)

Modifys a key. Can remove or remap them.

Type ID: `lunali:modify_key_press`

| Field     | Type                                                                          | Default | Description                                        |
| --------- | ----------------------------------------------------------------------------- | ------- | -------------------------------------------------- |
| `key`     | [String](https://origins.readthedocs.io/en/latest/types/data_types/string/)   |         | The key you want to target.                        |
| `replace` | [String](https://origins.readthedocs.io/en/latest/types/data_types/string/)   |         | The key you want to replace with the targetted key |
| `remove`  | [Boolean](https://origins.readthedocs.io/en/latest/types/data_types/integer/) |         | Should the targetted key be removed                |

## Examples

```JSON
"confused": {
  "type": "lunali:modify_key_press",
    "key": "key.back",
    "remove": false,
    "replace": "key.forward"
  }
```

This example will cause the forward movement key to become the back movement key.

```JSON
"remove_primary": {
  "type": "lunali:modify_key_press",
    "key": "key.origins.primary_active",
    "remove": true
  }
```

This example will cause the primary key for origins to become unusable.
