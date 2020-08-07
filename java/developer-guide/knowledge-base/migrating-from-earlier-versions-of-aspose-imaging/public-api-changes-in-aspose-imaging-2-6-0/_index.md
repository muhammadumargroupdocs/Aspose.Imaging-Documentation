---
title: Public API Changes in Aspose.Imaging 2.6.0
type: docs
weight: 170
url: /java/public-api-changes-in-aspose-imaging-2-6-0/
---

{{% alert color="primary" %}} 

This document describes the changes to the Aspose.Imaging API from version 2.4.0 to 2.6.0 that may be of interest to module/application developers. It includes not only new and updated public methods, [added classes etc.](/imaging/java/public-api-changes-in-aspose-imaging-2-6-0-html/), and [removed classes etc.](/imaging/java/public-api-changes-in-aspose-imaging-2-6-0-html/), but also a description of any changes in the behavior behind the scenes in Aspose.Imaging.

{{% /alert %}} 
## **Added Classes, Enumerations, Constructors and Methods**
### **Classes VectorRasterizationOptions & CadRasterizationOptions Added**
The new classes VectorRasterizationOptions and CadRasterizationOptions has been added to the com.aspose.imaging.ImageOptions in order to facilitate the user with CAD to vector & CAD to raster conversion. Moreover, some members of the PdfOptions class has been moved to the aforesaid classes.

With these changes in place, the CAD to PDF conversion can now be achieved as follow.

**Java**

{{< highlight csharp >}}

 Image image = Image.load(sourceFile);

//Create an instance of CadRasterizationOptions and set its various properties

CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();

rasterizationOptions.setBackgroundColor(Color.getWhite());

rasterizationOptions.setPageWidth(1600);

rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);

rasterizationOptions.setLayoutName("layout1");

//Create an instance of PdfOptions

PdfOptions pdfOptions = new PdfOptions();

//Set the VectorRasterizationOptions property

pdfOptions.setVectorRasterizationOptions(rasterizationOptions);

//Export the DWG to PDF

image.save(outputFile, pdfOptions);

{{< /highlight >}}
### **Support for Binary DXF Format Added**
In order to provide the support for Binary DXF file format, Aspose.Imaging for Java 2.6.0 has added the following classes & enumerations to the public API.

1. Class com.aspose.imaging.fileformats.cad.CadBinaryCodeValue
1. Class com.aspose.imaging.fileformats.cad.CadConsts.DxfFileFormat
1. Class com.aspose.imaging.fileformats.cad.CadParameters.CadBinaryParameter
1. Enum com.aspose.imaging.fileformats.cad.CadConsts.CadGroupCodeTypes
### **Class TransparentColorSetting Added**
A new class, com.aspose.imaging.TransparentColorSetting, assists with the process of specifying transparency for PNG images.

**Java**

{{< highlight csharp >}}

 image.savePixels(new Rectangle(0, 0, w, h), pixel);

PngOptions options = new PngOptions();

options.setTransparentColor(new TransparentColorSetting(Color.getRed()));

image.save(outputFile, options);

{{< /highlight >}}
### **Class ResolutionSetting Added**
The class com.aspose.imaging.ResolutionSetting has been added to Aspose.Imaging 2.6.0 to assist with the setting vertical & horizontal resolution for images. The members of {{ResolutionSetting }} class are:

1. com.aspose.imaging.ResolutionSetting.HorizontalResolution: Gets or sets the horizontal resolution.
1. com.aspose.imaging.ResolutionSetting.VerticalResolution: Gets or sets the vertical resolution.

**Java**

{{< highlight csharp >}}

 image.savePixels(new Rectangle(0, 0, height, width), pixel);

PngOptions options = new PngOptions();

options.setResolutionSettings(new ResolutionSetting(72, 96));

image.save(outputFile, options);

{{< /highlight >}}
### **Class DeflateCompressorException Added**
The class com.aspose.imaging.exceptions.Compressors.DeflateCompressorException has been added to Aspose.Imaging 2.6.0 to handle possible problems with PNG inner compression.
### **Constructors Added to PngImage Class**
We have added the following constructors to PngImage class in order to assist with the PNG encoding & decoding.

**com.aspose.imaging.fileformats.png.PngImage.#ctor(com.aspose.imaging.imageOptions.PngOptions, int, int)**

**Java**

{{< highlight csharp >}}

 PngOptions options = new PngOptions();

PngImage image = new PngImage(options, width, height);

{{< /highlight >}}

**com.aspose.imaging.fileformats.png.PngImage.#ctor(com.aspose.imaging.RasterImage, com.aspose.imaging.fileformats.png.PngColorType)**

**Java**

{{< highlight csharp >}}

 PngImage pngImage = new PngImage(prevLoadedImage, PngColorType.TruecolorWithAlpha);

{{< /highlight >}}

**com.aspose.imaging.fileformats.png.PngImage.#ctor(int , int, com.aspose.imaging.fileformats.png.PngColorType)**

**Java**

{{< highlight csharp >}}

 PngImage pngImage = new PngImage(width, height, PngColorType.TruecolorWithAlpha);

{{< /highlight >}}

**com.aspose.imaging.fileformats.png.PngImage.#ctor(String, com.aspose.imaging.fileformats.png.PngColorType)**

**Java**

{{< highlight csharp >}}

 PngImage pngImage = new PngImage("pngimage.png", PngColorType.TruecolorWithAlpha);

{{< /highlight >}}
### **Enumeration PngColorType added**
The enumeration com.aspose.imaging.fileformats.png.PngColorType has been added to Aspose.Imaging 2.6.0 to specify the PNG color type.
Possible values are as follows:

