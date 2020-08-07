---
title: Crop, Rotate and Resize Images
type: docs
weight: 60
url: /java/crop-rotate-and-resize-images/
---


## **Crop Images**
**Image cropping** usually refers to the removal of the outer parts of an image to help improve the framing. Cropping may also be used for to cut out some portion of an image to increase the focus on a particular area.

From Aspose.Imaging for Java 2.4.0, the API supports two different approaches to image cropping: by [shifts](/imaging/java/crop-2c-rotate-and-resize-images-html/) and [rectangle](/imaging/java/crop-2c-rotate-and-resize-images-html/).
### **Crop by Shifts**
The RasterImage class provides an overload of the crop method that accepts 4 integer values denoting Left, Right, Top & Bottom. Based on these four values, the crop method moves the image boundaries toward the center of the image while discarding the outer portion.

The code snippet below demonstrates how to crop an image by shifts.



{{< gist "aspose-com-gists" "07be292db0a393dc95f153f84b28c069" "Examples-src-main-java-com-aspose-imaging-examples-metafile-CropbyShifts-CropbyShifts.java" >}}
### **Crop by Rectangle**
The RasterImage class provides another overloaded version of the crop method that accepts an instance of the Rectangle class. You can cut out any portion of an image by providing the desired boundaries to the Rectangle object.

The code snippet below demonstrates how.



{{< gist "aspose-com-gists" "07be292db0a393dc95f153f84b28c069" "Examples-src-main-java-com-aspose-imaging-examples-metafile-CropbyRectangle-CropbyRectangle.java" >}}
## **Rotate and Flip an Image**
Aspose.Imaging for Java is an easy to use API because it provides simple routines to perform complex operations while hiding ugly details from it's users. In order to perform a **Rotate & Flip** procedure on an image, the Aspose.Imaging for Java API has provided the rotateFlip method for the base class Image.

**Rotating an Image**

Image.rotateFlip method can be used to rotate the image by 90/180/270-degrees or flip the image horizontally or vertically. Image.rotateFlip method accepts a parameter of RotateFlipType that specifies the type of rotation and flip to apply to the image.

The steps to perform **Rotate & Flip** are as simple as below,

1. Load in image using the factory method load exposed by Image class.
1. Call the Image.rotateFlip method while specifying the appropriate RotateFlipType.
1. Save the results.

The following code example demonstrates how to set the rotateFlip property of an Image and the RotateFlipType enumeration.



{{< gist "aspose-com-gists" "07be292db0a393dc95f153f84b28c069" "Examples-src-main-java-com-aspose-imaging-examples-ModifyingImages-RotatingAnImage-RotatingAnImage.java" >}}



**RotateFlipType Enumeration**

Members of RotateFlipType class and their details are outlined as follow.

|**Member**|**Description**|
| :- | :- |
|**Rotate180FlipNone**|Specifies a 180-degree clockwise rotation without flipping.|
|**Rotate180FlipX**|Specifies a 180-degree clockwise rotation followed by a horizontal flip.|
|**Rotate180FlipXY**|Specifies a 180-degree clockwise rotation followed by a horizontal and vertical flip.|
|**Rotate180FlipY**|Specifies a 180-degree clockwise rotation followed by a vertical flip.|
|**Rotate270FlipNone**|Specifies a 270-degree clockwise rotation without flipping.|
|**Rotate270FlipX**|Specifies a 270-degree clockwise rotation followed by a horizontal flip.|
|**Rotate270FlipXY**|Specifies a 270-degree clockwise rotation followed by a horizontal and vertical flip.|
|**Rotate270FlipY**|Specifies a 270-degree clockwise rotation followed by a vertical flip.|
|**Rotate90FlipNone**|Specifies a 90-degree clockwise rotation without flipping.|
|**Rotate90FlipX**|Specifies a 90-degree clockwise rotation followed by a horizontal flip.|
|**Rotate90FlipXY**|Specifies a 90-degree clockwise rotation followed by a horizontal and vertical flip.|
|**Rotate90FlipY**|Specifies a 90-degree clockwise rotation followed by a vertical flip.|
|**RotateNoneFlipNone**|Specifies no rotation and no flipping.|
|**RotateNoneFlipX**|Specifies no rotation followed by a horizontal flip.|
|**RotateNoneFlipXY**|Specifies no rotation followed by a horizontal and vertical flip.|
|**RotateNoneFlipY**|Specifies no rotation followed by a vertical flip.|
## **Rotate an Image on a Specific Angle**
From version 2.5.0, the Aspose.Imaging for Java API has exposed the RasterImage.Rotate method to facilitate its users who wish to rotate an image on a specific angle.

