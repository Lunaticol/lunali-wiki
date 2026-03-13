# Energy Swirl
[Power Type](https://lunali-wiki.readthedocs.io/en/latest/types/power_types/)

Renders an animated energy swirl effect around the entity, using a custom texture and configurable motion pattern.

Type ID: `lunali:energy_swirl`

| Field | Type | Default | Description |
| --- | --- | --- | --- |
| `texture` | [String](https://origins.readthedrees.io/en/latest/types/data_types/string/) | | The resource location of the texture to use for the swirl effect (e.g. `mymod:textures/entity/swirl.png`). |
| `size` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/) | | The size of the swirl effect. |
| `speed` | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/) | `1.0` | How fast the swirl animates. Higher values spin faster. |
| `motion_type` | [String](https://origins.readthedocs.io/en/latest/types/data_types/string/) | `"CREEPER"` | The animation pattern of the swirl. Accepted values: `VERTICAL`, `HORIZONTAL`, `CREEPER`, `WITHER`. |

!!! note
    Multiple `energy_swirl` powers can be active on the same entity simultaneously, each rendering independently.

## Examples
```json
 "energy_swirl": {
    "type": "lunali:energy_swirl",
    "texture": "minecraft:textures/misc/enchanted_glint_entity.png",
    "size": 1,
    "speed": 1,
    "motion_type": "WITHER"
}
```
This example renders a wither-style swirl effect around the entity at 1 speed using the enchantment glint texture.
