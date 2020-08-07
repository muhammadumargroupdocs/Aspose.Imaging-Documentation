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
## **Memory strategy optimization**
The memory optimization strategy is now supported for Dicom images.

Here are some examples of its use:

{{< gist "aspose-com-gists" "07be292db0a393dc95f153f84b28c069" "Examples-Dicom-Memory-Strategy-Optimization.java" >}}



