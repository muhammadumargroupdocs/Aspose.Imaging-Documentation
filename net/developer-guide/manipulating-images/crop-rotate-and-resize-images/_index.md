---
title: Crop, Rotate and Resize Images
type: docs
weight: 50
url: /net/crop-rotate-and-resize-images/
---

## **Cropping Images**
**Image cropping** usually refers to the removal of the outer parts of an image to help improve the framing. Cropping may also be used for to cut out some portion of an image to increase the focus on a particular area. From Aspose.Imaging 2.3.0, the API supports two different approaches to image cropping: by [shifts](http://www.aspose.com/docs/display/imagingnet/Crop%2C+Rotate+and+Resize+Images#Crop%2CRotateandResizeImages-CroppingbyShifts) and [rectangle](http://www.aspose.com/docs/display/imagingnet/Crop%2C+Rotate+and+Resize+Images#Crop%2CRotateandResizeImages-CroppingbyRectangle).
### **Cropping by Shifts**
The [RasterImage](http://www.aspose.com/api/net/imaging/aspose.imaging/rasterimage) class provides an overloaded version of the [Crop](http://www.aspose.com/api/net/imaging/aspose.imaging/rasterimage/methods/crop/index) method that accepts 4 integer values denoting Left, Right, Top & Bottom. Based on these four values, the [Crop](http://www.aspose.com/api/net/imaging/aspose.imaging/rasterimage/methods/crop/index) method moves the image boundaries toward the center of the image while discarding the outer portion. The code snippet below demonstrates how to crop an image by shifts.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-JPEG-CroppingByShifts-CroppingByShifts.cs" >}}


### **Cropping by Rectangle**
The [RasterImage](http://www.aspose.com/api/net/imaging/aspose.imaging/rasterimage) class provides another overloaded version of the [Crop](http://www.aspose.com/api/net/imaging/aspose.imaging/rasterimage/methods/crop/index) method that accepts an instance of the [Rectangle](http://www.aspose.com/api/net/imaging/aspose.imaging/rectangle) class. You can cut out any portion of an image by providing the desired boundaries to the [Rectangle](http://www.aspose.com/api/net/imaging/aspose.imaging/rectangle) object. The code snippet below demonstrates how to Crop any image by Rectangle.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-JPEG-CroppingByRectangle-CroppingByRectangle.cs" >}}


## **Rotate and Flip an Image**
Aspose.Imaging for .NET is an easy to use library because it provides simple methods to perform complex operations while encapsulating all ugly details. For instance, Aspose.Imaging for .NET has provided [RotateFlip](http://www.aspose.com/api/net/imaging/aspose.imaging/image/methods/rotateflip) method for it's base class [Image](http://www.aspose.com/api/net/imaging/aspose.imaging/image) if an application requires rotating an image. Irrespective of the image format, the library can perform specific **Rotate & Flip** procedure on it.
### **Rotating an Image**
The Image.RotateFlip method can be used to rotate the image by 90/180/270-degrees and flip the image horizontally or vertically. Image.RotateFlip method accepts a parameter of [RotateFlipType](http://www.aspose.com/api/net/imaging/aspose.imaging/rotatefliptype) that specifies the type of rotation and flip to apply to the image. The steps to perform **Rotate & Flip** are as simple as below,

1. Load in image using the factory method [Load](http://www.aspose.com/api/net/imaging/aspose.imaging/image/methods/load/index) exposed by [Image](http://www.aspose.com/api/net/imaging/aspose.imaging/image) class.
1. Call the Image.RotateFlip method while specifying the appropriate [RotateFlipType](http://www.aspose.com/api/net/imaging/aspose.imaging/rotatefliptype).
1. Save the results.

The following code example demonstrates how to set the [RotateFlip](http://www.aspose.com/api/net/imaging/aspose.imaging/image/methods/rotateflip) property of an [Image](http://www.aspose.com/api/net/imaging/aspose.imaging/image) and the [RotateFlipType](http://www.aspose.com/api/net/imaging/aspose.imaging/rotatefliptype) enumeration.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-JPEG-RotatingAnImage-RotatingAnImage.cs" >}}



**RotateFlipType Enumeration**

Members of [RotateFlipType](http://www.aspose.com/api/net/imaging/aspose.imaging/rotatefliptype) enumeration and their details are [available here](http://www.aspose.com/api/net/imaging/aspose.imaging/rotatefliptype).
## **Rotating an Image on a Specific Angle**
From version 2.5.0, the Aspose.Imaging for .NET API has exposed the RasterImage.Rotate method to facilitate its users who wish to rotate an image on a specific angle. Unlike the [RasterImage.RotateFlip](http://www.aspose.com/api/net/imaging/aspose.imaging/image/methods/rotateflip) method, the RasterImage.Rotate method accepts three parameters:

1. Rotation angle: A float type parameter that specifies the rotation angle to which the image has to be rotated. A positive value rotates the image clockwise; a negative value performs an anticlockwise rotation.
1. Resize proportionally: A Boolean type parameter specifies if the image size has to changed according to the rotated rectangle (corner points) projections. If set to false, the image dimensions would be untouched and only internal image contents are rotated.
1. Background color: A Color type parameter specifies the color to be filled in the background of the rotated image.

The code snippet below demonstrates the usage of RasterImage.Rotate method.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-RotatingImageOnSpecificAngle-RotatingImageOnSpecificAngle.cs" >}}



From version 2.5.0, the Aspose.Imaging for .NET API has exposed the RasterImage.Rotate method to facilitate its users who wish to rotate an image on a specific angle.
## **Resizing Images**
This article demonstrates the usage of Aspose.Imaging for .NET to perform **Resize** operation on an image. Aspose.Imaging APIs have exposed efficient & easy to use methods to achieve this goal. Aspose.Imaging for .NET has exposed the Resize method for the [Image](http://www.aspose.com/api/net/imaging/aspose.imaging/image) class that can be used to re-size existing images on the fly. There are two overloads of the Resize method to suit the application needs.
### **Resizing Images : Simple Resizing**
The steps to perform **Resize** are as simple as below,

1. Load in image using the factory method [Load](http://www.aspose.com/api/net/imaging/aspose.imaging/image/methods/load/index) exposed by [Image](http://www.aspose.com/api/net/imaging/aspose.imaging/image) class.
1. Call the Image.Resize method while specifying new Height & Width.
1. Save the results.

The following code example demonstrates how to Resize an image.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-SimpleResizing-SimpleResizing.cs" >}}


### **Resizing Images : Resizing with ResizeType Enumeration**
Aspose.Imaging API has exposed [ResizeType enumeration](http://www.aspose.com/api/net/imaging/aspose.imaging/resizetype) that can be used with Image.Resize to achieve desired results. Below provided code snippet demonstrates the usage of [ResizeType enumeration](http://www.aspose.com/api/net/imaging/aspose.imaging/resizetype), whereas the details of [ResizeType enumeration](http://www.aspose.com/api/net/imaging/aspose.imaging/resizetype) members can be found at the bottom of this page.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-ResizingWithResizeTypeEnumeration-ResizingWithResizeTypeEnumeration.cs" >}}



If you intend to get quality result after applying the re-size then it is suggested that you should always use ResizeType.LanczosResample because it will output highly qualitative results but may work slower than ResizeType.NearestNeighbourResample. On the other hand, ResizeType.NearestNeighbourResample algorithm is specifically used for fast re-sizing while compromising on the image quality. This method may be useful for thumbnail generation in real time or similar processes where performance is required.
### **Resizing Images : ResizeType Enumeration**
ResizeType determines the type of re-sizing to be performed on the image based on the selected filter.

Members of ResizeType Enumeration

|**Member Name**|**Value**|**Description**|
| :- | :- | :- |
|LeftTopToLeftTop|0|Left top point of the new image will coincide with the left top point of the original image. Crop will occur if required.|
|RightTopToRightTop|1|Right top point of the new image will coincide with the right top point of the original image. Crop will occur if required.|
|RightBottomToRightBottom|2|Right bottom point of the new image will coincide with the right bottom point of the original image. Crop will occur if required.|
|LeftBottomToLeftBottom|3|Left bottom point of the new image will coincide with the left bottom point of the original image. Crop will occur if required.|
|CenterToCenter|4|Center of the new image will coincide with the center of the original image. Crop will occur if required.|
|LancrosResample|5|Resample using lancros algorithm using 7x7 mask.|
|NearestNeighbourResample|6|Resample using nearest neighbour algorithm.|
### **Resizing Images : Svg native resize**
{{< gist "aspose-com-gists" "2d1bcb9853315458808ffbcd9e7e3e02" "SvgNativeResize.cs" >}}
## **Resize Image Proportionally**
You can [resize images]() by passing new height & width values as parameters to the Image.Resize method but in that case you have to calculate the aspect ratio yourself. This is because when the width or height of an image is altered, the image is either scaled or shrinked to fill the new size . If the changes to the width and height of an image are not in proportion this can lead to stretched and distorted result. This article demonstrates the use of Aspose.Imaging for .NET API to resize images by passing either new height or width while allowing the API to automatically calculate the other proportional value.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-SimpleResizeImageProportionally-SimpleResizeImageProportionally.cs" >}}


### **Resize Image Proportionally**
Aspose.Imaging for .NET has exposed the [ResizeWidthProportionally](http://www.aspose.com/api/net/imaging/aspose.imaging/image/methods/resizewidthproportionally/index) and [ResizeHeightProportionally](http://www.aspose.com/api/net/imaging/aspose.imaging/image/methods/resizeheightproportionally/index) methods for the [Image](http://www.aspose.com/api/net/imaging/aspose.imaging/image) class that can be used to re-size existing images on the fly while keeping the aspect ratio.
### **Simple Resizing**
The following code example demonstrates the use of [ResizeWidthProportionally](http://www.aspose.com/api/net/imaging/aspose.imaging/image/methods/resizewidthproportionally/index) and [ResizeHeightProportionally](http://www.aspose.com/api/net/imaging/aspose.imaging/image/methods/resizeheightproportionally/index) methods.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-SimpleResizeImageProportionally-SimpleResizeImageProportionally.cs" >}}


### **Resizing with ResizeType Enumeration**
Aspose.Imaging for .NET API has also exposed overload versions of the [ResizeWidthProportionally](http://www.aspose.com/api/net/imaging/aspose.imaging/image/methods/resizewidthproportionally/index) and [ResizeHeightProportionally](http://www.aspose.com/api/net/imaging/aspose.imaging/image/methods/resizeheightproportionally/index) methods that can accept ResizeType as second parameter to achieve desired results. Below provided code snippet demonstrates the usage of [ResizeType enumeration](http://www.aspose.com/api/net/imaging/aspose.imaging/resizetype), whereas the details of [ResizeType enumeration](http://www.aspose.com/api/net/imaging/aspose.imaging/resizetype) members can be found at the bottom of this page.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-ResizeImageWithResizeTypeEnumeration-ResizeImageWithResizeTypeEnumeration.cs" >}}


### **ResizeType Enumeration**
ResizeType determines the type of re-sizing to be performed on the image based on the selected filter.
### **Members of ResizeType Enumeration**

|**Member Name**|**Value**|**Description**|
| :- | :- | :- |
|LeftTopToLeftTop|0|Left top point of the new image will coincide with the left top point of the original image. Crop will occur if required.|
|RightTopToRightTop|1|Right top point of the new image will coincide with the right top point of the original image. Crop will occur if required.|
|RightBottomToRightBottom|2|Right bottom point of the new image will coincide with the right bottom point of the original image. Crop will occur if required.|
|LeftBottomToLeftBottom|3|Left bottom point of the new image will coincide with the left bottom point of the original image. Crop will occur if required.|
|CenterToCenter|4|Center of the new image will coincide with the center of the original image. Crop will occur if required.|
|LancrosResample|5|Resample using lancros algorithm using 7x7 mask.|
|NearestNeighbourResample|6|Resample using nearest neighbour algorithm.|
If you intend to get quality result after applying the re-size then it is suggested that you should always use ResizeType.LanczosResample because it will output highly qualitative results but may work slower than ResizeType.NearestNeighbourResample. On the other hand, ResizeType.NearestNeighbourResample algorithm is specifically used for fast re-sizing while compromising on the image quality. This method may be useful for thumbnail generation in real time or similar processes where performance is required.
