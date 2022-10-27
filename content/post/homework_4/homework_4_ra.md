+++
title = "Homework 4, research on application"
date = 2022-10-23T18:09:21+02:00
draft = false
author = "Andrea Di Paolo"
+++
Assignment:
<ul>
    <li> Give a simple introduction to graphics in the .NET environment. How to create a bitmap and a chart on it, </li>
    <li> explain in simple terms how to get device coordinates from world coordinates. </li>
</ul>
<!--more-->
# <mark> How to graphics in .NET</mark>
To manage graphics in the .NET environment we need to create objects from the bitmapObject and graphicsObject. We can do that in the Form Load event. Add these two lines to your form load event in C#:
```cs
bitmapObject = new Bitmap(PbSurface.Width, PbSurface.Height);
graphicsObject = Graphics.FromImage(bitmapObject);
Rectangle r = new Rectangle(30,30, b.Width - 30, b.Height - 30);
g.DrawRectangle(Pens.Red, r);
PbSurface.Image = bitmapObject;
```
The first new line creates a Bitmap image object. It uses the width and height of the Picture Box called PbSurface between the round brackets of Bitmap. The second new line create a new Graphics object. This has a routine called FromImage. In between the round brackets of FromImage you type the name of your Bitmap object. What you're doing here is using the Graphics object to draw on a bitmap. This is drawn in memory and retrieved when you want to display something on the Picture Box drawing surface. The DrawRectangle method will create in the bitmap object opened in g a rectancle. The last line finally assign the bitmap object to the picture box. To draw a chart it is possible to use the DrawLines method, it will display connected points that are in an array.

# <mark> From world coordinates to device coordinates </mark>
To pass from real world coordinates, from the cartesian axes, to a device coordinates we have to "adjust" the real ones like this:
```cs
 public int linearTransformX(double X, double minX, double maxX, int Left, int W)
{
    return Left + (int)(W * ((X - minX) / (maxX - minX)));
}
public int linearTransformY(double Y, double minY, double maxY, int Top, int H)
{
    return Top + (int)(H - H * ((Y - minY) / (maxY - minY)));
}
```

# References
[1] learn.microsoft.com, "PictureBox Class", [URL](https://learn.microsoft.com/en-us/dotnet/api/system.windows.forms.picturebox?view=windowsdesktop-7.0), <br>
[2] learn.microsoft.com, "Bitmap Class", [URL](https://learn.microsoft.com/en-us/dotnet/api/system.drawing.bitmap?view=dotnet-plat-ext-6.0), <br>
[3] learn.microsoft.com, "Graphics Class", [URL](https://learn.microsoft.com/en-us/dotnet/api/system.drawing.graphics?view=windowsdesktop-7.0), <br>
[4] homeandlearn.co.uk, "Bitmap and Graphics Objects", [URL](https://www.homeandlearn.co.uk/extras/draw-stick-figures/stick-figures-bitmaps-graphics.html). <br>