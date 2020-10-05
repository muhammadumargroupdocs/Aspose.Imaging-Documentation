---
title: Manipulating DICOM Formats
type: docs
weight: 120
url: /java/manipulating-dicom-formats/
---

## **Adjusting Brightness, Contrast and Gamma**
Color adjustments in digital images is one of the core features that most of the imaging libraries provide. Color adjustments can be categorized in the following.

1. **Brightness** refers to the lightness or darkness of color. Increasing the brightness of an image lights out all colors whereas decreasing the brightness darkens all colors.
1. **Contrast** refers to making the objects or details within an image more obvious. Increasing the contrast of an image increases the difference between light and dark areas so that the light areas becomes lighter and dark areas becomes darker. Decreasing the contrast will make lighter and darker areas stay approximately the same but the overall image becomes more homogeneous.
1. **Gamma** optimizes the contrast and brightness of the indirect lighting that is illuminating an object in the image.
### **Adjusting Brightness**
Aspose.Imaging for Java API provide adjustBrightness method for the DicomImage class that can be used to adjust the **Brightness** by passing an integer value as parameter.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-dicom-AdjustingBrightness-AdjustingBrightness.java" >}}
### **Adjusting Contrast**
The adjustContrast method exposed by the DicomImage class can be used to adjust the **Contrast** of an image by passing a float value as parameter.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-dicom-AdjustingContrast-AdjustingContrast.java" >}}
### **Adjusting Gamma**
The adjustGamma method exposed by the DicomImage class can be used to adjust the **Gamma** of an image by passing a float value as parameter.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-dicom-AdjustingGamma-AdjustingGamma.java" >}}
## **Applying Filters**
This article demonstrates the usage of Aspose.Imaging for Java to apply filter on a DICOM image. Aspose.Imaging APIs have exposed efficient & easy to use methods to achieve this goal.

The following code example demonstrates how to apply filter on DICOM image.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-dicom-ApplyFilterOnDICOMImage-ApplyFilterOnDICOMImage.java" >}}
## **Applying Binarization**
In order to understand the concept of Binarization, it is important to define a Binary Image; that is a digital image that can have only two possible values for each pixel. Normally, the two colors used for a binary image are black and white though any two colors can be used. Binarization is the process of converting an image to bi-level meaning that each pixel is stored as a single bit (0 or 1) where 0 denotes the absence of color and 1 means presence of color.
### **Using Fixed Threshold**
Following code snippet demonstrates how Fixed Threshold Binarization can be applied to a DICOM image.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-dicom-BinarizationwithFixedThreshold-BinarizationwithFixedThreshold.java" >}}
### **Using Otsu Threshold**
Following code snippet demonstrates how Otsu Threshold Binarization can be applied to a DICOM image.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-dicom-BinarizationwithOtsuThreshold-BinarizationwithOtsuThreshold.java" >}}
### **Using Bradley's Adaptive Threshold**
Following code snippet demonstrates how Bradley's Adaptive Threshold Binarization can be applied to a DICOM image.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-dicom-BinarizationwithOtsuThreshold-BinarizationwithOtsuThreshold.java" >}}
### **Using Grayscaling**
Gray-scaling is the process of converting a continuous-tone image to an image with discontinues gray shades.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-dicom-Grayscaling-Grayscaling.java" >}}
## **Cropping Image**
**Image cropping** usually refers to the removal of the outer parts of an image to help improve the framing. Cropping may also be used to take out some portion of an image to increase the focus on a particular area. Aspose.Imaging for Java API now supports DICOM image cropping.
## **Cropping by Shifts**
**Image cropping** usually refers to the removal of the outer parts of an image to help improve the framing. Cropping may also be used to take out some portion of an image to increase the focus on a particular area.

Aspose.Imaging for Java API now supports DICOM image cropping.

The DicomImage class provides the Crop method that accepts 4 integer values. Based on these four values, the Crop method take out that part of the image while discarding the rest of the image.
### **Programming Sample**
The code snippet below demonstrates how to crop a DICOM image.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-dicom-CropbyShifts-CropbyShifts.java" >}}
## **Dithering For DICOM Image**
Dithering is a technique of creating the illusion of new colors and shades by varying the pattern of dots that actually create an image. It is the most common means of reducing the color range of images down to the 256 (or fewer) colors.
### **Dithering**
Aspose.Imaging provides the dithering support for DicomImage class by introducing Dither method that accepts two parameters. First is of type DitheringMethod to be applied with two possible options FloydSteinbergDithering and ThresholdDithering. The second parameter to Dither method is the BitCount in integer.

{{% alert color="primary" %}} 

BitCount defines the sampling size for the dithering result. Default value is 1 that represents black and white, whereas allowed values are 1, 4, 8 generating palettes with 2, 4 and 256 colors respectively.

{{% /alert %}} 

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-dicom-DitheringForDICOMImage-DitheringForDICOMImage.java" >}}
## **Resizing DICOM Image**
This article demonstrates the usage of Aspose.Imaging for Java to perform Resize operation on a DICOM image. Aspose.Imaging APIs have exposed efficient & easy to use methods to achieve this goal.
### **Resizing Image**
Aspose.Imaging for Java has exposed the **Resize** method of the **DicomImage** class that can be used to re-size existing images on the fly.

