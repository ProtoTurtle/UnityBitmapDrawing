UnityBitmapDrawing
==================

Bitmap Drawing API extension methods for Unity 3D's Texture2D class.

This will add extension methods for drawing bitmap shapes like lines, circles and rectangles.


*Usage:
Texture2D texture = new Texture2D(1024, 1024, TextureFormat.RGB24, false, true);
texture.filterMode = FilterMode.Point;
texture.wrapMode = TextureWrapMode.Clamp;

texture.DrawCircle(80, 150, 5, Color.blue);
texture.DrawCircle(300, 300, 200, Color.yellow);
texture.FloodFill(100, 100, Color.green);
texture.DrawLine(new Vector2(10, 10), new Vector2(400, 200), Color.magenta);

