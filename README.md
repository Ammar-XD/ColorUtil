# ColorUtil Documentation

## Overview
The `ColorUtil` provides utility methods for working with colors in Minecraft plugins. It includes functions for translating color codes, converting between different color representations (hex, RGB, ChatColor), as well as color manipulation and blending.

## Methods

1. `translateColorCodes(String message)`
   - Translates color codes in a string using the '&' symbol.
   - **Parameters:** 
     - `message`: The message containing color codes.
   - **Returns:** 
     - Translated message with color codes.

2. `hexToChatColor(String hexColor)`
   - Converts a hex color code to Minecraft ChatColor.
   - **Parameters:** 
     - `hexColor`: The hex color code to convert.
   - **Returns:** 
     - ChatColor representing the hex color.

3. `chatColorToHex(ChatColor chatColor)`
   - Converts a Minecraft ChatColor to hex color code.
   - **Parameters:** 
     - `chatColor`: The ChatColor to convert.
   - **Returns:** 
     - Hex color code.

4. `rgbToChatColor(int red, int green, int blue)`
   - Converts RGB color values to Minecraft ChatColor.
   - **Parameters:** 
     - `red`: Red component (0-255).
     - `green`: Green component (0-255).
     - `blue`: Blue component (0-255).
   - **Returns:** 
     - ChatColor representing the RGB color.

5. `rgbToHex(int red, int green, int blue)`
   - Converts RGB color values to hex color code.
   - **Parameters:** 
     - `red`: Red component (0-255).
     - `green`: Green component (0-255).
     - `blue`: Blue component (0-255).
   - **Returns:** 
     - Hex color code.

6. `hexToRGB(String hexColor)`
   - Converts a hex color code to RGB components.
   - **Parameters:** 
     - `hexColor`: Hex color code.
   - **Returns:** 
     - Array containing RGB components [red, green, blue].

7. `darkenColor(String hexColor, int percentage)`
   - Darkens a given color by a specified percentage.
   - **Parameters:** 
     - `hexColor`: Hex color code to darken.
     - `percentage`: Percentage to darken (0-100).
   - **Returns:** 
     - Darkened hex color code.

8. `lightenColor(String hexColor, int percentage)`
   - Lightens a given color by a specified percentage.
   - **Parameters:** 
     - `hexColor`: Hex color code to lighten.
     - `percentage`: Percentage to lighten (0-100).
   - **Returns:** 
     - Lightened hex color code.

9. `blendColors(String color1, String color2, double ratio)`
   - Blend two colors with a specific ratio.
   - **Parameters:** 
     - `color1`: First color to blend.
     - `color2`: Second color to blend.
     - `ratio`: Blending ratio, should be between 0 and 1.
   - **Returns:** 
     - Blended color as hex code.

10. `generateColorGradient(String startColor, String endColor, int steps)`
    - Generate a gradient of colors between two colors.
    - **Parameters:** 
      - `startColor`: Starting color.
      - `endColor`: Ending color.
      - `steps`: Number of steps in the gradient.
    - **Returns:** 
      - Array of colors forming the gradient.

## Example Usage

```java
import org.bukkit.plugin.java.JavaPlugin;

public class MyPlugin extends JavaPlugin {
    
    @Override
    public void onEnable() {
        // Example usage of ColorUtil
        String message = "&6Hello &2world!";
        String translatedMessage = ColorUtil.translateColorCodes(message);
        getLogger().info("Translated message: " + translatedMessage);
        
        String hexColor = "#ff0000";
        ChatColor chatColor = ColorUtil.hexToChatColor(hexColor);
        getLogger().info("ChatColor from hex: " + chatColor);
    }
}
