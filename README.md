# KF2-BoxPainterLib

[![GitHub tag (latest by date)](https://img.shields.io/github/v/tag/GenZmeY/KF2-BoxPainterLib)](https://github.com/GenZmeY/KF2-BoxPainterLib/tags)
[![GitHub top language](https://img.shields.io/github/languages/top/GenZmeY/KF2-BoxPainterLib)](https://docs.unrealengine.com/udk/Three/WebHome.html)
[![GitHub](https://img.shields.io/github/license/GenZmeY/KF2-BoxPainterLib)](LICENSE)

**2D box drawing library**  

# Add to your project
There are two ways to add BoxPainterLib to your project:  
### 1. As [git submodule](https://git-scm.com/book/en/v2/Git-Tools-Submodules)  
Open git-bash and go to your project: `cd <your_project_path>`  
Add submodule: `git submodule add https://github.com/GenZmeY/KF2-BoxPainterLib BoxPainterLib`  

**updating library:**  
Get updates: `pushd BoxPainterLib && git pull && popd`  
Commit the changes: `git add BoxPainterLib && git commit -m 'update box painter lib'`  

### 2. As standalone sources
Create a `BoxPainterLib` folder and put [this repo](https://github.com/GenZmeY/KF2-BoxPainterLib) there.  

# Using
1. Create `BoxPainter` object: `BoxPainter = new class'BoxPainterLib.BoxPainter';`  
2. Initialize the canvas: `BoxPainter.Canvas = <REPLACE_THIS_WITH_YOUR_CANVAS_OBJECT>;`  
3. `BoxPainter` is ready! Use functions [DrawBox(...)](https://github.com/GenZmeY/KF2-BoxPainterLib/blob/master/Classes/BoxPainter.uc#L3) and [DrawShapedBox(...)](https://github.com/GenZmeY/KF2-BoxPainterLib/blob/master/Classes/BoxPainterBase.uc#L129) to draw cool interface boxes.  

# Available Functions
#### DrawShapedBox(float X, float Y, float W, float H, float Edge, byte TopLeftShape, byte TopRightShape, byte BottomLeftShape, byte BottomRightShape)
Draws a box using the [shape code](https://github.com/GenZmeY/KF2-BoxPainterLib/blob/master/Classes/BoxPainterBase.uc#L13) for each corner:  
- ECS_Corner
- ECS_BeveledCorner
- ECS_VerticalCorner
- ECS_HorisontalCorner

#### DrawBox(float X, float Y, float Width, float Height, float Edge, optional byte Shape = 0)
Draws a box using the shape code:  
![](rect_shapes.png)

# Build
If you are using [KF2-BuildTools](https://github.com/GenZmeY/KF2-BuildTools) open `builder.cfg` and add `BoxPainterLib` **first** in `PackageBuildOrder` and `PackageUpload` parameters  

If you are building manually add line `ModPackages=BoxPainterLib` to your `KFEditor.ini` before all other `ModPackages`  

Now build the mod. `BoxPainterLib.u` library will be next to your `*.u` files  

# Examples
[KF2-YetAnotherScoreboard](https://github.com/GenZmeY/KF2-YetAnotherScoreboard)  

# License
[GNU LGPLv3](LICENSE)
