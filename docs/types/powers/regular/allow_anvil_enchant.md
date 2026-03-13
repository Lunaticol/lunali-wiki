# Allow Anvil Enchant

[Power Type](https://lunali-wiki.readthedocs.io/en/latest/types/power_types/)

Allows the holder to apply specific enchantments via an anvil that would normally be unavailable to that item, optionally gated behind an item condition and an enchantment level comparison.

Type ID: `lunali:allow_anvil_enchant`

| Field            | Type                                                                                                                                                            | Default | Description                                                                                                    |
| ---------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------- | -------------------------------------------------------------------------------------------------------------- |
| `enchantments`   | [List](https://origins.readthedocs.io/en/latest/types/data_types/list/) of [Identifiers](https://origins.readthedocs.io/en/latest/types/data_types/identifier/) | `[]`    | The enchantments that this power allows to be applied via anvil.                                               |
| `comparison`     | [Comparison](https://origins.readthedocs.io/en/latest/types/data_types/comparison/)                                                                             | `>=`    | How the current enchantment level on the source item is compared against `compare_to`.                         |
| `compare_to`     | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/)                                                                                   | `0`     | The value the source item's current enchantment level is compared against.                                     |
| `item_condition` | [Item Condition](https://origins.readthedocs.io/en/latest/types/item_condition_types/)                                                                          | `null`  | Condition checked on the input item (the item being enchanted). If this fails, the enchantment is not allowed. |

!!! note

    The `comparison` and `compare_to` fields check the level of the enchantment on the **source** (book or second item), not the base item. This can be used to require a minimum enchantment level before the application is allowed.

## Examples

```json
"enchant_tridents": {
    "type": "lunali:allow_anvil_enchant",
    "enchantments": ["minecraft:sharpness"],
    "item_condition": {
      "type": "origins:ingredient",
      "ingredient": {
        "item": "minecraft:trident"
      }
    }
  }
```

This example allows the holder to apply sharpness to tridents.