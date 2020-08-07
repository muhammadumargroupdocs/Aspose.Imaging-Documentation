---
title: Manipulating JPEG Images
type: docs
weight: 110
url: /net/manipulating-jpeg-images/
---

## **Using ExifData Class to Read and Modify Jpeg EXIF Tags**
Almost all digital cameras (including smartphones), scanners and other systems handling image save images with EXIF (Exchangeable Image File) information. Camera settings and scene information are recorded by the camera into the image file. EXIF data also include shutter speed, date and time a photo was taken, focal length, exposure compensation, metering pattern and if a flash was used. Aspose.Imaging APIs has made possible to extract the EXIF information from a given image in a very easy and simple manner. Developers may also write EXIF data to the images or modify the existing information as per their requirement. Aspose.Imaging has provided [ExifData](http://www.aspose.com/api/net/imaging/aspose.imaging.exif/exifdata) class for reading, writing and modifying the EXIF data, where as [Aspose.Imaging.Exif.Enums](http://www.aspose.com/docs/display/imagingnet/Aspose.Imaging.Exif.Enums+namespace) namespace contains the relevant enumerations used in the process.
### **Reading EXIF Data**
Aspose.Imaging APIs provide means to read EXIF data from a given image. Below provided steps illustrate the usage of [ExifData](http://www.aspose.com/api/net/imaging/aspose.imaging.exif/exifdata) class to read the EXIF information from an image.

1. Load an image into an instance of Image using the factory method Load.
1. Create and initialize an instance of [ExifData](http://www.aspose.com/api/net/imaging/aspose.imaging.exif/exifdata) class.
1. Fetch the required information and write it to console.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTags-ReadAllEXIFTags.cs" >}}



Alternatively, developers may also get the specific information using the following code snippet.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-JPEG-ReadSpecificEXIFTagsInformation-ReadSpecificEXIFTagsInformation.cs" >}}


### **Writing & Modifying EXIF Data**
Using Aspose.Imaging APIs, developers can write new EXIF information and modify existing EXIF data of an image. Both processes (Writing & Modifying) requires loading of an image and getting the EXIF data into an instance of [ExifData](http://www.aspose.com/api/net/imaging/aspose.imaging.exif/exifdata) class. Then one can access properties exposed by [ExifData](http://www.aspose.com/api/net/imaging/aspose.imaging.exif/exifdata) class to set them accordingly. Sample code to demonstrate the usage is as follow:

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-JPEG-WritingAndModifyingEXIFData-WritingAndModifyingEXIFData.cs" >}}


## **Creating Thumbnails from JPEG Images**
Thumbnails are reduced-size versions of pictures, used to display a significant part of the picture instead of the full frame. Some image files (especially the ones shot with a digital camera) have a thumbnail image embedded in the file. In such cases, Aspose.Imaging API retrieves the embedded thumbnail image and allows you to store it separately on disk. With the release of Aspose.Imaging for .NET 2.3.1, the JpegImage class contains the ExifData.Thumbnail property that can retrieve the thumbnail information from a JPEG image file. The code snippet provided below demonstrates how to use it.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-CreateThumbnailsFromJPEGImages-CreateThumbnailsFromJPEGImages.cs" >}}



Use the approach discussed above to store the thumbnail to other supported file formats. The code snipped below demonstrates using the ExifData. Thumbnail property to retrieve a thumbnail's bitmap information and copying it to a new BMP image.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-DrawingAndFormattingImages-RetrieveThumbnailBitmapInformation-RetrieveThumbnailBitmapInformation.cs" >}}



If you wish to generate thumbnails from other image formats such as BMP & PNG, please refer to the [Resizing Images](http://www.aspose.com/docs/display/imagingnet/Modifying+and+Converting+Images#ModifyingandConvertingImages-ResizingImages).
## **Adding Thumbnails to JFIF and EXIF Segments of JPEG Images**
The release of Aspose.Imaging 2.3.1 enabled developers to [create thumbnails from JPEG images](http://www.aspose.com/docs/display/imagingnet/Manipulating+JPEG+Images#ManipulatingJPEGImages-CreatingThumbnailsfromJPEGImages) using the ExifData.Thumbnail property. Starting from Aspose.Imaging 2.4.0, it is possible to add thumbnails to the JFIF and EXIF segments of JPEG images. There are additional thumbnail properties in the [ExifData](http://www.aspose.com/api/net/imaging/aspose.imaging.exif/exifdata) and Jfif classes, which are of the JpegImage type, that can can be used to store additional thumbnail images inside the original JPEG image.
### **Add Thumbnail to JFIF Segment**
The code snippet below demonstrates how to use the Jfif.Thumbnail property to add a thumbnail image to the JFIF segment of a new JPEG image.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-JPEG-AddThumbnailToJFIFSegment-AddThumbnailToJFIFSegment.cs" >}}



Thumbnail images with other segment data cannot occupy more than 65,545 bytes because of the JPEG format specifications. In cases where large images are to be set as a thumbnail, exception may arise.
### **Add Thumbnail to EXIF Segment**
The code snippet below demonstrate how to use the ExifData.Thumbnail property to add a thumbnail image to the EXIF segment of a new JPEG image.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-JPEG-AddThumbnailToJFIFSegment-AddThumbnailToJFIFSegment.cs" >}}



In this case, the Aspose.Imaging API cannot estimate the thumbnail image size, but it can check the size of the entire EXIF data segment. This cannot be bigger than 65,535 bytes.
## **Using JpegExifData Class to Read and Modify Jpeg EXIF Tags**
Aspose.Imaging APIs provide [JpegExifData](http://www.aspose.com/api/net/imaging/aspose.imaging.exif/jpegexifdata) class that is exclusive to Jpeg image formats to retrieve & update EXIF information. This article demonstrates the usage of [JpegExifData](http://www.aspose.com/api/net/imaging/aspose.imaging.exif/jpegexifdata) class to achieve the same. Aspose.Imaging.Exif.JpegExifData class serves as EXIF data container for Jpeg images, and provide means to retrieve standard Jpeg EXIF tags as demonstrated below:

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-JPEG-ReadJpegEXIFTags-ReadJpegEXIFTags.cs" >}}


### **Complete List of EXIF Tags**
The above code snippet reads a few EXIF Tags using the properties offered by Aspose.Imaging.Exif.JpegExifData class. Complete list of these properties is available [here](http://www.aspose.com/api/net/imaging/aspose.imaging.exif/jpegexifdata/properties/index). Following code will read all the EXIF tags using the System.Reflection.PropertyInfo class.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTags-ReadAllEXIFTags.cs" >}}


## **Auto Correct Orientation of JPEG Images**
Photos can be shot with a camera rotated at 90°, 180°, 270°, or none (normal orientation). Most digital cameras stores the orientation information along with the image data as EXIF tags of the JEPG images. This information can be used to perform the auto rotation on the images to correct the orientation. Aspose.Imaging APIs provides the AutoRotate method for JpegImage class to auto correct the orientation of JPEG images. Here is how you can use the AutoRotate method with Aspose.Imaging for .NET API.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-AutoCorrectOrientationOfJPEGImages-AutoCorrectOrientationOfJPEGImages.cs" >}}
## **Support for JPEG-LS**
` `Aspose.Imaging for .NET API now provide support for JPEG-LS. The code snippet below demonstrates how to use that support for JPEG-LS image and decode that and save into PNG.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-JPEG-SupportForJPEG-LSFormat-SupportForJPEG-LSFormat.cs" >}}
## **Support for JPEG-LS with CMYK and YCCK**
` `Aspose.Imaging for .NET API now provide support for CMYK and YCCK color models with JPEG-LS. The code snippet below demonstrates how to use that support for JPEG-LS.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-JPEG-SupportForJPEG-LSWithCMYK-SupportForJPEG-LSWithCMYK.cs" >}}

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-JPEG-SupportForCMYKAndYCCKColorModesInJPEGLosslessUsingRGBProfile-SupportForCMYKAndYCCKColorModesInJPEGLosslessUsingRGBProfile.cs" >}}
## **Support for 2-7 bits per sample in JPEG-LS images**
` `Aspose.Imaging for .NET API now provide support for 2-7 bits per sample JPEG-LS images. The code snippet below demonstrates how to use that support for JPEG-LS.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-JPEG-SupportFor2-7BitsJPEG-SupportFor2-7BitsJPEG.cs" >}}
## **Setting ColorType and CompressionType for JPEG images**
` `Aspose.Imaging for .NET API now provide support for Color Type and compression Type and set them as gray scale and progressive for JPEG images. The code snippet below demonstrates how to use that support.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-JPEG-ColorTypeAndCompressionType-ColorTypeAndCompressionType.cs" >}}
## **Convert TIFF to JPEG image**
Using Aspose.Imaging for .NET, developers can convert TIFF to JPEG format. This topic explains the approach to load existing TIFF image and convert it to JPEG using **JpegOptions** class.

The steps to convert TIFF image to JPEG are as simple as below:

- Create an instance of the TiffImage and load image using Load method of Image class
- Iterate over the collection of frames of type TiffFrame
- Create an instance of JpegOptions class and set ResolutionSettings
- Set the resolution unit explicitly
- Call TiffFrame.Save method with destination path and an instance JpegOptions

Below provided sample code demonstrate how to convert TIFF to JPEG.

{{< gist "aspose-com-gists" "2d1bcb9853315458808ffbcd9e7e3e02" "Examples-CSharp-ModifyingAndConvertingImages-JPEG-ConvertTIFFToJPEG-ConvertTIFFToJPEG.cs" >}}
## **Memory Strategy optimization**
Loading and creating of JPEG images can be proceeded using memory strategy optimization - ie limiting memory buffer size for operation.

{{< gist "aspose-com-gists" "2d1bcb9853315458808ffbcd9e7e3e02" "MemoryStrategyOptimizationJPEG.cs" >}}
