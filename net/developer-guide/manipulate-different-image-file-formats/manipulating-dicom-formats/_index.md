---
title: Manipulating DICOM Formats
type: docs
weight: 30
url: /net/manipulating-dicom-formats/
---

## **Adjusting Brightness, Contrast and Gamma**
Color adjustments in digital images is one of the core features that most of the imaging libraries provide. Color adjustments can be categorized in the following.

1. **Brightness** refers to the lightness or darkness of color. Increasing the brightness of an image lights out all colors whereas decreasing the brightness darkens all colors.
1. **Contrast** refers to making the objects or details within an image more obvious. Increasing the contrast of an image increases the difference between light and dark areas so that the light areas becomes lighter and dark areas becomes darker. Decreasing the contrast will make lighter and darker areas stay approximately the same but the overall image becomes more homogeneous.
1. **Gamma** optimizes the contrast and brightness of the indirect lighting that is illuminating an object in the image.
### **Adjusting Brightness**
Aspose.Imaging for .NET API provide AdjustBrightness method for the DicomImage class that can be used to adjust the **Brightness** by passing an integer value as parameter.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-DICOM-AdjustBrightnessDICOM-AdjustBrightnessDICOM.cs" >}}


### **Adjusting Contrast**
The AdjustContrast method exposed by the DicomImage class can be used to adjust the **Contrast** of an image by passing a float value as parameter.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-DICOM-AdjustContrastDICOM-AdjustContrastDICOM.cs" >}}


### **Adjusting Gamma**
The AdjustGamma method exposed by the DicomImage class can be used to adjust the **Gamma** of an image by passing a float value as parameter.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-DICOM-AdjustGammaDICOM-AdjustGammaDICOM.cs" >}}


## **Applying Filters**
This article demonstrates the usage of Aspose.Imaging for .NET to apply filter on a DICOM image. Aspose.Imaging APIs have exposed efficient & easy to use methods to achieve this goal. The following code example demonstrates how to apply filter on DICOM image.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-DICOM-ApplyFilterOnDICOMImage-ApplyFilterOnDICOMImage.cs" >}}


## **Applying Binarization**
In order to understand the concept of Binarization, it is important to define a Binary Image; that is a digital image that can have only two possible values for each pixel. Normally, the two colors used for a binary image are black and white though any two colors can be used. Binarization is the process of converting an image to bi-level meaning that each pixel is stored as a single bit (0 or 1) where 0 denotes the absence of color and 1 means presence of color. Aspose.Imaging for .NET API supports three different methods of binarization for DICOM images.
### **Using Fixed Threshold**
Following code snippet demonstrates how Fixed Threshold Binarization can be applied to a DICOM image.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-BinarizationWithFixedThreshold-BinarizationWithFixedThreshold.cs" >}}


### **Using Otsu Threshold**
Following code snippet demonstrates how Otsu Threshold Binarization can be applied to a DICOM image.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-DICOM-BinarizationWithOtsuThresholdOnDICOMImage-BinarizationWithOtsuThresholdOnDICOMImage.cs" >}}


### **Using Bradley's Adaptive Threshold**
Following code snippet demonstrates how Bradley's Adaptive Threshold Binarization can be applied to a DICOM image.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-DICOM-BinarizationWithOtsuThresholdOnDICOMImage-BinarizationWithOtsuThresholdOnDICOMImage.cs" >}}


### **Using Grayscaling**
Gray-scaling is the process of converting a continuous-tone image to an image with discontinues gray shades.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-DICOM-GrayscalingOnDICOM-GrayscalingOnDICOM.cs" >}}


## **Cropping Image**
**Image cropping** usually refers to the removal of the outer parts of an image to help improve the framing. Cropping may also be used to take out some portion of an image to increase the focus on a particular area. Aspose.Imaging for .NET API now supports DICOM image cropping.
## **Cropping by Shifts**
The DicomImage class provides the Crop method that accepts 4 integer values. Based on these four values, the Crop method take out that part of the image while discarding the rest of the image. The code snippet below demonstrates how to crop a DICOM image.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-DICOM-DICOMCroppingByShifts-DICOMCroppingByShifts.cs" >}}


