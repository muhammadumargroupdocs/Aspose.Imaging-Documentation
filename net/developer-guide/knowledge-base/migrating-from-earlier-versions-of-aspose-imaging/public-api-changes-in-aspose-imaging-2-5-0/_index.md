---
title: Public API Changes in Aspose.Imaging 2.5.0
type: docs
weight: 180
url: /net/public-api-changes-in-aspose-imaging-2-5-0/
---

{{% alert color="primary" %}} 

This document describes the changes to the Aspose.Imaging API from version 2.4.0 to 2.5.0 that may be of interest to module/application developers. It includes not only new and updated public methods, [added classes etc.](/imaging/net/public-api-changes-in-aspose-imaging-2-5-0-html/), and [removed classes etc.](/imaging/net/public-api-changes-in-aspose-imaging-2-5-0-html/), but also a description of any changes in the behavior behind the scenes in Aspose.Imaging.

{{% /alert %}} 
## **Added Classes, Constructors and Methods**
### **Constructors Added to PngImage Class**
We have added the following constructors to PngImage class in order to assist with the PNG encoding & decoding.

**Aspose.Imaging.FileFormats.Png.PngImage.#ctor(Aspose.Imaging.ImageOptions.PngOptions,System.Int32,System.Int32)**

**C#**

{{< highlight csharp >}}

 var options = new PngOptions();

var image = new PngImage(options, width, height);

{{< /highlight >}}

**Visual Basic**

{{< highlight csharp >}}

 Dim options = New PngOptions()

Dim image = New PngImage(options, width, height)

{{< /highlight >}}

**Aspose.Imaging.FileFormats.Png.PngImage.#ctor(Aspose.Imaging.RasterImage,Aspose.Imaging.FileFormats.Png.PngColorType)**

**C#**

{{< highlight csharp >}}

 var pngImage = new PngImage(prevLoadedImage, PngColorType.TruecolorWithAlpha)

{{< /highlight >}}

**Visual Basic**

{{< highlight csharp >}}

 Dim pngImage = New PngImage(prevLoadedImage, PngColorType.TruecolorWithAlpha)

{{< /highlight >}}

**Aspose.Imaging.FileFormats.Png.PngImage.#ctor(System.Int32,System.Int32,Aspose.Imaging.FileFormats.Png.PngColorType)**

**C#**

{{< highlight csharp >}}

 var pngImage = new PngImage(width, height, PngColorType.TruecolorWithAlpha);

{{< /highlight >}}

**Visual Basic**

{{< highlight csharp >}}

 Dim pngImage = New PngImage(width, height, PngColorType.TruecolorWithAlpha)

{{< /highlight >}}

**Aspose.Imaging.FileFormats.Png.PngImage.#ctor(System.String,Aspose.Imaging.FileFormats.Png.PngColorType)**

**C#**

{{< highlight csharp >}}

 var pngImage = new PngImage("pngimage.png", PngColorType.TruecolorWithAlpha);

{{< /highlight >}}

**Visual Basic**

{{< highlight csharp >}}

 Dim pngImage = New PngImage("pngimage.png", PngColorType.TruecolorWithAlpha)

{{< /highlight >}}
### **Class TransparentColorSetting Added**
A new class, Aspose.Imaging.TransparentColorSetting, assists with the process of specifying transparency for PNG images.

**C#**

{{< highlight csharp >}}

 image.SavePixels(new Rectangle(0, 0, w, h), pixel);

PngOptions options = new PngOptions();

options.TransparentColor = new TransparentColorSetting(Color.Red);

image.Save(ms, options);

{{< /highlight >}}

**Visual Basic**

{{< highlight csharp >}}

 image.SavePixels(New Rectangle(0, 0, w, h), pixel)

Dim options As New PngOptions()

options.TransparentColor = New TransparentColorSetting(Color.Red)

image.Save(ms, options)

{{< /highlight >}}

