---
title: Public API Changes in Aspose.Imaging 2.9.0
type: docs
weight: 150
url: /java/public-api-changes-in-aspose-imaging-2-9-0/
---

{{% alert color="primary" %}} 

This document describes the changes to the Aspose.Imaging API from version 2.7.0 to 2.9.0 that may be of interest to module/application developers. It includes not only new and updated public methods, [added classes etc.](/imaging/java/public-api-changes-in-aspose-imaging-2-9-0-html/) and [removed classes etc.](/imaging/java/public-api-changes-in-aspose-imaging-2-9-0-html/), but also a description of any changes in the behavior behind the scenes in Aspose.Imaging.

{{% /alert %}} 
## **Added Classes, Enumerations and Methods**
### **Improved the Imaging Core for Performance**
Aspose.Imaging for Java 2.9.0 has improved the overall performance by utilizing the following new methods for internal processing. By relying on these methods, the imaging core works now much more faster than before.

Details of newly added APIs are as follow:

- int[] RasterImage.loadArgb32Pixels(Rectangle desiredRectangle)
- void RasterImage.loadPartialArgb32Pixels(Rectangle desiredRectangle, IPartialArgb32PixelLoader pixelLoader);
- void RasterImage.saveArgb32Pixels(Rectangle desiredRectangle, int[] pixels);
- int ColorPalette.getArgbColor(int index);
- int[] ColorPalette.getArgbEntries();
- int ColorPalette.getNearestArgbColorIndex(int argb32Color);

These methods are intended to be used when high performance is required. Moreover, it is advised to use these methods instead of standard 'Color' related methods.
### **Support for Jpeg2000 Format Added**
Aspose.Imaging for Java 2.9.0 has introduced a series of new classes, methods, enumerations and properties to correctly process the images of type Jpeg2000. 

Details of newly added APIs are as follow:

- com.aspose.imaging.imageoptions.Jpeg2000Options Class
- com.aspose.imaging.fileformats.jpeg2000.Jpeg2000Image Class
- com.aspose.imaging.exceptions.imageformats.Jpeg2000Exception Class
- com.aspose.imaging.fileformat.Jpeg2000 Field/Enum
- com.aspose.imaging.imageoptions.Jpeg2000Options.#ctor Method
- com.aspose.imaging.imageoptions.Jpeg2000Options.#ctor(com.aspose.imaging.imageoptions.Jpeg2000Options) Method
- com.aspose.imaging.fileformats.jpeg2000.Jpeg2000Image.#ctor(com.aspose.imaging.RasterImage) Method
- com.aspose.imaging.fileformats.jpeg2000.Jpeg2000Image.#ctor(com.aspose.imaging.RasterImage, int) Method
- com.aspose.imaging.fileformats.jpeg2000.Jpeg2000Image.#ctor(int, int) Method
- com.aspose.imaging.fileformats.jpeg2000.Jpeg2000Image.#ctor(int, int, int) Method
- com.aspose.imaging.fileformats.jpeg2000.Jpeg2000Image.#ctor(Stream) Method
- com.aspose.imaging.fileformats.jpeg2000.Jpeg2000Image.#ctor(Stream, int) Method
- com.aspose.imaging.fileformats.jpeg2000.Jpeg2000Image.#ctor(String) Method
- com.aspose.imaging.fileformats.jpeg2000.Jpeg2000Image.#ctor(String, int)
- com.aspose.imaging.exceptions.imageformats.Jpeg2000Exception.#ctor(String) Method
- com.aspose.imaging.exceptions.imageformats.Jpeg2000Exception.#ctor(String, Exception) Method
- com.aspose.imaging.fileformats.jpeg2000.Jpeg2000Image.BitsPerPixel Property
- com.aspose.imaging.fileformats.jpeg2000.Jpeg2000Image.Comments Property
- com.aspose.imaging.fileformats.jpeg2000.Jpeg2000Image.Height Property
- com.aspose.imaging.fileformats.jpeg2000.Jpeg2000Image.RawDataFormat Property
- com.aspose.imaging.fileformats.jpeg2000.Jpeg2000Image.RawLineSize Property
- com.aspose.imaging.fileformats.jpeg2000.Jpeg2000Image.Width Property
- com.aspose.imaging.imageoptions.Jpeg2000Options.Comments Property
### **Optimized Dithering Mechanism**
The dithering process is now more optimized and predictable. All you need to do is to use the newly exposed RasterImage.dither method instead of the creating & setting DitheringSettings and RawDitheringMethod properties. The dithering is then performed right in-place and you can then review the dithered results by loading pixels or raw data. Additionally the DitheringMethod enumeration has been moved to the com.aspose.imaging package.

**Java**

{{< highlight csharp >}}

 RasterImage image = (RasterImage)Image.load(sourceFilePath);

image.dither(DitheringMethod.FloydSteinbergDithering, 4);

{{< /highlight >}}
### **Improved Creation of TiffOptions**
In order to facilitate the users and to avoid the miss-configuration of the TiffOptions instance, the Aspose.Imaging for Java API has exposed another constructor that accepts a parameter of type TiffExpectedFormat. Based on the selected value from the TiffExpectedFormat enumeration, the API auto configures all the mandatory properties for the TiffOptions instance in order to produce the desired results. 

