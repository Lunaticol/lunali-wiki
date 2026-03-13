# Radial Menu Action

Used by [Radial Menu](https://lunali-wiki.readthedocs.io/en/latest/types/power_types/radial_menu/) power to define the behaviour and appearance of each directional slot.

| Field        | Type                                                                                 | Default | Description                                                                                                      |
| ------------ | ------------------------------------------------------------------------------------ | ------- | ---------------------------------------------------------------------------------------------------------------- |
| `index`      | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/)        | `0`     | The display index of this slot, used for ordering icons in the menu UI.                                          |
| `action`     | [Entity Action](https://origins.readthedocs.io/en/latest/types/entity_action_types/) | `null`  | The entity action to execute on the holder when this slot is confirmed. If `null`, nothing happens.              |
| `swap_index` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/)        | `-1`    | If set to a value other than `-1`, selects a different menu slot index to swap to when this action is triggered. |
| `icon_scale` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/)            | `1.0`   | The scale of the icon rendered in this slot. Values above `1.0` make the icon larger, below `1.0` smaller.       |

!!! note
`swap_index` can be used to switch the active selection to another slot after an action fires, useful for chained or toggle-style menus.

## Examples

```json
{
  "index": 0,
  "icon_scale": 1.2,
  "action": {
    "type": "origins:heal",
    "amount": 4
  }
}
```

This example defines a radial slot that heals the holder for 2 hearts when confirmed, with its icon rendered at 1.2x scale.
