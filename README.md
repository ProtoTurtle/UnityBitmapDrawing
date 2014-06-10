UnityBitmapDrawing
==================

Bitmap Drawing API extension methods for Unity 3D's Texture2D class.

<b>What is it?</b>
By default, Texture2D only provides the methods SetPixel and GetPixel (and SetPixels and GetPixels). This library extends that functionality with useful basic drawing operations.
```csharp
texture.DrawLine(new Vector2(0,0), new Vector2(100,200), Color.red);
```



<b>Usage:</b>
```csharp
Texture2D texture = new Texture2D(1024, 1024, TextureFormat.RGB24, false, true);
texture.filterMode = FilterMode.Point;
texture.wrapMode = TextureWrapMode.Clamp;

texture.DrawCircle(80, 150, 5, Color.blue);
texture.DrawCircle(300, 300, 200, Color.yellow);
texture.FloodFill(100, 100, Color.green);
texture.DrawLine(new Vector2(10, 10), new Vector2(400, 200), Color.magenta);
```
