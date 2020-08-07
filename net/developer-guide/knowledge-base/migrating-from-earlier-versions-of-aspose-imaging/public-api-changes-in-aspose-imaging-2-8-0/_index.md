---
title: Public API Changes in Aspose.Imaging 2.8.0
type: docs
weight: 150
url: /net/public-api-changes-in-aspose-imaging-2-8-0/
---

{{% alert color="primary" %}} 

This document describes the changes to the Aspose.Imaging API from version 2.7.0 to 2.8.0 that may be of interest to module/application developers. It includes not only new and updated public methods, [added APIs](/imaging/net/public-api-changes-in-aspose-imaging-2-8-0-html/) and [removed APIs](/imaging/net/public-api-changes-in-aspose-imaging-2-8-0-html/), but also a description of any changes in the behavior behind the scenes in Aspose.Imaging.

{{% /alert %}} 
## **Added Classes, Enumerations and Methods**
### **Support for Jpeg2000 Format Added**
Aspose.Imaging for .NET 2.8.0 has introduced a series of new classes, methods, enumerations and properties to correctly process the images of type Jpeg2000. Details of newly added APIs are as follow:

- Aspose.Imaging.ImageOptions.Jpeg2000Options Class
- Aspose.Imaging.FileFormats.Jpeg2000.Jpeg2000Image Class
- Aspose.Imaging.Exceptions.ImageFormats.Jpeg2000Exception Class
- Aspose.Imaging.FileFormat.Jpeg2000 Field/Enum
- Aspose.Imaging.ImageOptions.Jpeg2000Options.#ctor Method
- Aspose.Imaging.ImageOptions.Jpeg2000Options.#ctor(Aspose.Imaging.ImageOptions.Jpeg2000Options) Method
- Aspose.Imaging.FileFormats.Jpeg2000.Jpeg2000Image.#ctor(Aspose.Imaging.RasterImage) Method
- Aspose.Imaging.FileFormats.Jpeg2000.Jpeg2000Image.#ctor(Aspose.Imaging.RasterImage,System.Int32) Method
- Aspose.Imaging.FileFormats.Jpeg2000.Jpeg2000Image.#ctor(System.Int32,System.Int32) Method
- Aspose.Imaging.FileFormats.Jpeg2000.Jpeg2000Image.#ctor(System.Int32,System.Int32,System.Int32) Method
- Aspose.Imaging.FileFormats.Jpeg2000.Jpeg2000Image.#ctor(System.IO.Stream) Method
- Aspose.Imaging.FileFormats.Jpeg2000.Jpeg2000Image.#ctor(System.IO.Stream,System.Int32) Method
- Aspose.Imaging.FileFormats.Jpeg2000.Jpeg2000Image.#ctor(System.String) Method
- Aspose.Imaging.FileFormats.Jpeg2000.Jpeg2000Image.#ctor(System.String,System.Int32)
- Aspose.Imaging.Exceptions.ImageFormats.Jpeg2000Exception.#ctor(System.String) Method
- Aspose.Imaging.Exceptions.ImageFormats.Jpeg2000Exception.#ctor(System.String,System.Exception) Method
- Aspose.Imaging.FileFormats.Jpeg2000.Jpeg2000Image.BitsPerPixel Property
- Aspose.Imaging.FileFormats.Jpeg2000.Jpeg2000Image.Comments Property
- Aspose.Imaging.FileFormats.Jpeg2000.Jpeg2000Image.Height Property
- Aspose.Imaging.FileFormats.Jpeg2000.Jpeg2000Image.RawDataFormat Property
- Aspose.Imaging.FileFormats.Jpeg2000.Jpeg2000Image.RawLineSize Property
- Aspose.Imaging.FileFormats.Jpeg2000.Jpeg2000Image.Width Property
- Aspose.Imaging.ImageOptions.Jpeg2000Options.Comments Property
### **Optimized Dithering Mechanism**
The dithering process is now more optimized and predictable. All you need to do is use the newly exposed RasterImage.Dither method instead of the creating & setting DitheringSettings and RawDitheringMethod properties. The dithering is then performed right in-place and you can then review the dithered results by loading pixels or raw data. Additionally the DitheringMethod enumeration has been moved to the Aspose.Imaging namespace.

**C#**

{{< highlight csharp >}}

 RasterImage image = (RasterImage)Image.Load(sourceFilePath);

image.Dither(DitheringMethod.FloydSteinbergDithering, 4);

{{< /highlight >}}

**Visual Basic**

{{< highlight csharp >}}

 Dim image As RasterImage = CType(Image.Load(sourceFilePath), RasterImage)

image.Dither(DitheringMethod.FloydSteinbergDithering, 4)

{{< /highlight >}}
### **Improved Creation of TiffOptions**
In order to facilitate the users and to avoid the miss-configuration of the TiffOptions instance, the Aspose.Imaging for .NET API has exposed another constructor that accepts a parameter of type TiffExpectedFormat. Based on the selected value from the TiffExpectedFormat enumeration, the API auto configures all the mandatory properties for the TiffOptions instance in order to produce the desired results. 

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

**C#**

{{< highlight csharp >}}

 //Load an image through file path location or stream

using (Image image = Image.Load(sourceFilePath))

{

    //Create an instance of TiffOptions while specifying desired format

    //Passsing TiffExpectedFormat.TiffJpegRGB will set the compression to Jpeg 

    //and BitsPerPixel according to the RGB color space

    TiffOptions options = new TiffOptions(TiffExpectedFormat.TiffJpegRGB); 

    //Save the result in Tiff format RGB with Jpeg compression

    image.Save(destinationFilePath, options);

}

{{< /highlight >}}

**Visual Basic**

{{< highlight csharp >}}

 'Load an image through file path location or stream

Using image As Image = Image.Load(sourceFilePath)

	'Create an instance of TiffOptions while specifying desired format

	'Passsing TiffExpectedFormat.TiffJpegRGB will set the compression to Jpeg 

	'and BitsPerPixel according to the RGB color space

	Dim options As New TiffOptions(TiffExpectedFormat.TiffJpegRGB)

	'Save the result in Tiff format RGB with Jpeg compression

	image.Save(destinationFilePath, options)

End Using

{{< /highlight >}}
## **Removed Classes and Properties**
### **Class Dithering.DitheringMethod Removed**
The Aspose.Imaging.Dithering.DitheringMethod class has been replaced by the Aspose.Imaging.DitheringMethod class that can be used to apply the dithering while using the RasterImage.Dither method.
### **Fields DitheringMethod.FloydSteinbergDithering & DitheringMethod.None Removed**
The enumeration fields Aspose.Imaging.Dithering.DitheringMethod.FloydSteinbergDithering and Aspose.Imaging.Dithering.DitheringMethod.None have been removed. It is advised to use the Aspose.Imaging.DitheringMethod.FloydSteinbergDithering and Aspose.Imaging.DitheringMethod.ThresholdDithering instead.
