---
title: Public API Changes in Aspose.Imaging 2.9.1
type: docs
weight: 140
url: /java/public-api-changes-in-aspose-imaging-2-9-1/
---

{{% alert color="primary" %}} 

This document describes the changes to the Aspose.Imaging API from version 2.9.0 to 2.9.1 that may be of interest to module/application developers. It includes not only new and updated public methods, [added classes etc.](/imaging/java/public-api-changes-in-aspose-imaging-2-9-1-html/) and [removed classes etc.](/imaging/java/public-api-changes-in-aspose-imaging-2-9-1-html/), but also a description of any changes in the behavior behind the scenes in Aspose.Imaging.

{{% /alert %}} 
## **Added Classes, Enumerations and Methods**
### **Convert Image or Part of Image to BufferedImage**
Aspose.Imaging for Java 2.9.1 has introduced two new method for the com.aspose.imaging.extensions.ImageExtensions that allows to convert an instance of Image to an instance of BufferedImage. 

Details of newly added methods are as follow:

- com.aspose.imaging.extensions.ImageExtensions.toJava(com.aspose.imaging.Image image)
- com.aspose.imaging.extensions.ImageExtensions.toJava(com.aspose.imaging.Image image, com.aspose.imaging.Rectangle rectangle)

**Java**

{{< highlight csharp >}}

 //Load an image through file path location or stream

Image image = Image.load(sourceFilePath);

//Convert Image to BufferedImage

BufferedImage bImage = ImageExtensions.toJava(image);

{{< /highlight >}}

**Java**

{{< highlight csharp >}}

 //Load an image through file path location or stream

Image image = Image.load(sourceFilePath);

//Convert part of Image to BufferedImage

BufferedImage bImage = ImageExtensions.toJava(image, new Rectangle(new Point(0, 0), new Size(100, 100)));

{{< /highlight >}}
### **Constructors for EmfOptions Added**
Aspose.Imaging for Java 2.9.1 has added new constructors for the com.aspose.imaging.imageoptions.EmfOptions class that can accept the DPI values. 

Details for these constructors are as follow.

- com.aspose.imaging.imageoptions.EmfOptions.#ctor(float dpiX, float dpiY)
- com.aspose.imaging.imageoptions.EmfOptions.#ctor(float dpi)

The blank constructor for the com.aspose.imaging.imageoptions.EmfOptions class has been removed from the Public APIs.
### **Method getWatermarkDrawer Added for Metafiles**
Aspose.Imaging for Java 2.9.1 has exposed the getWatermarkDrawer method for all classes that represent metafiles. The getWatermarkDrawer method returns an instance of Graphics2D object which allows to create custom watermarks.

Details of newly added methods are as follow:

- com.aspose.imaging.fileformats.metafile.EmfMetafileImage.getWatermarkDrawer
- com.aspose.imaging.fileformats.metafile.MetafileImage.getWatermarkDrawer
- com.aspose.imaging.fileformats.metafile.WmfMetafileImage.getWatermarkDrawer
### **Method MetafileImage.crop Added**
In order to facilitate the users to perform cropping on metafiles, the Aspose.Imaging for Java 2.9.1 has exposed two MetafileImage.crop methods.

Details of newly added methods are as follow:

- com.aspose.imaging.fileformats.metafile.MetafileImage.crop(int leftShift, int rightShift, int topShft, int bottomShift)
- com.aspose.imaging.fileformats.metafile.MetafileImage.crop(com.aspose.imaging.Rectangle rectangle)

**Java**

{{< highlight csharp >}}

 //Load an image through file path location or stream

MetafileImage metaImage = (MetafileImage) Image.load("emf file");

//Perform crop operation

metaImage.crop(30, 100, 30, 100);

//Save the result in raster format

metaImage.save("output.png", new PngOptions());

{{< /highlight >}}

{{% alert color="primary" %}} 

The cropping feature works only if result has to be stored in raster image formats. In case the result has to be stored in metafile format then the cropping will not take effect.

{{% /alert %}} 
### **Method MetafileImage.getCroppingRectangle Added**
Aspose.Imaging for Java 2.9.1 has exposed com.aspose.imaging.fileformats.metafile.MetafileImage.getCroppingRectangle method that can be used to get the cropping rectangle of the metafiles.
### **Methods Added for WmfRecorderGraphics2D Class**
The com.aspose.imaging.fileformats.metafile.WmfRecorderGraphics2D has exposed new methods because the WMF format does not support matrix transformations.

Details of newly added methods are as follow:

- com.aspose.imaging.fileformats.metafile.WmfRecorderGraphics2D.setTransform(java.awt.geom.AffineTransform transform)
- com.aspose.imaging.fileformats.metafile.WmfRecorderGraphics2D.transform(java.awt.geom.AffineTransform transform)
- com.aspose.imaging.fileformats.metafile.WmfRecorderGraphics2D.rotate(double theta)
- com.aspose.imaging.fileformats.metafile.WmfRecorderGraphics2D.rotate(double theta, double x, double y)
- com.aspose.imaging.fileformats.metafile.WmfRecorderGraphics2D.shear(double shX, double shY)
### **Optimized Performance**
In order to improve the overall performance of core processing, the Aspose.Imaging for Java 2.9.1 has added new interfaces and methods. Color is represented as 32-bit ARGB integer structure where there are 4 color channels and they are stored in the following order: | A | R | G | B |

