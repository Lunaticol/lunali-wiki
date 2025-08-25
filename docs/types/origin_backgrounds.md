# Origin Backgrounds

Lunali introduces the ability to set custom backgrounds for Origins v1.10.0 (1.20.1)

## How do I set custom backgrounds?

Setting custom backgrounds is pretty straight forward and only requires two lines of code and minimal resourcepack set-up.

There are two background options you can set. You can use one or the other, or both if you prefer.

| Field              | Type                                                                                | Default                               | Description                                                                  |
| ------------------ | ----------------------------------------------------------------------------------- | ------------------------------------- | ---------------------------------------------------------------------------- |
| `background`       | [Identifier](https://origins.readthedocs.io/en/latest/types/data_types/string/)     | lunali:textures/gui/choose_origin.png | Defines the GUI background to use. Just uses the default Origins background. |
| `block_background` | [Identifier](https://origins.readthedocs.io/en/latest/types/data_types/identifier/) | minecraft:textures/block/dirt.png     | Defines the tile background when choosing an origin for the first time.      |

```JSON
{
  "name": "Lunali",
  "description": "Description",
  "impact": 0,
  "icon": "origins:orb_of_origin",
  "powers": [],
  "background": "lunali:textures/gui/choose_origin_test.png",
  "block_background": "minecraft:textures/block/cherry_log.png"
}
```

## How do I make a custom background?

<center>

![background template](https://i.imgur.com/Oz49RsX.png)

</center>

Above is the default template for custom backgrounds. If you havent noticed, some areas may have a box over them.

- Black: Border for the Origin GUI
- Turqoise: Where text is visible
- Pink: the boundry for the Plaque aswell as where it renders on the main GUI

### Additonal Information

- The circles are impacts, changing one changes all 3 that are rendered
- The gray bock with the green smile is unused, ignore it (or say hi to karl)
- the red & blue rectangles are scroll bars, red for unclicked and blue for clicked.
- The black bar beside the scroll bars is the main scroll bar.
