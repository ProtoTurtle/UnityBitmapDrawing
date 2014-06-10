UnityBitmapDrawing
==================

Bitmap Drawing API extension methods for Unity 3D's Texture2D class.

<b>What is it?</b>  
By default, Texture2D only provides the methods SetPixel and GetPixel (and SetPixels and GetPixels). This library extends that functionality with useful basic drawing operations.
```csharp
texture.DrawLine(new Vector2(0,0), new Vector2(100,200), Color.red);
```

<b>x = 0, y = 0 is the top left corner</b>  
This library uses the convention of having the left top corner of the bitmap be the 0, 0 position. By default, Texture2D uses the bottom left corner convention which can be confusing for bitmap operations.
  
![ScreenShot](https://raw.githubusercontent.com/ProtoTurtle/UnityBitmapDrawing/master/documentation/extensionMethods.png)
C# Extension Methods work in a way that adds methods to a existing class. To start using this, you only need to include the namespace:
```
using ProtoTurtle.BitmapDrawing;
```
Your Texture2D instances will then have all the new methods in them.

<b>Features</b>
* DrawPixel(position, color) - Draws a pixel but with the top left corner being position (x = 0, y = 0)
* DrawLine(start, end, color) - Draws a line between two points
* DrawCircle(position, radius, color) - Draws a circle
* DrawRectangle() - Draws a rectangle or a square
* DrawFilledRectangle() - Draws a rectangle or a square filled with a color
* FloodFill() - Starts a flood fill of a certaing at the point

<b>Example</b>
```csharp
using ProtoTurtle.BitmapDrawing;

// ...

Texture2D texture = new Texture2D(1024, 1024, TextureFormat.RGB24, false, true);
texture.filterMode = FilterMode.Point;
texture.wrapMode = TextureWrapMode.Clamp;

texture.DrawCircle(80, 150, 5, Color.blue);
texture.DrawCircle(300, 300, 200, Color.yellow);
texture.FloodFill(100, 100, Color.green);
texture.DrawLine(new Vector2(10, 10), new Vector2(400, 200), Color.magenta);
texture.Apply();
```
