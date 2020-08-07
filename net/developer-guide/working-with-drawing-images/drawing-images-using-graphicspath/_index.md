---
title: Drawing Images using GraphicsPath
type: docs
weight: 30
url: /net/drawing-images-using-graphicspath/
---

## **Drawing Images using GraphicsPath**
The [GraphicsPath](http://www.aspose.com/api/net/imaging/aspose.imaging/graphicspath) class is responsible for creating and maintaining a graphics path. The [GraphicsPath](http://www.aspose.com/api/net/imaging/aspose.imaging/graphicspath) has no reference to an image and does not change the image itself, instead, it can be considered as an object that contains metadata that describes the paths that [Graphics](http://www.aspose.com/api/search/net/imaging/Graphics) class can draw. The [GraphicsPath](http://www.aspose.com/api/net/imaging/aspose.imaging/graphicspath) class uses figures; each figure is either composed of a sequence of connected lines and curves or a geometric shape primitive. Each shape may be split into shape segments. You can add, remove and change different figures or shapes in a [GraphicsPath](http://www.aspose.com/api/net/imaging/aspose.imaging/graphicspath) object. When the [GraphicsPath](http://www.aspose.com/api/net/imaging/aspose.imaging/graphicspath) has been fully described, use the corresponding [Graphics](http://www.aspose.com/api/search/net/imaging/Graphics) class methods (DrawPath and [Fill Paths](http://www.aspose.com/api/net/imaging/aspose.imaging/graphics/methods/fillpath)) to draw over or fill the paths. The [Graphics](http://www.aspose.com/api/search/net/imaging/Graphics) class takes each shape segment and draws it to produce the final image.
### **Drawing using GraphicsPath Class**
Below is an example demonstrating the use of the [GraphicsPath](http://www.aspose.com/api/net/imaging/aspose.imaging/graphicspath) class. The example source code has been split in several parts to keep it simple and easy to follow. Step by step, the examples show you how to:

1. Create an image.
1. Initialize a [Graphics](http://www.aspose.com/api/search/net/imaging/Graphics) object.
1. Clear the surface.
1. Create an instance of [GraphicsPath](http://www.aspose.com/api/net/imaging/aspose.imaging/graphicspath).
1. Create a figure.
1. Add shapes to the figure.
1. Create a Figures array.
1. Draw paths.
1. Fill paths.
### **Drawing Images using GraphicsPath: Programming Samples**
#### **GraphicsPath : Create an Image**
Start by creating an image using any of the methods described in [Creating Files](http://www.aspose.com/docs/display/imagingnet/Drawing+and+Formatting+Images#DrawingandFormattingImages-CreatingImageFiles).

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-DrawingAndFormattingImages-CreatingAnImage-CreatingAnImage.cs" >}}


#### **GraphicsPath : Initialize a Graphics Objects**
Create and initialize a [Graphics](http://www.aspose.com/api/search/net/imaging/Graphics) object by passing the [Image](http://www.aspose.com/api/net/imaging/aspose.imaging/image) object to its constructor.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-GraphicsPath-InitializeGraphicsObjects-InitializeGraphicsObjects.cs" >}}


#### **GraphicsPath : Clear the Surface**
Clear the [Graphics](http://www.aspose.com/api/search/net/imaging/Graphics) surface by calling the [Graphics](http://www.aspose.com/api/search/net/imaging/Graphics) class [Clear](http://www.aspose.com/api/net/imaging/aspose.imaging/graphics/methods/clear) method and pass a Color as a parameter. This method fills the [Graphics](http://www.aspose.com/api/search/net/imaging/Graphics) surface with the color passed in as argument.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-GraphicsPath-ClearSurface-ClearSurface.cs" >}}


#### **GraphicsPath : Create an Instance of the GraphicsPath**
Create an instance of [GraphicsPath](http://www.aspose.com/api/net/imaging/aspose.imaging/graphicspath) with [GraphicsPath](http://www.aspose.com/api/net/imaging/aspose.imaging/graphicspath) set to **Alternate** by default. This mode determines how to fill the interior of a closed figure. The other possible [GraphicsPath](http://www.aspose.com/api/net/imaging/aspose.imaging/graphicspath) value is **Winding**.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-GraphicsPath-CreateInstanceofGraphicsPath-CreateInstanceofGraphicsPath.cs" >}}


#### **GraphicsPath : Create a Figure**
Create an instance of the [Figure](http://www.aspose.com/api/net/imaging/aspose.imaging/figure) class. As discussed earlier, [Figure](http://www.aspose.com/api/net/imaging/aspose.imaging/figure) can contain Shapes and shapes reside in the [Aspose.Imaging.Shapes](http://www.aspose.com/docs/display/imagingnet/Aspose.Imaging.Shapes+namespace) namespace.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-GraphicsPath-CreateFigure-CreateFigure.cs" >}}


#### **GraphicsPath : Add Shapes to the Figure**
The [Add Shapes](http://www.aspose.com/api/net/imaging/aspose.imaging/figure/methods/addshapes) method exposed by the [Figure](http://www.aspose.com/api/net/imaging/aspose.imaging/figure) class lets you add shapes to the figure. In the code examples below, several shapes are added to a [Figure](http://www.aspose.com/api/net/imaging/aspose.imaging/figure) object.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-GraphicsPath-AddShapeToFigure-AddShapeToFigure.cs" >}}


#### **GraphicsPath : Add Figures to an Array**
Multiple figures can be added to a [GraphicsPath](http://www.aspose.com/api/net/imaging/aspose.imaging/graphicspath) object using the AddFigures method exposed by the [GraphicsPath](http://www.aspose.com/api/net/imaging/aspose.imaging/graphicspath) class. This method accepts an array of figures as a parameter.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-GraphicsPath-AddFiguresToAnArray-AddFiguresToAnArray.cs" >}}


#### **GraphicsPath : Draw the Paths**
Draw the [GraphicsPath](http://www.aspose.com/api/net/imaging/aspose.imaging/graphicspath) using the DrawPath method exposed by [Graphics](http://www.aspose.com/api/search/net/imaging/Graphics) class. The method accepts two parameters. The first parameter is an object of the [Pen](http://www.aspose.com/api/net/imaging/aspose.imaging/pen) class, which determines the color, width and style of the path. The second parameter is the object of the [GraphicsPath](http://www.aspose.com/api/net/imaging/aspose.imaging/graphicspath) class, representing the path itself.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-GraphicsPath-DrawPaths-DrawPaths.cs" >}}


#### **GraphicsPath : Fill Paths**
You can fill a path by passing a [GraphicsPath](http://www.aspose.com/api/net/imaging/aspose.imaging/graphicspath) object to the [Fill Paths](http://www.aspose.com/api/net/imaging/aspose.imaging/graphics/methods/fillpath) method exposed by the [Graphics](http://www.aspose.com/api/search/net/imaging/Graphics) class. The [Fill Paths](http://www.aspose.com/api/net/imaging/aspose.imaging/graphics/methods/fillpath) method fills the path according to the fill mode (alternate or winding) currently set for the path. If the path has any open figures, the path is filled as if those figures were closed.

The [Fill Paths](http://www.aspose.com/api/net/imaging/aspose.imaging/graphics/methods/fillpath) method accepts two parameters. The first parameter is an object of any brush class from the [Aspose.Imaging.Brushes](http://www.aspose.com/docs/display/imagingnet/Aspose.Imaging.Brushes+namespace) namespace. The second parameter is the path itself. For the sake of this example, use the HatchBrush which is a rectangular brush with a hatch style, a foreground color, and a background color. Before passing the HatchBrush object to the [Fill Paths](http://www.aspose.com/api/net/imaging/aspose.imaging/graphics/methods/fillpath) method, set its properties.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-GraphicsPath-FillPaths-FillPaths.cs" >}}


### **GraphicsPath : Complete Source**
{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-DrawingAndFormattingImages-DrawingUsingGraphicsPath-DrawingUsingGraphicsPath.cs" >}}


All classes that implements IDisposable are instantiated in a Using statement to ensure that they are disposed of correctly.
