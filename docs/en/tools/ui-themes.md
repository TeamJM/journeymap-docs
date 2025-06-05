## **Overview**

The look-and-feel of the toolbars can be changed using the UI Theme button (icon of a paint palette). You can also create new themes with your own images, icons, and colors. 

## **Available Themes**

- [Vault](https://minecraft.curseforge.com/projects/journeymap/files/2303051) (Fallout Pipboy)

**If you create a really cool theme and would like to share it with the world, PM techbrew on MinecraftForums (or tweet [@JourneyMapMod](https://twitter.com/journeymapmod) on twitter).**

## **How to Create a UI Theme: Easy Start**

1. Copy **.minecraft/journeymap/icon/theme/Victorian** and paste the copy into the **/theme** folder with a new name ex: ("MyTheme")
2. In your new theme folder:
    1. Delete **Purist.theme.json**
    2. Rename **Victorian.theme.json** to something new (Ex: "MyTheme.theme.json")
    3. Edit your new theme.json file with a text editor and change the directory name, theme name, and author properties to match your folder and file. 
    4. Browse the images in your theme directory and see how they correlate to the buttons and toolbars in JourneyMap
    5. Replace the images in your theme directory with your own creations - except for the images in **icon/**, and make sure your replacements are the exact same size as the ones you're replacing.
3. Use the UI Theme button in the Fullscreen Map (with the icon of a paint palette) to switch to your new Theme
4. Share your theme with others by simply zipping up your theme folder and giving it to them.  When they unzip it to **.minecraft/journeymap/icon/theme/**, they can use it by pressing the UI Theme button

## **How to Create a UI Theme: Advanced Tips**

The theme.json file uses conventions very similar to Cascading Style Sheets (CSS).  Images like the button icons can be colored using standard hex RGB colors just like you'd use in CSS.

The image sizes don't need to be exactly the same as what you'll find in the Victorian theme. However, you'll need to edit the theme.json file and start changing image dimensions to match your creation.

Create images 2x larger than the sizes you specify in the theme.json file.  This allows for larger resolution screens and people who use Minecraft's GUI Scale Auto (or Large) to still have nice looking buttons.

## **How to Designate a Default UI Theme in Modpacks**

Modpacks can provide a theme for users by creating a theme folder just like the above. If a modpack author so wishes, they can also designate that theme to be the default theme for users who are using JourneyMap 5 for the first time.  

This can be done by creating this file: .minecraft/journeymap/icon/theme/default.theme.config

The contents of the file provide the theme folder name, json file name, and the name designated within the json file, like so:

```json
 {
  "directory": "Victorian",
  "filename": "Victorian",
  "name": "Victorian"
 }
```

## **Code and Comments for Themes**

Each theme.json file is read by JourneyMap via GSON and creates a simple Java class hierarchy used to build the UI elements. **You cannot change the structure of the json files in any way, only edit the values provided.**

Here is the source code of the Java class used to generate the theme.json files.  The comments are intended to give you insight into how each property is used:

```java
 /**
  * Theme specification for JourneyMap 5.0
  */
 public class Theme implements Comparable<Theme>
 {
    /**
     * Current version of this specification
     */
    public static final int VERSION = 1; 
 
    /**
     * Theme author.
     */
    @Since(1)
    public String author; 
 
    /**
     * Theme name.
     */
    @Since(1)
    public String name; 
 
    /**
     * Parent directory name of theme files.
     */
    @Since(1)
    public String directory; 
 
    /**
     * Container specs for images in the /container directory.
     * Currently just Toolbar.
     */
    @Since(1)
    public Container container = new Container(); 
 
    /**
     * UI Control specs for images in the /control directory.
     * Currently: Button & Toggle.
     */
    @Since(1)
    public Control control = new Control(); 
 
    /**
     * FullMap Map specs for images in the /fullscreen directory.
     */
    @Since(1)
    public Fullscreen fullscreen = new Fullscreen(); 
 
    /**
     * General size for all icons in the /icon directory
     */
    @Since(1)
    public ImageSpec icon = new ImageSpec(); 
 
    /**
     * Circular Minimap specs for images in the /minimap/circle directory.
     */
    @Since(1)
    public Minimap minimap = new Minimap(); 
 
    /**
     * Container class for images in /container.
     */
    public static class Container
    {
        /**
         * Specs for toolbar images in /container.
         */
        @Since(1)
        public Toolbar toolbar = new Toolbar(); 
 
        /**
         * Toolbar class for toolbar images in /container.
         */
        public static class Toolbar
        {
            /**
             * Specs for horizontal toolbar images.
             */
            @Since(1)
            public ToolbarSpec horizontal = new ToolbarSpec(); 
 
            /**
             * Specs for vertical toolbar images.
             */
            @Since(1)
            public ToolbarSpec vertical = new ToolbarSpec(); 
 
            /**
             * ToolbarSpec class. A toolbar consists of a beginning image, a
             * repeating inner image (one rep per button), and an end image.
             * <p/>
             * Filenames expected by the Theme loader are:
             * toolbar_begin.png, toolbar_inner.png, toolbar_end.png
             */
            public static class ToolbarSpec
            {
                /**
                 * True to use theme images, false for invisible.
                 */
                @Since(1)
                public boolean useThemeImages; 
 
                /**
                 * Filename prefix. Example: "h" for horizontal, "v" for vertical.
                 */
                @Since(1)
                public String prefix = ""; 
 
                /**
                 * Margin in pixels around toolbar.
                 */
                @Since(1)
                public int margin; 
 
                /**
                 * Padding in pixels between buttons in toolbar.
                 */
                @Since(1)
                public int padding; 
 
                /**
                 * Image dimensions for the beginning of the toolbar.
                 */
                @Since(1)
                public ImageSpec begin; 
 
                /**
                 * Image dimensions for the inner repeating section of the toolbar.
                 */
                @Since(1)
                public ImageSpec inner; 
 
                /**
                 * Image dimensions for the end of the toolbar.
                 */
                @Since(1)
                public ImageSpec end;
            }
        }
    } 
 
    /**
     * Control class for images in /control
     */
    public static class Control
    {
        /**
         * Specs for a normal button.
         */
        @Since(1)
        public ButtonSpec button = new ButtonSpec(); 
 
        /**
         * Specs for a toggle button.
         */
        @Since(1)
        public ButtonSpec toggle = new ButtonSpec(); 
 
        /**
         * Specification for a button.
         * Filenames expected by the Theme loader are:
         * on.png, off.png, hover.png, disabled.png
         */
        public static class ButtonSpec
        {
            /**
             * True to use theme images.  False to use current resource pack's button texture.
             */
            @Since(1)
            public boolean useThemeImages; 
 
            /**
             * Button width.
             */
            @Since(1)
            public int width; 
 
            /**
             * Button height.
             */
            @Since(1)
            public int height; 
 
            /**
             * Filename prefix. Optional.
             */
            @Since(1)
            public String prefix = ""; 
 
            /**
             * String format style (using § control codes) for tooltips when the button is on.
             */
            @Since(1)
            public String tooltipOnStyle = ""; 
 
            /**
             * String format style (using § control codes) for tooltips when the button is off.
             */
            @Since(1)
            public String tooltipOffStyle = ""; 
 
            /**
             * String format style (using § control codes) for tooltips when the button is disabled.
             */
            @Since(1)
            public String tooltipDisabledStyle = ""; 
 
            /**
             * Hex color for icons when button is on.
             */
            @Since(1)
            public String iconOnColor = ""; 
 
            /**
             * Hex color for icons when button is off.
             */
            @Since(1)
            public String iconOffColor = ""; 
 
            /**
             * Hex color for icons when button is hovered.
             */
            @Since(1)
            public String iconHoverColor = ""; 
 
            /**
             * Hex color for icons when button is disabled.
             */
            @Since(1)
            public String iconDisabledColor = "";
        }
    } 
 
    /**
     * FullMap class for images in /fullscreen.
     */
    public static class Fullscreen
    {
        /**
         * Hex color for map background (behind tiles).
         */
        @Since(1)
        public String mapBackgroundColor = ""; 
 
        /**
         * Hex color for background of status text on the bottom of the screen.
         */
        @Since(1)
        public LabelSpec statusLabel = new LabelSpec();
    } 
 
    /**
     * Image dimensions.
     */
    public static class ImageSpec
    {
        /**
         * Image width.
         */
        @Since(1)
        public int width; 
 
        /**
         * Image height.
         */
        @Since(1)
        public int height; 
 
        public ImageSpec()
        {
        } 
 
        public ImageSpec(int width, int height)
        {
            this.width = width;
            this.height = height;
        }
    } 
 
    /**
     * Class for images in /minimap
     */
    public static class Minimap
    {
        /**
         * Circular minimap specifications, corresponds to /minimap/circle
         */
        @Since(1)
        public MinimapCircle circle = new MinimapCircle(); 
 
        /**
         * Square minimap specifications, corresponds to /minimap/square
         */
        @Since(1)
        public MinimapSquare square = new MinimapSquare(); 
 
        /**
         * Shared minimap spec
         */
        public static abstract class MinimapSpec
        {
            /**
             * Minimum margin outside of minimap frame.
             */
            @Since(1)
            public int margin; 
 
            /**
             * Whether key shown at the top of the minimap (FPS) should
             * be inside the frame (true), or outside/above it (false)
             */
            @Since(1)
            public boolean labelTopInside; 
 
            /**
             * Margin around top labels in minimap.
             */
            @Since(1)
            public int labelTopMargin; 
 
            /**
             * Whether labels shown at the bottom of the minimap (location) should
             * be inside the frame (true), or outside/below it (false)
             */
            @Since(1)
            public boolean labelBottomInside; 
 
            /**
             * Margin around bottom labels in minimap.
             */
            @Since(1)
            public int labelBottomMargin; 
 
            /**
             * Label spec for showing FPS
             */
            @Since(1)
            public LabelSpec fpsLabel = new LabelSpec(); 
 
            /**
             * Label spec for showing location
             */
            @Since(1)
            public LabelSpec locationLabel = new LabelSpec(); 
 
            /**
             * Label spec for showing location
             */
            @Since(1)
            public LabelSpec biomeLabel = new LabelSpec(); 
 
            /**
             * Label spec for showing compass points
             */
            @Since(1)
            public LabelSpec compassLabel = new LabelSpec(); 
 
            /**
             * Background image on which to place compass points.
             * Expecting filename "compass_point.png"
             */
            @Since(1)
            public ImageSpec compassPoint = new ImageSpec(); 
 
            /**
             * Hex color used to draw compass point. Use #ffffff to leave unchanged.
             */
            @Since(1)
            public String compassPointColor = "#ffffff"; 
 
            /**
             * Number of pixels to pad around a compass point's key. Effects the scaled size of the compass point image.
             */
            @Since(1)
            public int compassPointLabelPad; 
 
            /**
             * Number of pixels to shift the center of a compass point away from the map center.
             * Use this to adjust how it overlays the minimap frame.
             */
            @Since(1)
            public double compassPointOffset; 
 
            /**
             * Whether to show the North compass point.
             * Defaults to true.
             */
            @Since(1)
            public boolean compassShowNorth = true; 
 
            /**
             * Whether to show the South compass point.
             * Defaults to true.
             */
            @Since(1)
            public boolean compassShowSouth = true; 
 
            /**
             * Whether to show the East compass point.
             * Defaults to true.
             */
            @Since(1)
            public boolean compassShowEast = true; 
 
            /**
             * Whether to show the West compass point.
             * Defaults to true.
             */
            @Since(1)
            public boolean compassShowWest = true; 
 
            /**
             * Number of pixels to shift the center of an "off-map" waypoint away from the map center.
             * Use this to adjust how it overlays the minimap frame.
             */
            @Since(1)
            public double waypointOffset; 
 
            /**
             * Hex color used to draw reticle.
             */
            @Since(1)
            public String reticleColor = ""; 
 
            /**
             * General alpha transparency (0-255) of reticle.
             * Default is 128.
             */
            @Since(1)
            public int reticleAlpha = 96; 
 
            /**
             * Alpha transparency (0-255) for the heading segment of reticle.
             * Default is 150.
             */
            @Since(1)
            public int reticleHeadingAlpha = 112; 
 
            /**
             * General reticle thickness in pixels.
             * Default is 2.25 pixels.
             */
            @Since(1)
            public double reticleThickness = 2.25; 
 
            /**
             * Reticle thickness in pixels for the heading segment of reticle.
             * Default is 2.5 pixels.
             */
            @Since(1)
            public double reticleHeadingThickness = 2.5; 
 
            /**
             * Number of pixels to shift the outer endpoint of a reticle segment away from the map center.
             * Negative values move the end closer to the center.
             * Use this to adjust how it underlays the minimap frame.
             */
            @Since(1)
            public int reticleOffset; 
 
            /**
             * Hex color to apply to frame image. Use #ffffff to keep unchanged.
             */
            @Since(1)
            public String frameColor = ""; 
 

            /**
             * Image prefix (optional) for images in /minimap/square
             */
            @Since(1)
            public String prefix = "";
        } 
 
        /**
         * Class for images in /minimap/circle.
         * <p/>
         * The mask defines the area of the minimap that will be shown.
         * The rim is the frame/overlay placed atop the minimap.
         * <p/>
         * Filenames expected by the Theme loader are:
         * mask_256.png, rim_256.png, mask_512.png, rim_512.png, compass_point.png
         * <p/>
         * Minimap sizes <=256 will use mask_256 and rim_256. Anything
         * larger will use mask_512 and rim_512.
         */
        public static class MinimapCircle extends MinimapSpec
        {
            /**
             * Size of rim_256.png (Ideally 256x256px)
             */
            @Since(1)
            public ImageSpec rim256 = new ImageSpec(256, 256); 
 
            /**
             * Size of mask_256.png (Ideally 256x256px)
             */
            @Since(1)
            public ImageSpec mask256 = new ImageSpec(256, 256); 
 
            /**
             * Size of rim_512.png (Ideally 512x512px)
             */
            @Since(1)
            public ImageSpec rim512 = new ImageSpec(512, 512); 
 
            /**
             * Size of mask_512.png (Ideally 512x512px)
             */
            @Since(1)
            public ImageSpec mask512 = new ImageSpec(512, 512);
        } 
 
        /**
         * Class for images in /minimap/square.
         * <p/>
         * Filenames expected by the Theme loader are:
         * topleft.png, top.png, topright.png, left.png, right.png,
         * bottomleft.png, bottom.png, bottomright.png, compass_point.png
         * <p/>
         * Images are centered along the edges of the minimap area.
         */
        public static class MinimapSquare extends MinimapSpec
        {
            /**
             * Dimensions of topleft.png
             */
            @Since(1)
            public ImageSpec topLeft = new ImageSpec(); 
 
            /**
             * Dimensions of top.png. It will be stretched to fit minimap size.
             */
            @Since(1)
            public ImageSpec top = new ImageSpec(); 
 
            /**
             * Dimensions of topright.png
             */
            @Since(1)
            public ImageSpec topRight = new ImageSpec(); 
 

            /**
             * Dimensions of right.png. It will be stretched to fit minimap size.
             */
            @Since(1)
            public ImageSpec right = new ImageSpec(); 
 
            /**
             * Dimensions of bottomright.png
             */
            @Since(1)
            public ImageSpec bottomRight = new ImageSpec(); 
 
            /**
             * Dimensions of bottom.png. It will be stretched to fit minimap size.
             */
            @Since(1)
            public ImageSpec bottom = new ImageSpec(); 
 
            /**
             * Dimensions of bottomleft.png
             */
            @Since(1)
            public ImageSpec bottomLeft = new ImageSpec(); 
 
            /**
             * Dimensions of left.png. It will be stretched to fit minimap size.
             */
            @Since(1)
            public ImageSpec left = new ImageSpec();
        }
    } 
 
    /**
     * Class for defining key characteristics.
     */
    public static class LabelSpec
    {
        /**
         * Hex color for key background.
         * Default is black.
         */
        @Since(1)
        public String backgroundColor = toHexColor(Color.black); 
 
        /**
         * Alpha transparency (0-255) of key background.
         * Default is 200.
         */
        @Since(1)
        public int backgroundAlpha = 200; 
 
        /**
         * Hex color for key foreground.
         * Default is white.
         */
        @Since(1)
        public String foregroundColor = toHexColor(Color.white); 
 
        /**
         * Alpha transparency (0-255) of key background.
         * Default is 255.
         */
        @Since(1)
        public int foregroundAlpha = 255; 
 
        /**
         * Whether to use font shadow.
         * Default is false.
         */
        @Since(1)
        public boolean shadow = false;
    } 
 
    /**
     * The basis of default.theme.json, which
     * is used to load a specific theme as the default.
     */
    public static class DefaultPointer
    {
        /**
         * Parent directory name of theme files.
         */
        @Since(1)
        public String directory; 
 
        /**
         * Theme filename.
         */
        @Since(1)
        public String filename; 
 
        /**
         * Theme name.
         */
        @Since(1)
        public String name; 
 
        protected DefaultPointer()
        {
        } 
 
        public DefaultPointer(Theme theme)
        {
            this.name = theme.name;
            this.filename = theme.name;
            this.directory = theme.directory;
        }
    }
 }
```