Please check the detailed article [Specifying Transparency for PNG Images](http://aspose.com/docs/display/imagingnet/Specifying+Transparency+for+PNG+Images) for more information on this topic.
### **Class ResolutionSetting Added**
The class Aspose.Imaging.ResolutionSetting has been added to Aspose.Imaging 2.5.0 to assist with the setting vertical & horizontal resolution for images.
The members of {{ResolutionSetting }} class are:

1. Property Aspose.Imaging.ResolutionSetting.HorizontalResolution: Gets or sets the horizontal resolution.
1. Property Aspose.Imaging.ResolutionSetting.VerticalResolution: Gets or sets the vertical resolution.

**C#**

{{< highlight csharp >}}

 image.SavePixels(new Rectangle(0, 0, h, w), pixl);

PngOptions options = new PngOptions();

options.ResolutionSettings = new ResolutionSetting(72, 96);

image.Save(ms, options);

{{< /highlight >}}

**Visual Basic**

{{< highlight csharp >}}

 image.SavePixels(New Rectangle(0, 0, h, w), pixl)

Dim options As New PngOptions()

options.TransparentColor = New TransparentColorSetting(Color.Red)

image.Save(ms, options)

{{< /highlight >}}
### **Class DeflateCompressorException Added**
The class Aspose.Imaging.Exceptions.Compressors.DeflateCompressorException has been added to Aspose.Imaging 2.5.0 to handle possible problems with PNG inner compression.
### **Enumeration PngColorType added**
The enumeration Aspose.Imaging.FileFormats.Png.PngColorType has been added to Aspose.Imaging 2.5.0 to specify the PNG color type.
Possible values are as follows:

1. PngColorType.Greyscale: Represents the color type where each pixel is a greyscale sample.
1. PngColorType.Truecolor: Represents the color type where each pixel is an R,G,B triple.
1. PngColorType.IndexedColor: Represents the color type where each pixel is a palette index; a PLTE chunk shall appear.
1. PngColorType.GreyscaleWithAlpha: Represents the color type where each pixel is a greyscale sample followed by an alpha sample.
1. PngColorType.TruecolorWithAlpha: Represents the color type where each pixel is an R,G,B triple followed by an alpha sample.

**C#**

{{< highlight csharp >}}

 PngOptions options = new PngOptions();

options.ColorType = PngColorType.Greyscale;

{{< /highlight >}}

**Visual Basic**

{{< highlight csharp >}}

 Dim options As New PngOptions()

options.ColorType = PngColorType.Greyscale

{{< /highlight >}}
### **Field PixelFormat.BGR Added**
The field/enumeration Aspose.Imaging.PixelFormat.BGR has been added to distinguish the PNG RGB color order from BMP BGR color order.
The sample code below returns RGB color order:

**C#**

{{< highlight csharp >}}

 using (PngImage image = new PngImage(testFilePath))

{

   pixels = image.LoadPixels(image.Bounds);

   Console.WriteLine(image.RawDataFormat.PixelFormat);

}

{{< /highlight >}}

**Visual Basic**

{{< highlight csharp >}}

 Using image As New PngImage(testFilePath)

   pixels = image.LoadPixels(image.Bounds)

   Console.WriteLine(image.RawDataFormat.PixelFormat)

End Using

{{< /highlight >}}

Sample code returns BGR color order. 

**C#**

{{< highlight csharp >}}

 using (BmpImage image = new BmpImage("bmp.bmp"))

{

   pixels = image.LoadPixels(image.Bounds);

   Console.WriteLine(image.RawDataFormat.PixelFormat);

}

{{< /highlight >}}

**Visual Basic**

{{< highlight csharp >}}

 Using image As New BmpImage("bmp.bmp")

   pixels = image.LoadPixels(image.Bounds)

   Console.WriteLine(image.RawDataFormat.PixelFormat)

End Using

{{< /highlight >}}
### **Method RasterCachedImage.Rotate Added**
The method Aspose.Imaging.RasterCachedImage.Rotate has been added with version 2.5.0 to make it possible to specify a custom angle for image rotation.

**C#**

{{< highlight csharp >}}

 using (Image image = Image.Load(fileName))

{

    RasterImage rasterImage = (RasterImage)image;

    if (!rasterImage.IsCached)

    {

        rasterImage.CacheData();

    }

    // The rotate angle in degrees. Positive values will rotate clockwise

    float rotateAngle = 10;

    // If set to true you will have your image size changed according to rotated rectangle (corner points) projections in other case that leaves dimensions untouched and only internal image contents are rotated

    bool resizeProportionally = true;

    // Background color

    Aspose.Imaging.Color backgroundColor = Color.DarkRed;

    rasterImage.Rotate(rotateAngle, resizeProportionally, backgroundColor);

    // save

    rasterImage.Save(outputFile);

}

{{< /highlight >}}

**Visual Basic**

{{< highlight csharp >}}

 Using image As Image = Image.Load(fileName)

	Dim rasterImage As RasterImage = CType(image, RasterImage)

	If (Not rasterImage.IsCached) Then

		rasterImage.CacheData()

	End If

	' The rotate angle in degrees. Positive values will rotate clockwise

	Dim rotateAngle As Single = 10

	' If set to true you will have your image size changed according to rotated rectangle (corner points) projections in other case that leaves dimensions untouched and only internal image contents are rotated

	Dim resizeProportionally As Boolean = True

	' Background color

	Dim backgroundColor As Aspose.Imaging.Color = Color.DarkRed

	rasterImage.Rotate(rotateAngle, resizeProportionally, backgroundColor)

	' save

	rasterImage.Save(outputFile)

End Using

{{< /highlight >}}
### **Property PngImage.RawDataFormat Added**
The property Aspose.Imaging.FileFormats.Png.PngImage.RawDataFormat has been added with version 2.5.0 to help with PNG raw data format.

**C#**

{{< highlight csharp >}}

 var pngImage = new PngImage("png.png");

Console.WriteLine(pngImage.RawDataFormat.PixelFormat);

{{< /highlight >}}

**Visual Basic**

{{< highlight csharp >}}

 Dim pngImage = New PngImage("png.png")

Console.WriteLine(pngImage.RawDataFormat.PixelFormat)

{{< /highlight >}}
### **Property ResolutionSettings Added**
The property ResolutionSettings has been added to the Aspose.Imaging.ImageOptionsBase class in order to make it accessible through all the options classes.

**C#**

{{< highlight csharp >}}

 TiffOptions options = new TiffOptions();

opts.ResolutionSettings = new ResolutionSetting(72, 96);

{{< /highlight >}}

**Visual Basic**

{{< highlight csharp >}}

 Dim options As New TiffOptions()

opts.ResolutionSettings = New ResolutionSetting(72, 96)

{{< /highlight >}}
### **Properties Added to ExifData Class**
Following properties have been added to the Aspose.Imaging.Exif.ExifData class.

1. Property ExifData.CommonTags
1. Property ExifData.ExifTags
1. Property ExifData.GPSTags
### **Properties Added to PngOptions Class**
Following properties have been added to the Aspose.Imaging.ImageOptions.PngOptions class.

1. Property PngOptions.ColorType
1. Property PngOptions.Progressive
1. Property PngOptions.TransparentColor
### **Properties Added to PixelDataFormat Class**
Following properties have been added to the Aspose.Imaging.PixelDataFormat class.

1. Property PixelDataFormat.GrayscaleAlpha
1. Property PixelDataFormat.Rgb24BppPng
1. Property PixelDataFormat.Rgba32Bpp
## **Removed Classes and Methods**
### **Methods Removed from PngImage Class**
Following methods have been removed from the Aspose.Imaging.FileFormats.Png.PngImage class. It is advised to use the same methods of the base class instead.

1. Method PngImage.CacheData.
1. Method PngImage.Crop(Aspose.Imaging.Rectangle).
1. Method PngImage.Resize(System.Int32,System.Int32,Aspose.Imaging.ResizeType)
1. Method PngImage.RotateFlip(Aspose.Imaging.RotateFlipType).
1. Method PngImage.SetResolution(System.Double,System.Double).
### **Unused CAD Classes Removed**
The following classes have been removed with version 2.5.0 of Aspose.Imaging for .NET as they were of no use.

1. Class Aspose.Imaging.FileFormats.Cad.CadObjects.CadInvisibleObject.
1. Class Aspose.Imaging.FileFormats.Cad.CadObjects.CadMesh.
1. Class Aspose.Imaging.FileFormats.Cad.CadObjects.CadProxyEntity.
1. Class Aspose.Imaging.FileFormats.Cad.CadObjects.CadSectionEntity.