New methods have parameters int[] instead Color[] or int instead Color. Also names of the newly exposed methods have the prefix Argb32 whereas the old interfaces (using Colors) remained unchanged.

**Added Interfaces** 
Class com.aspose.imaging.IPartialArgb32PixelLoader
Method com.aspose.imaging.IPartialArgb32PixelLoader.Process(com.aspose.imaging.Rectangle, int[], com.aspose.imaging.Point, com.aspose.imaging.Point)
Class com.aspose.imaging.IRasterImageArgb32PixelLoader
Method com.aspose.imaging.IRasterImageArgb32PixelLoader.LoadPartialArgb32Pixels(com.aspose.imaging.Rectangle, com.aspose.imaging.IPartialArgb32PixelLoader)

**Added Methods for IColorPalette** 
Method com.aspose.imaging.IColorPalette.GetArgb32Color(int)
Method com.aspose.imaging.IColorPalette.GetNearestColorIndex(int)
Property com.aspose.imaging.IColorPalette.Argb32Entries

**Implementation of Palette Classes** 
Method com.aspose.imaging.ColorPalette.#ctor(int[])
Method com.aspose.imaging.ColorPalette.#ctor(int[],Boolean)
Method com.aspose.imaging.ColorPalette.GetArgb32Color(int)
Method com.aspose.imaging.ColorPalette.GetNearestColorIndex(int)
Property com.aspose.imaging.ColorPalette.Argb32Entries
Method com.aspose.imaging.fileformats.psd.PsdColorPalette.#ctor(int[],Boolean)
Method com.aspose.imaging.fileformats.psd.PsdColorPalette.GetArgb32Color(int)
Method com.aspose.imaging.fileformats.psd.PsdColorPalette.GetNearestColorIndex(int)
Property com.aspose.imaging.fileformats.psd.PsdColorPalette.Argb32Entries

**Color Converters** 
Method com.aspose.imaging.CMYKColor.ToArgb32(com.aspose.imaging.CMYKColor[])
Method com.aspose.imaging.CMYKColor.ToCMYK(int)
Method com.aspose.imaging.CMYKColor.ToCMYK(int[])

**Get/Load Argb32 Pixels Methods** 
Method com.aspose.imaging.RasterImage.GetArgb32Pixel(int, int)
Method com.aspose.imaging.RasterImage.GetDefaultArgb32Pixels(com.aspose.imaging.Rectangle)
Method com.aspose.imaging.RasterImage.GetDefaultPixels(com.aspose.imaging.Rectangle, com.aspose.imaging.IPartialArgb32PixelLoader)
Method com.aspose.imaging.RasterImage.LoadArgb32Pixels(com.aspose.imaging.Rectangle)
Method com.aspose.imaging.RasterImage.LoadPartialArgb32Pixels(com.aspose.imaging.Rectangle, com.aspose.imaging.IPartialArgb32PixelLoader)
Method com.aspose.imaging.RasterImage.LoadPixelsInternal(com.aspose.imaging.Rectangle, com.aspose.imaging.IPartialArgb32PixelLoader)

**Set/Save Argb32 Pixels Methods** 
Method com.aspose.imaging.RasterImage.SetArgb32Pixel(int, int, int)
Method com.aspose.imaging.RasterImage.SaveArgb32Pixels(com.aspose.imaging.Rectangle, int[])
Method com.aspose.imaging.RasterImage.SavePixelsInternal(com.aspose.imaging.Rectangle, int[])
Method com.aspose.imaging.RasterCachedImage.SavePixelsInternal(com.aspose.imaging.Rectangle, int[])

**Other APIs** 
Method com.aspose.imaging.image.GetFitRectangle(com.aspose.imaging.Rectangle, int[])
Method com.aspose.imaging.image.GetFittingRectangle(com.aspose.imaging.Rectangle, int[], int, int)
Property com.aspose.imaging.fileformats.psd.resources.ThumbnailResource.ThumbnailArgb32Data

Working with new methods is similar as of the methods with Color arguments, for instance following is the code to load pixels with new implementation.

**Java**

{{< highlight java >}}

 com.aspose.imaging.RasterImage image = (com.aspose.imaging.RasterImage) com.aspose.imaging.Image.load(sfilename);

com.aspose.imaging.Rectangle objRect = image.getBounds();

int[] pixels = image.loadArgb32Pixels(objRect);

{{< /highlight >}}

Following is the code to save pixels with new implementation.

**Java**

{{< highlight java >}}

 int[] pixels;

com.aspose.imaging.RasterImage image = new com.aspose.imaging.fileformats.bmp.BmpImage(width, height);

image.SaveArgb32Pixels(image.getBounds(), pixels);

image.Save(outFileName);

{{< /highlight >}}
## **Removed Methods**
### **Constructor for EmfOptions Removed**
The com.aspose.imaging.imageoptions.EmfOptions.#ctor() has been removed. It is advised to use the newly added constructors that could accept DPI values.
