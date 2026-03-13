# Offset Action

[Entity Action](https://lunali-wiki.readthedocs.io/en/latest/types/entity_action_types/)

Causes the users screen to shake.

Type ID: `lunali:offset_action`

| Field            | Type                                                                          | Default | Description                                                                                                        |
| ---------------- | ----------------------------------------------------------------------------- | ------- | ------------------------------------------------------------------------------------------------------------------ |
| `gravity`        | [Boolean](https://origins.readthedocs.io/en/latest/types/data_types/boolean/) | true    | When true, fangs will spawn on the top most block in their position, when false fangs will spawn at the players y. |
| `texture`        | [String](https://origins.readthedocs.io/en/latest/types/data_types/string/)   | null    | The texture the fangs should use.                                                                                  |
| `sound`          | [String](https://origins.readthedocs.io/en/latest/types/data_types/string/)   | null    | Overwrites the normal fang chomp sound.                                                                            |
| `radial`         | [Boolean](https://origins.readthedocs.io/en/latest/types/data_types/boolean/) | false   | Should the fangs spawn in a circle instead of in a line.                                                           |
| `length`         | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/) | 5       | How many fangs spawn in the line.                                                                                  |
| `damage`         | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/)     | 6.0     | The amount of damage the fangs should do.                                                                          |
| `delay`          | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/) | 0       | how long before each fang spawns out from the ground.                                                              |
| `spacing`        | [Double](https://origins.readthedocs.io/en/latest/types/data_types/double/)   | 1.25    | how far apart each fang should be from each other.                                                                 |
| `yaw_offset`     | [Float](https://origins.readthedocs.io/en/latest/types/data_types/float/)     | 0.0     | Sets the roation of the fangs.                                                                                     |
| `max_range`      | [Double](https://origins.readthedocs.io/en/latest/types/data_types/double/)   | 16.0    | The maximum range the fangs can spawn regardless of length & spacing.                                              |
| `fangs_per_ring` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer/) | 12      | How many fangs should spawn per ring.                                                                              |
| `ring_spacing`   | [Double](https://origins.readthedocs.io/en/latest/types/data_types/double/)   | 1.5     | Distance between each ring.                                                                                        |
| `start_radius`   | [Double](https://origins.readthedocs.io/en/latest/types/data_types/double/)   | 1.0     | radius of the first ring.                                                                                          |

## Examples

```JSON
"fangs_grr": {
    "type": "origins:active_self",
    "key": "key.origins.quinary_active",
    "cooldown": 0,
    "entity_action": {
      "type": "lunali:spawn_evoker_fangs",
      "texture": "lunali:textures/entity/pink_spike_wisp.png",
      "delay": 10,
      "radial": true,
      "gravity": true
    }
  }
```

This example will spawn rings in a radius
10 second delay between each ring aswell as obeying gravity. It also has a set texture.
