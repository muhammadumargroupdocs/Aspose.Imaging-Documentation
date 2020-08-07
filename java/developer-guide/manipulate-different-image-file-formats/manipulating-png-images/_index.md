---
title: Manipulating PNG Images
type: docs
weight: 220
url: /java/manipulating-png-images/
---

## **Specifying Transparency for PNG Images**
One of the advantages of saving images in PNG format is that PNG can have transparent background. Aspose.Imaging for Java provides the feature for specifying transparency for the PngImage & RasterImage classes as demonstrated in the below section.

Aspose.Imaging for Java API can be used to set any color as transparent while creating new PNG images or converting existing images to PNG format. For this purposes, the Aspose.Imaging for Java API has exposed TransparentColor property and PngColorType enumeration that can be set to specify any color to be rendered as transparent in the resultant PNG image.

The below provided code snippet demonstrates how to convert an existing BMP image to PNG format by creating a PNG image from scratch while specifying the desired color as transparent.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-ManipulatingPNGImages-SpecifyTransparency-SpecifyTransparency.java" >}}


Another example that converts any loaded image directly to PNG format while specifying the transparent color is as follow.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-ManipulatingPNGImages-ConvertanyLoadedImageDirectlyToPNGformat-ConvertanyLoadedImageDirectlyToPNGformat.java" >}}
## **Compressing PNG Files**
The Portable Network Graphic (PNG) is a lossless compression format for transmitting a bitmap over networks. When you save an image as a PNG file in any program, you may be asked to choose a compression level in a range from 0 to any max level. Setting this value actually compresses the file size and does not decrease the image quality. This article describes how Aspose.Imaging APIs allows you to control the PNG file size.

Aspose.Imaging APIs can be used to set the Compression Levels for the PNG file format using the PngOptions class that has an int type CompressionLevel property. This property accepts a value from 0 to 9 where 9 is the maximum compression.

The below provided code snippet demonstrates how to set the Compression Levels using Aspose.Imaging for Java API.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-ManipulatingPNGImages-CompressingFiles-CompressingFiles.java" >}}
## **Specifying Bit Depth for PNG Images**
Bit depth in imaging is the number of bits used to indicate the color of a single pixel in a bitmap image. Like all other bitmap formats, PNG color depth is also represented in bit such as 1-bit (2 colors), 2-bit (4 colors), 4-bit (16 colors) and 8-bit (256 colors).

Aspose.Imaging for Java API can be used to set bit depth for PNG images using BitDepth property exposed by the PngOptions class. At the moment, the BitDepth property can be set to 1, 2, 4 or 8 bits for grayscale and indexed color types. For all other color types only 8 bits are supported at the moment.

The below provided code snippet demonstrates how to set the Bit Depth of an existing PNG.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-ManipulatingPNGImages-SpecifyBitDepth-SpecifyBitDepth.java" >}}
## **Applying Filter Methods on PNG Images**
Aspose.Imaging for Java provides the functionality to apply filter methods (algorithms) before compression as demonstrated in the below section. The purpose of these filter methods is to prepare the image data for optimum compression.
### **PngFilterType Enumeration**
Following are the different type of filter methods:

|**Name**|**Value**|**Description**|
| :- | :- | :- |
|Adaptive|5|Adaptive filtering, means that saving process will choose most sutable filter for each data row. Best compression, slowest execution time.|
|Avg|3|The avg filter, means, that average filter will be applied to image data.|
|None|0|The null-filter, means no filtering for image data rows.|
|Paeth|4|The paeth predictor filter.|
|Sub|1|The sub filter, means substractive filtering will be applied to image data.|
|Up|2|The up filter, means row-by-row substraction filter will be applied.|
### **Applying Filter Method on PNG Images**
Aspose.Imaging for Java API can be used to apply filter methods before compressing any PNG image. For this purposes, the Aspose.Imaging for Java API has exposed a property named FilterType of PngOptions class. It accepts PngFilterType enumeration that can be used to specify the filter method (algorithm) among the five including 0 for none. The below provided code snippet demonstrates how to apply filter method on PNG image.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-ManipulatingPNGImages-ApplyFilterMethod-ApplyFilterMethod.java" >}}
## **Changing Background Color of a Transparent PNG Image**
PNG format images can have transparent background. Aspose.Imaging for Java provides the feature to change the background color of a PNG image that has transparent background.

Aspose.Imaging for Java API can be used to set/change color of a transparent PNG image. 
The below provided code snippet demonstrates how to set/change the background color of a transparent PNG image.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-ManipulatingPNGImages-ChangeBackgroundColor-ChangeBackgroundColor.java" >}}
## **Optimizing Memory Usage**
When reading a big PNG file, the total amount of RAM the process will take is always a concern. There are measures which can be adopted to cope with the challenge. Aspose.Imaging provides some relevant options and API calls to lower, reduce and optimize memory use. Also, it can help the process work more efficiently and run faster.

The following example shows how to read a large PNG file in optimized mode.



{{< gist "aspose-com-gists" "07be292db0a393dc95f153f84b28c069" "Examples-src-main-java-com-aspose-imaging-examples-ManipulatingPNGImages-ReadLargePNGFile-ReadLargePNGFile.java" >}}