1. PngColorType.Greyscale: Represents the color type where each pixel is a greyscale sample.
1. PngColorType.Truecolor: Represents the color type where each pixel is an R,G,B triple.
1. PngColorType.IndexedColor: Represents the color type where each pixel is a palette index; a PLTE chunk shall appear.
1. PngColorType.GreyscaleWithAlpha: Represents the color type where each pixel is a greyscale sample followed by an alpha sample.
1. PngColorType.TruecolorWithAlpha: Represents the color type where each pixel is an R,G,B triple followed by an alpha sample.

**Java**

{{< highlight csharp >}}

 PngOptions options = new PngOptions();

options.setColorType(PngColorType.Greyscale);

{{< /highlight >}}
### **Field PixelFormat.BGR Added**
The field/enumeration com.aspose.imaging.PixelFormat.BGR has been added to distinguish the PNG RGB color order from BMP BGR color order.
The sample code below returns RGB color order:

**Java**

{{< highlight csharp >}}

 PngImage image = new PngImage(sourceFile);

Color[] pixels = image.loadPixels(image.getBounds());

System.out.println(image.getRawDataFormat().getPixelFormat());

{{< /highlight >}}

Sample code returns BGR color order. 

**Java**

{{< highlight csharp >}}

 BmpImage image = new BmpImage(sourceFile);

Color[] pixels = image.loadPixels(image.getBounds());

System.out.println(image.getRawDataFormat().getPixelFormat());

{{< /highlight >}}
### **Methods resizeWidthProportionally & resizeHeightProportionally Added**
The com.aspose.imaging.Image class has now exposed the resizeWidthProportionally and resizeHeightProportionally with the release of Aspose.Imaging 2.6.0 to assist with the re-sizing operation while keeping the aspect ratio. The aforesaid methods requires only one parameter (either Height or Width) and automatically calculates the other value.
### **Methods getProportionalWidth & getProportionalHeight Added**
The class com.aspose.imaging.Image has exposed getProportionalWidth & getProportionalHeight methods to calculate proportional width or height.

**Java**

{{< highlight csharp >}}

 int newHeight = Image.getProportionalHeight(150, 120, 100);  // 80

int newWIdth = Image.getProportionalWidth(150, 120, 60);  // 75

{{< /highlight >}}
### **Method RasterCachedImage.rotate Added**
The method com.aspose.imaging.RasterCachedImage.rotate has been added with version 2.6.0 to make it possible to specify a custom angle for image rotation.

**Java**

{{< highlight csharp >}}

 //Load an image in an instance of RasterImage class

RasterImage image = (RasterImage)Image.load(sourceFile);

//Specify rotate angle in degrees. Positive values will rotate clockwise

float rotateAngle = 10;

//If set to true you will have your image size changed according to rotated rectangle (corner points) projections in other case that leaves dimensions untouched and only internal image contents are rotated

Boolean resizeProportionally = true;

//Background color

Color backgroundColor = Color.getDarkRed();

//Rotate the image at specified angle

image.rotate(rotateAngle, resizeProportionally, backgroundColor);

//Save result

image.save(outputFile);

{{< /highlight >}}
### **Property PngImage.RawDataFormat Added**
The property com.aspose.imaging.fileformats.png.PngImage.RawDataFormat has been added with version 2.6.0 to help with PNG raw data format.

**Java**

{{< highlight csharp >}}

 PngImage pngImage = new PngImage("png.png");

System.out.println(pngImage.getRawDataFormat().getPixelFormat());

{{< /highlight >}}
### **Property ResolutionSettings Added**
The property ResolutionSettings has been added to the com.aspose.imaging.ImageOptionsBase class in order to make it accessible through all the options classes.

**Java**

{{< highlight csharp >}}

 TiffOptions options = new TiffOptions();

options.setResolutionSettings(new ResolutionSetting(72, 96));

{{< /highlight >}}
### **Properties Added to ExifData Class**
Following properties have been added to the com.aspose.imaging.exif.ExifData class.

1. Property ExifData.CommonTags
1. Property ExifData.ExifTags
1. Property ExifData.GPSTags
### **Properties Added to PngOptions Class**
Following properties have been added to the com.aspose.imaging.imageoptions.PngOptions class.

1. Property PngOptions.ColorType
1. Property PngOptions.Progressive
1. Property PngOptions.TransparentColor
### **Properties Added to PixelDataFormat Class**
Following properties have been added to the com.aspose.imaging.PixelDataFormat class.

1. Property PixelDataFormat.GrayscaleAlpha
1. Property PixelDataFormat.Rgb24BppPng
1. Property PixelDataFormat.Rgba32Bpp
## **Removed Classes and Methods**
### **Methods Removed from PngImage Class**
Following methods have been removed from the com.aspose.imaging.fileformats.png.PngImage class. It is advised to use the same methods of the base class instead.

1. Method PngImage.cacheData.
1. Method PngImage.crop(Rectangle).
1. Method PngImage.resize(int, int, ResizeType)
1. Method PngImage.rotateFlip(RotateFlipType).
1. Method PngImage.setResolution(double, double).
### **Unused CAD Classes Removed**
The following classes have been removed with version 2.6.0 of Aspose.Imaging for Java as they were of no use.

1. Class com.aspose.imaging.fileformats.cad.CadObjects.CadInvisibleObject.
1. Class com.aspose.imaging.fileformats.cad.CadObjects.CadMesh.
1. Class com.aspose.imaging.fileformats.cad.CadObjects.CadProxyEntity.
1. Class com.aspose.imaging.fileformats.cad.CadObjects.CadSectionEntity.