## **Dithering For DICOM Image**
Dithering is a technique of creating the illusion of new colors and shades by varying the pattern of dots that actually create an image. It is the most common means of reducing the color range of images down to the 256 (or fewer) colors. Aspose.Imaging provides the dithering support for DicomImage class by introducing Dither method that accepts two parameters. First is of type DitheringMethod to be applied with two possible options FloydSteinbergDithering and ThresholdDithering. The second parameter to Dither method is the BitCount in integer. BitCount defines the sampling size for the dithering result. Default value is 1 that represents black and white, whereas allowed values are 1, 4, 8 generating palettes with 2, 4 and 256 colors respectively.
## **Resizing DICOM Image**
This article demonstrates the usage of Aspose.Imaging for .NET to perform Resize operation on a DICOM image. Aspose.Imaging APIs have exposed efficient & easy to use methods to achieve this goal. Aspose.Imaging for .NET has exposed the **Resize** method of the **DicomImage** class that can be used to re-size existing images on the fly. The steps to perform Resize are as simple as below:

1. Load in image using the constructor of the **DicomImage** class.
1. Call the DicomImage.Resize method while specifying new Height & Width.
1. Save the results.
### **Simple Resizing**
The following code example demonstrates how to Resize an image.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-DICOM-DICOMSimpleResizing-DICOMSimpleResizing.cs" >}}


### **Other Resizing Options**
Aspose.Imaging API has exposed **ResizeHeightProportionally** and **ResizeWidthProportionally** methods of the **DicomImage** class that can be used to re-size the DICOM images. These methods take in an integer as first argument and **ResizeType** enumeration to achieve desired results. Below provided code snippet demonstrates the usage of these methods.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-DICOM-DICOMSOtherImageResizingOptions-DICOMSOtherImageResizingOptions.cs" >}}


## **Rotate and Flip DICOM Image**
Aspose.Imaging for .NET has provided **Rotate** and **RotateFlip** methods of **DicomImage** class to rotate/flip a DICOM image. The **DicomImage.Rotate** method can be used to rotate the image. The **Rotate** method take an integer parameter as degrees to rotate. **DicomImage.RotateFlip** method accepts a parameter of RotateFlipType that specifies the type of rotation and flip to apply to the image. The steps to perform Rotate & Flip are as simple as below:

1. Load in image using the **DicomImage** class constructor.
1. Call the **DicomImage.RotateFlip** or **DicomImage.Rotate** method while specifying the appropriate parameter.
1. Save the results.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-DICOM-RotatingDICOMImage-RotatingDICOMImage.cs" >}}

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-DICOM-FlipDICOMImage-FlipDICOMImage.cs" >}}
## **Export to DICOM**
Aspose.Imaging supports export from various raster file formats including multi-paged to DICOM. Below there are some examples related to this.

{{< gist "aspose-com-gists" "2d1bcb9853315458808ffbcd9e7e3e02" "ExportToDicom.cs" >}}
## **Support of Jpeg, Jpeg2000 and RLE compression methods in Dicom**
Dicom format can be compressed using Jpeg, Jpeg2000 and RLE compressions.
{{< gist "aspose-com-gists" "2d1bcb9853315458808ffbcd9e7e3e02" "Examples-dicom-compression-JPEG-JPEG2000-RLE.cs" >}}

## **Memory strategy optimization**
The memory optimization strategy is now supported for Dicom images.

Here are some examples of its use:

{{< gist "aspose-com-gists" "2d1bcb9853315458808ffbcd9e7e3e02" "Examples-Dicom-Memory-Strategy-Optimization.cs" >}}
