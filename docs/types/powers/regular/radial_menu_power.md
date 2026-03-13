# Radial Menu

[Power Type](https://lunali-wiki.readthedocs.io/en/latest/types/power_types/)

Gives the entity a radial menu with up to 9 directional slots, each capable of executing a custom action when selected.

Type ID: `lunali:radial_menu`

| Field               | Type                                                                                         | Default    | Description                                                                                                                                                   |
| ------------------- | -------------------------------------------------------------------------------------------- | ---------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `key`               | [Key Binding](https://origins.readthedocs.io/en/latest/types/data_types/key/)                |            | The key that opens and closes the radial menu.                                                                                                                |
| `sprite_location`   | [Identifier](https://origins.readthedocs.io/en/latest/types/data_types/identifier/)          | `null`     | Optional sprite to display in the center of the radial menu. Its recommended to set a sprite however.                                                         |
| `swap_time`         | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/)                | `20`       | How many ticks the transition animation takes when switching between directions.                                                                              |
| `default_direction` | [String](https://origins.readthedocs.io/en/latest/types/data_types/string/)                  | `"center"` | The direction selected when the menu first opens. Accepted values: `center`, `up`, `down`, `left`, `right`, `up_left`, `up_right`, `down_left`, `down_right`. |
| `center_action`     | [Radial Menu Action](https://lunali-wiki.readthedocs.io/en/latest/types/radial_menu_action/) | `null`     | Action executed when the center slot is selected and confirmed.                                                                                               |
| `up_action`         | [Radial Menu Action](https://lunali-wiki.readthedocs.io/en/latest/types/radial_menu_action/) | `null`     | Action executed when the up slot is selected and confirmed.                                                                                                   |
| `down_action`       | [Radial Menu Action](https://lunali-wiki.readthedocs.io/en/latest/types/radial_menu_action/) | `null`     | Action executed when the down slot is selected and confirmed.                                                                                                 |
| `left_action`       | [Radial Menu Action](https://lunali-wiki.readthedocs.io/en/latest/types/radial_menu_action/) | `null`     | Action executed when the left slot is selected and confirmed.                                                                                                 |
| `right_action`      | [Radial Menu Action](https://lunali-wiki.readthedocs.io/en/latest/types/radial_menu_action/) | `null`     | Action executed when the right slot is selected and confirmed.                                                                                                |
| `up_left_action`    | [Radial Menu Action](https://lunali-wiki.readthedocs.io/en/latest/types/radial_menu_action/) | `null`     | Action executed when the upper-left slot is selected and confirmed.                                                                                           |
| `up_right_action`   | [Radial Menu Action](https://lunali-wiki.readthedocs.io/en/latest/types/radial_menu_action/) | `null`     | Action executed when the upper-right slot is selected and confirmed.                                                                                          |
| `down_left_action`  | [Radial Menu Action](https://lunali-wiki.readthedocs.io/en/latest/types/radial_menu_action/) | `null`     | Action executed when the lower-left slot is selected and confirmed.                                                                                           |
| `down_right_action` | [Radial Menu Action](https://lunali-wiki.readthedocs.io/en/latest/types/radial_menu_action/) | `null`     | Action executed when the lower-right slot is selected and confirmed.                                                                                          |
| `lost_action`       | [Entity Action](https://origins.readthedocs.io/en/latest/types/entity_action_types/)         | `null`     | Entity action executed on the holder when the power is lost while the menu is open.                                                                           |

!!! note

Any direction slot left as `null` will simply do nothing when selected. You do not need to define all 9 slots. It is also recommended to set a sprite.

## Examples

```json
{
  "type": "lunali:radial_menu",
  "key": {
    "key": "key.origins.primary_active"
  },
  "swap_time": 10,
  "default_direction": "center",
  "up_action": {
    "action": {
      "type": "origins:heal",
      "amount": 4
    }
  },
  "down_action": {
    "action": {
      "type": "origins:exhaust",
      "amount": 2
    }
  }
}
```

This example opens a radial menu on the primary key. Selecting up heals the entity for 2 hearts, selecting down exhausts them.
