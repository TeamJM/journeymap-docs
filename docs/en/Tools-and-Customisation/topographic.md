## **Terminology**

- **Topographic map**: A graphic representation of position, scale, shape, relief, and distribuation of selected natural and cultural features of an area of the Earth's surface.
- **Contour Line**: A line drawn on a topographic map connecting two points of equal elevation above sea level.
- **Contour Interval**: The vertical distance between two adjacent contour lines.

[Source](https://quizlet.com/16183184/topographic-maps-terms-flash-cards)

## **Overview of Topographic Maps in JourneyMap**

JourneyMap's Topographic Maps let you see the elevation contours of your world.  You can customize the topographic map properties and colors in (`.minecraft/journeymap/config/5.2/journeymap.topo.config`) according to what looks best to you, or what you want to emphasize.  

Here's how it works:

**{World height} ÷ {Number of colors} = {Contour interval}**

So, given a **world height of 256** blocks, a palette of **32 colors** will create 32 elevation contours, each with a **contour interval of 8** blocks high.

- 1st color: y 0-7
- 2nd color: y 8-15
- etc.

## **Customization**

The topographic maps config file `.minecraft/journeymap/config/5.2/journeymap.topo.config` can be edited with a simple text editor.  You can make changes to it, save it, and see the results immediately in JourneyMap without a need to restart.

The file has the following properties:

- **showContour**: Whether to show a contour line between contour intervals.  Defaults to true.
- **landContour**: Hex color (#rrggbb) of the contour lines on land.  Ignored if showContour is false.
- **waterContour**: Hex color (#rrggbb) of the contour lines on water.  Ignored if showContour is false.
- **land**: Quoted, comma-delimited list of hex colors (#rrggbb) for land terrain.  The number of colors determines the contour intervals (see Overview above).
- **water**: Quoted, comma-delimited list of hex colors (#rrggbb) for water.  The number of colors determines the contour intervals (see Overview above).
- **configVersion**: Used by JourneyMap to track configuration changes. You can ignore this, and don't need to change it.

If you get the file hopelessly broken, don't panic.  Simply delete it and restart Minecraft, and a new one will be created for you.

## **Choosing Good Colors**

In truth, finding a "one size fits all" set of colors for topographic maps isn't likely. Most real-life maps have nonlinear gradients customized to work best with the unique terrain features of a specific area.  For example, colors that help you see elevation changes clearly in a place like Kansas, US (very flat) would not work well in the neighboring state of Colorado and it's Rocky Mountains.

For some examples of topographic gradients used in the real world, see [this site](http://soliton.vm.bytemark.co.uk/pub/cpt-city/index.html), especially [this page](http://soliton.vm.bytemark.co.uk/pub/cpt-city/views/topo.html).

For your convenience, [the Color Editor tool](https://jsfiddle.net/techbrew/4vm9as0o/embedded/result/) and the [Gradient Generator tool](https://jsfiddle.net/techbrew/umh423j0/embedded/result/) may be helpful in choosing colors for your topographic maps.
