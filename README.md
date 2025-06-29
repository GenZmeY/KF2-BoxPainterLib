# Box Painter Library
[![GitHub tag (latest by date)](https://img.shields.io/github/v/tag/GenZmeY/KF2-BoxPainterLib)](https://github.com/GenZmeY/KF2-BoxPainterLib/tags)
[![GitHub](https://img.shields.io/github/license/GenZmeY/KF2-BoxPainterLib)](COPYING.LESSER)

## Description
2D box drawing library for [Killing Floor 2](https://store.steampowered.com/app/232090/Killing_Floor_2/).  
Ported from [YetAnotherScoreboard](https://github.com/GenZmeY/KF2-YetAnotherScoreboard) and published under LGPLv3 due to licensing issues with some closed source mods.  

## Using
1. Add Box Painter Library to your project  
2. Create `BoxPainter` object: `BoxPainter = new class'BoxPainterLib.BoxPainter';`  
3. Initialize the canvas: `BoxPainter.Canvas = <REPLACE_THIS_WITH_YOUR_CANVAS_OBJECT>;`  
4. `BoxPainter` is ready! Use functions [DrawBox(...)](https://github.com/GenZmeY/KF2-BoxPainterLib/blob/master/Classes/BoxPainter.uc#L21) and [DrawShapedBox(...)](https://github.com/GenZmeY/KF2-BoxPainterLib/blob/master/Classes/BoxPainterBase.uc#L147) to draw boxes on your UI.  

## Available Functions
**DrawShapedBox(float X, float Y, float W, float H, float Edge, byte TopLeftShape, byte TopRightShape, byte BottomLeftShape, byte BottomRightShape)**  
Draws a box using the [shape code](https://github.com/GenZmeY/KF2-BoxPainterLib/blob/master/Classes/BoxPainterBase.uc#L31) for each corner:  
- ECS_Corner
- ECS_BeveledCorner
- ECS_VerticalCorner
- ECS_HorisontalCorner

**DrawBox(float X, float Y, float Width, float Height, float Edge, optional byte Shape = 0)**  
Draws a box using the shape code:  
![codes_table](rect_shapes.png)  

## Examples
- [YetAnotherScoreboard](https://github.com/GenZmeY/KF2-YetAnotherScoreboard)  

## Status: Completed
- The library works with the current version of the game (v1150) and I have implemented everything I planned.  
- Development has stopped: I no longer have the time or motivation to maintain this library. No further updates or bug fixes are planned.  

## Mirrors
- https://github.com/GenZmeY/KF2-BoxPainterLib  
- https://codeberg.org/GenZmeY/KF2-BoxPainterLib  

## License
**LGPL-3.0-or-later**  
  
[![license](https://www.gnu.org/graphics/lgplv3-with-text-154x68.png)](COPYING.LESSER)  
