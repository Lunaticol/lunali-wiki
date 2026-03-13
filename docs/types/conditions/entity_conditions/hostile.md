# Hostile Entity Condition

[Entity Condition Type](https://lunali-wiki.readthedocs.io/en/latest/types/entity_condition_types/)

Checks if a mob is a "hostile mob" by comparing it to any java classes extended from "hostile." Mobs with a brain, such as piglins or wardens are unaffected by this.

Type ID: `lunali:hostile`

## Examples

```JSON
"hostile": {
   "type": "lunali:mobs_ignore",
    "mob_condition": {
      "type": "lunali:hostile"
    }
  }
```

This example will cause hostile mobs to ignore you.