Here is the list of the TiffExpectedFormat fields and their details for better understanding of the usage.

1. TiffExpectedFormat.Default: Setting the field to Default acts similar to the default constructor of TiffOptions class with no compression set and BitsPerPixel set to 1 in order to produce a black n white result. It is advised to use this field when other format specific properties are to be set manually according to the desired results.
1. TiffExpectedFormat.TiffCcitRle: Specific to RLE encoding while saving the result in 1 BitsPerPixel (black n white) TIFF format.
1. TiffExpectedFormat.TiffCcittFax3: Specific to CCITT Fax3 encoding while saving the result in 1 BitsPerPixel (black n white) TIFF format.
1. TiffExpectedFormat.TiffCcittFax4: Specific to CCITT Fax4 encoding while saving the result in 1 BitsPerPixel (black n white) TIFF format.
1. TiffExpectedFormat.TiffDeflateBW: Specific to Deflate compression while saving the result in 1 BitsPerPixel (black n white) TIFF format.
1. TiffExpectedFormat.TiffDeflateRGB: Specific to Deflate compression while saving the result in RGB (color) TIFF format.
1. TiffExpectedFormat.TiffJpegRGB: Specific to Jpeg compression while saving the result in RGB (color) TIFF format.
1. TiffExpectedFormat.TiffJpegYCBCR: Specific to Deflate compression while saving the result in YCBCR (color) TIFF format.
1. TiffExpectedFormat.TiffLzwBW: Specific to LZW compression while saving the result in 1 BitsPerPixel (black n white) TIFF format.
1. TiffExpectedFormat.TiffLzwRGB: Specific to LZW compression while saving the result in RGB (color) TIFF format.
1. TiffExpectedFormat.TiffLzwRGBA: Specific to LZW compression while saving the result in RGBA (color with transparency) TIFF format.
1. TiffExpectedFormat.TiffNoCompressionBW: Specific to uncompressed TIFF format while saving the result in 1 BitsPerPixel (black n white).
1. TiffExpectedFormat.TiffNoCompressionRGB: Specific to uncompressed TIFF format while saving the result in RGB (color).
1. TiffExpectedFormat.TiffNoCompressionRGBA: Specific to uncompressed TIFF format while saving the result in RGBA (color with transparency).

The following code snippet elaborates the usage of TiffExpectedFormat fields while creating an instance of TiffOptions class.

**Java**

{{< highlight csharp >}}

 //Load an image through file path location or stream

Image image = Image.load(sourceFilePath);

//Create an instance of TiffOptions while specifying desired format

//Passing TiffExpectedFormat.TiffJpegRGB will set the compression to Jpeg 

//and BitsPerPixel according to the RGB color space

TiffOptions options = new TiffOptions(TiffExpectedFormat.TiffJpegRGB); 

//Save the result in Tiff format RGB with Jpeg compression

image.save(destinationFilePath, options);

{{< /highlight >}}
### **Methods getDefaultRawData Added**
Aspose.Imaging for Java 2.9.0 has introduced two overload version of com.aspose.imaging.RasterImage.getDefaultRawData method that could be of help in retrieving empty raw data when image is created from scratch. Below are the signature for both overloads.

- com.aspose.imaging.RasterImage.getDefaultRawData(com.aspose.imaging.Rectangle,com.aspose.imaging.IPartialRawDataLoader,com.aspose.imaging.RawDataSettings)
- com.aspose.imaging.RasterImage.getDefaultRawData(com.aspose.imaging.Rectangle,com.aspose.imaging.RawDataSettings)
### **Property AutomaticLayoutsScaling Added**
Property com.aspose.imaging.imageoptions.CadRasterizationOptions.AutomaticLayoutsScaling has been added to perform auto layouts scaling for CAD images. This property could be of help in scenarios where scale for layouts differs from the scale for Model sheet. 

{{% alert color="primary" %}} 

Default value is false and layouts are scaled in a same manner as Model sheet.

{{% /alert %}} 

**Java**

{{< highlight csharp >}}

 CadImage cadImage = (CadImage)Image.load(sourceFilePath);

PdfOptions pdfOptions = new PdfOptions();

pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());

CadRasterizationOptions cadRasterizationOptions = (CadRasterizationOptions)pdfOptions.getVectorRasterizationOptions();

cadRasterizationOptions.setAutomaticLayoutsScaling(true);

cadImage.save(destinationFilePath, pdfOptions);

{{< /highlight >}}
## **Removed Properties**
### **Class Dithering.DitheringMethod Removed**
The com.aspose.imaging.dithering.DitheringMethod class has been replaced by the com.aspose.imaging.DitheringMethod class that can be used to apply the dithering while using the RasterImage.dither method.
### **Fields DitheringMethod.FloydSteinbergDithering & DitheringMethod.None Removed**
The enumeration fields com.aspose.imaging.dithering.DitheringMethod.FloydSteinbergDithering and com.aspose.imaging.dithering.DitheringMethod.None have been removed. It is advised to use the com.aspose.imaging.DitheringMethod.FloydSteinbergDithering and com.aspose.imaging.DitheringMethod.ThresholdDithering instead.