Unlike the [RasterImage.RotateFlip](http://www.aspose.com/api/java/imaging/aspose.imaging/image/methods/rotateflip) method, the RasterImage.Rotate method accepts three parameters:

1. Rotation angle: A float type parameter that specifies the rotation angle to which the image has to be rotated. A positive value rotates the image clockwise; a negative value performs an anticlockwise rotation.
1. Resize proportionally: A Boolean type parameter specifies if the image size has changed according to the rotated rectangle (corner points) projections. If set to false, the image dimensions would be untouched and only internal image contents are rotated.
1. Background color: A Color type parameter specifies the color to be filled in the background of the rotated image.

The code snippet below demonstrates the usage of RasterImage.Rotate method.



{{< gist "aspose-com-gists" "07be292db0a393dc95f153f84b28c069" "Examples-src-main-java-com-aspose-imaging-examples-ModifyingImages-RotatingImageOnSpecificAngle-RotatingImageOnSpecificAngle.java" >}}
## **Resize Images**
This article demonstrates the usage of Aspose.Imaging APIs to perform the **Resize** operation on an image. Aspose.Imaging APIs have exposed efficient & easy to use methods to achieve this goal.

Aspose.Imaging for Java has exposed the resize method for the Image class that can be used to re-size existing images on the fly. There are two overloads of the resize method to suit the application needs.

The steps to perform **Resize** are as simple as below,

1. Load in image using the factory method load exposed by Image class.
1. Call the Image.resize method while specifying new Height & Width.
1. Save the results.

**Simple Resize**

The following code example demonstrates how to resize an image.



{{< gist "aspose-com-gists" "07be292db0a393dc95f153f84b28c069" "Examples-src-main-java-com-aspose-imaging-examples-ModifyingImages-SimpleResizing-SimpleResizing.java" >}}
### **Resize with ResizeType Enumeration**
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
{{< gist "aspose-com-gists" "07be292db0a393dc95f153f84b28c069" "Examples-src-main-java-com-aspose-imaging-examples-ModifyingImages-ResizeImageWidthwithResizeTypeEnumeration-ResizeImageWidthwithResizeTypeEnumeration.java" >}}

{{% alert color="primary" %}} 

If you intend to get a quality result after applying the re-size then it is suggested that you should always use ResizeType.LanczosResample because it will output highly qualitative results but may work slower than ResizeType.NearestNeighbourResample. On the other hand, ResizeType.NearestNeighbourResample algorithm is specifically used for fast re-sizing while compromising on the image quality. This method may be useful for thumbnail generation in real time or similar processes where performance is required.

{{% /alert %}} 
### **Resizing Images : Svg native resize**
## **Resize Image Proportionally**
You can [resize images](/pages/createpage.action?spaceKey=imagingjava&title=Resizing+Images&linkCreation=true&fromPageId=15303063) by passing the new height & width values as parameters to the Image.resize method but in that case you have to calculate the aspect ratio yourself. This is because when the width or height of an image is altered, the image either scales or shrinks to fill the new size. If the changes to the width and height of an image are not in proportion this can lead to stretched and distorted result.

This article demonstrates the use of Aspose.Imaging for Java API to resize images by passing either new height or width while allowing the API to automatically calculate the other proportional value.

Aspose.Imaging for Java has exposed the resizeWidthProportionally and resizeHeightProportionally methods for the Image class that can be used to re-size existing images on the fly while keeping the aspect ratio.

**Simple Resize**

The following code example demonstrates the use of resizeWidthProportionally and resizeHeightProportionally methods.



{{< gist "aspose-com-gists" "07be292db0a393dc95f153f84b28c069" "Examples-src-main-java-com-aspose-imaging-examples-ModifyingImages-SimpleResizeImageProportionally-SimpleResizeImageProportionally.java" >}}
### **Implement Lossy GIF Compressor**
Using Aspose.Imaging for Java, developers can sets pixel difference. GIF's compression is based on a "dictionary" of strings of pixels seen. Normal encoder searches the dictionary for the longest string of pixels that exactly matches pixels in the image. Lossy encoder picks longest string of pixels that's "similar enough" to pixels in the image. Below is the code demonstration of the said functionality.



{{< gist "aspose-com-gists" "07be292db0a393dc95f153f84b28c069" "Examples-src-main-java-com-aspose-imaging-examples-ModifyingImages-ResizeImageWidthwithResizeTypeEnumeration-ResizeImageWidthwithResizeTypeEnumeration.java" >}}
### **Resize Proportionally with ResizeType Enumeration**
Aspose.Imaging for Java API has also exposed overload versions of the resizeWidthProportionally and resizeHeightProportionally methods that can accept ResizeType as second parameter to achieve desired results. Below provided code snippet demonstrates the usage of ResizeType enumeration, whereas the details of ResizeType enumeration members can be found at the bottom of this page.



{{< gist "aspose-com-gists" "07be292db0a393dc95f153f84b28c069" "Examples-src-main-java-com-aspose-imaging-examples-ModifyingImages-ResizeImageWidthwithResizeTypeEnumeration-ResizeImageWidthwithResizeTypeEnumeration.java" >}}



**ResizeType Enumeration**

ResizeType determines the type of re-sizing to be performed on the image based on the selected filter.

**Members of ResizeType Enumeration**

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
