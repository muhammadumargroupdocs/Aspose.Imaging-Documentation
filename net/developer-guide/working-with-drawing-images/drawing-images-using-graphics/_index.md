---
title: Drawing Images using Graphics
type: docs
weight: 20
url: /net/drawing-images-using-graphics/
---

## **Drawing Images using Graphics**
With the Aspose.Imaging library you can draw simple shapes like lines, rectangles and circles, as well as complex shapes like polygons, curves, arcs and Bezier shapes. Aspose.Imaging library creates such shapes using [Graphics](http://www.aspose.com/api/search/net/imaging/Graphics) class that resides in the Aspose.Imaging namespace. Graphics objects are responsible for performing different drawing operations on an image, thus changing the image's surface. The [Graphics](http://www.aspose.com/api/search/net/imaging/Graphics) class uses a variety of helper objects to enhance the shapes:

- Pens, to draw lines, outline shapes, or render other geometric representations.
- Brushes, to define how areas are filled in.
- Fonts, to define the shape of characters of text.
### **Drawing with the Graphics Class**
Below is a code example demonstrating the use of the [Graphics](http://www.aspose.com/api/search/net/imaging/Graphics) class. The example source code has been split into several parts to keep it simple and easy to follow. Step by step, the examples show how to:

1. Create an image.
1. Create and initialize a [Graphics](http://www.aspose.com/api/search/net/imaging/Graphics) object.
1. Clear the surface.
1. Draw an ellipse.
1. Draw a filled polygon and save the image.
### **Programming Samples**
#### **Creating an Image**
Start by creating an image using any of the methods described in [Creating Files](http://www.aspose.com/docs/display/imagingnet/Drawing+and+Formatting+Images#DrawingandFormattingImages-CreatingImageFiles).

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-GraphicsPath-CreateAnImage.cs" >}}


#### **Create and Initialize a Graphics Object**
Then create and initialize a [Graphics](http://www.aspose.com/api/search/net/imaging/Graphics) object by passing the [Image](http://www.aspose.com/api/net/imaging/aspose.imaging/image) object to its constructor.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-GraphicsPath-InitializeGraphicsObjects-InitializeGraphicsObjects.cs" >}}


#### **Clear the Surface**
Clear the [Graphics](http://www.aspose.com/api/search/net/imaging/Graphics) surface by calling the [Graphics](http://www.aspose.com/api/search/net/imaging/Graphics) class [Clear](http://www.aspose.com/api/net/imaging/aspose.imaging/graphics/methods/clear) method and pass a color as a parameter. This method fills the [Graphics](http://www.aspose.com/api/search/net/imaging/Graphics) surface with the color passed in as argument.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-DrawingAndFormattingImages-ClearTheSurface-ClearTheSurface.cs" >}}


#### **Draw an Ellipse**
You may notice that the [Graphics](http://www.aspose.com/api/search/net/imaging/Graphics) class has exposed plenty of methods to draw and fill shapes. You'll find get the complete list of methods in the [Aspose.Imaging for .NET API Reference](http://www.aspose.com/docs/display/imagingnet/Aspose.Imaging+for+.NET++API+Reference). There are several overloaded versions of the [DrawEllipse](http://www.aspose.com/api/net/imaging/aspose.imaging/graphics/methods/drawellipse/index) method exposed by the [Graphics](http://www.aspose.com/api/search/net/imaging/Graphics) class. All these methods accept a [Pen](http://www.aspose.com/api/net/imaging/aspose.imaging/pen) object as its first argument. The later parameters are passed to define the bounding rectangle around the ellipse. For the sake of this example, use the version accepting a [Rectangle](http://www.aspose.com/api/net/imaging/aspose.imaging/rectangle) object as the second parameter to draw an ellipse using the [Pen](http://www.aspose.com/api/net/imaging/aspose.imaging/pen) object in your desired color.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-DrawingAndFormattingImages-DrawAnEllipse-DrawAnEllipse.cs" >}}


#### **Draw a Filled Polygon**
Next, draw a polygon using the LinearGradientBrush and an array of points. The [Graphics](http://www.aspose.com/api/search/net/imaging/Graphics) class has exposed several overloaded versions of the FillPolygon() method. All of these accept a Brush object as its first argument, defining the characteristics of the fill. The second parameter is an array of points. Please note that every two consecutive points in the array specify a side of the polygon.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-DrawingAndFormattingImages-DrawAFilledPolygon-DrawAFilledPolygon.cs" >}}


### **Drawing Images using Graphics : Complete Source**
{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-DrawingAndFormattingImages-DrawingUsingGraphics-DrawingUsingGraphics.cs" >}}

All classes that implements IDisposable and access unmanaged resources are instantiated in a Using statement to ensure that they are disposed of correctly.
## **Memory Strategy optimization**
Graphics operations can be proceeded using memory strategy optimization - ie limiting memory buffer size for operation.

{{< gist "aspose-com-gists" "2d1bcb9853315458808ffbcd9e7e3e02" "MemoryStrategyOptimizationGraphics.cs" >}}