The steps to perform Resize are as simple as below:

1. Load in image using the constructor of the **DicomImage** class.
1. Call the DicomImage.Resize method while specifying new Height & Width.
1. Save the results.
#### **Simple Resizing**
The following code example demonstrates how to Resize an image.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-dicom-SimpleResizing-SimpleResizing.java" >}}
### **Other Image Resizing Options**
Aspose.Imaging API has exposed **ResizeHeightProportionally** and **ResizeWidthProportionally** methods of the **DicomImage** class that can be used to re-size the DICOM images. These methods take in an integer as first argument and **ResizeType** enumeration to achieve desired results.

Below provided code snippet demonstrates the usage of these methods.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-dicom-ResizeHeightProportionally-ResizeHeightProportionally.java" >}}

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-dicom-ResizeWidthProportionally-ResizeWidthProportionally.java" >}}
## **Rotate and Flip DICOM Image**
Aspose.Imaging for Java has provided **Rotate** and **RotateFlip** methods of **DicomImage** class to rotate/flip a DICOM image.
### **Rotating an Image**
The **DicomImage.Rotate** method can be used to rotate the image. The **Rotate** method take an integer parameter as degrees to rotate. **DicomImage.RotateFlip** method accepts a parameter of RotateFlipType that specifies the type of rotation and flip to apply to the image.

The steps to perform Rotate & Flip are as simple as below:

1. Load in image using the **DicomImage** class constructor.
1. Call the **DicomImage.RotateFlip** or **DicomImage.Rotate** method while specifying the appropriate parameter.
1. Save the results.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-dicom-RotateDICOMImage-RotateDICOMImage.java" >}}
### **Fliping an Image**
{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-dicom-FlipDICOMImage-FlipDICOMImage.java" >}}
## **Export to DICOM**
Aspose.Imaging supports export from various raster file formats including multi-paged to DICOM. Below there are some examples related to this.

{{< gist "aspose-com-gists" "07be292db0a393dc95f153f84b28c069" "ExportToDicom.java" >}}

## **Support of Jpeg, Jpeg2000 and RLE compression methods in Dicom**
Dicom format can be compressed using Jpeg, Jpeg2000 and RLE compressions.

### What is a DICOM Image File?
The DICOM standard is useful for integrating all modern imaging equipments, accessories, networking servers, workstations and printers. Because of its ease of integration and continuous evolution this communication standard has over the years achieved a nearly universal level of acceptance among vendors of radiological equipment.

A DICOM image file is an outcome of the Digital Imaging and Communications in Medicine standard. Specifically, image files that are compliant with part 10 of the DICOM standard are generally referred to as “DICOM format files” or simply “DICOM files” and are represented as “.dcm”.

### DICOM compression settings
The property ***DicomOptions.Compression*** allows you to specify compression settings. For instance, ***CompressionType*** enumeration allows you to select compression algorithm: *None*, *Jpeg*, *Jpeg2000* or *Rle*. The *None* option corresponds to uncompressed DICOM image. The following code shows how to use DICOM compression settings:

{{< gist "aspose-com-gists" "07be292db0a393dc95f153f84b28c069" "Examples-dicom-no-compression.java" >}}

### Using JPEG compression in DICOM image
To use JPEG compression algorithm you should specify *CompressionType.Jpeg* enumeration value in ***Compression.Type*** property:

{{< gist "aspose-com-gists" "07be292db0a393dc95f153f84b28c069" "Examples-dicom-jpeg-compression.java" >}}

You can tune JPEG compression algorithm using ***Compression.Jpeg*** property. For instance, you can specify the *CompressionType*, *SampleRoundingMode* and *Quality*:

{{< gist "aspose-com-gists" "07be292db0a393dc95f153f84b28c069" "Examples-dicom-jpeg-tuned-compression.java" >}}

### Using JPEG 2000 compression in DICOM image
To use JPEG 2000 compression you need to use *CompressionType.Jpeg2000* enumeration value and ***Jpeg2000Options*** class for algorithm settings. The following code demonstrates how to specify JPEG 2000 *Codec* and *Irreversible* properties:

{{< gist "aspose-com-gists" "07be292db0a393dc95f153f84b28c069" "Examples-dicom-jpeg2000-compression.java" >}}

### Using RLE compression in DICOM image
For this compression type you need to use *CompressionType.Rle* enumeration value. The RLE compression algorithm doesn't have additional settings. The following code shows how you can use RLE compression algorithm in DICOM image:

{{< gist "aspose-com-gists" "07be292db0a393dc95f153f84b28c069" "Examples-dicom-rle-compression.java" >}}

### How to change Color Type in DICOM compression
The property ***DicomOptions.ColorType*** allows you to change color type in DICOM compression. There are several supported color types: *Grayscale8Bit*, *Grayscale16Bit* and *Rgb24Bit*. Use the following code in order to change the color type:

{{< gist "aspose-com-gists" "07be292db0a393dc95f153f84b28c069" "Examples-dicom-grayscale.java" >}}

## **Memory strategy optimization**
The memory optimization strategy is now supported for Dicom images.

Here are some examples of its use:

{{< gist "aspose-com-gists" "07be292db0a393dc95f153f84b28c069" "Examples-Dicom-Memory-Strategy-Optimization.java" >}}



