<img width="600" src="https://i.imgur.com/g60BMQH.jpeg"/>

# Mod Mmm Ortholinear Edition

The ortholinear build is almost identical to the standard one and utilizes the same daughterboard.  Below are some additional notes regarding this layout

* 1u or 2u spacebars
* 1u or 1.5u vertical center keys
* [KLE Layout](http://www.keyboard-layout-editor.com/#/gists/545144b17525bc6cdfc75478dbc9cbd3)

## Switch Spacer Pad

Since the Model M backplate was not designed around an ortholinear layout, the mounting screws end overlapping the switch footprints on the PCB.  What this means is that the screw heads will prevent the switch from being seated completely against the PCB.  As a work around, I've designed what is esentially a foam spacer to lift switches high enough to clear the screws.  The screw heads are around 0.9mm, so this spacer needs to cut out of 1mm EVA foam.  Because of this extra lift, the alpha keycaps end up being 1mm higher than the rest, and the gap between the case and the keycap increases by the same amount.  The path to the file is:

`case/ortho-switch-pad.ai`

<img width="300" src="https://i.imgur.com/e4oIn5v.png" />

NOTE: There are no cutouts for the stabalizers, so you may need to cut those manually with scissors depending on your layout.

In my build, I have this spacer pad sitting directly on top of the PCB.  Then I have 3.5mm plate foam on top of that.  And then finally the 5mm switch plate on top of that.

I wasn't able to find 3.5mm foam, so my stack (for the alpha keys only) ends up looking like this:

| Layer | Tickness | Description |
| ----- | -------- | ----------- |
| 1     | 1.0 mm     | Steel backplate |
| 2     | 2.0 mm     | Case foam |
| 3     | 1.6 mm     | PCB |
| 4     | 1.0 mm     | Switch spacer pad |
| 5     | 1.5 mm     | Plate foam |
| 6     | 2.0 mm     | Plate foam |
| 7     | 1.5 mm     | Switch plate |

## Switch Plate

I did not create a universal plate since I didn't want to risk the structural strength by adding too many cuts.  You will need I have an all 1u key version under the layer name `Plate`, and a layout with 1.5u vertical center keys, and 2u spacebars labed as `Plate v2`.  You can optionally apply the `Hinges` layer to cut hinges in between the switch holes to allow it bend there, thus keeping the switch holes relatively flat.

* `case/plate-orth.ai` - File location
* `Plate` - Layer with 1u keys
* `Plate v2` - Layer with 1.5u vertical center and 2u space keys
* `F-row support` - 1.5mm acrylic plate support