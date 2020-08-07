---
title: Manipulating JPEG Images
type: docs
weight: 190
url: /java/manipulating-jpeg-images/
---

## **Using ExifData Class to Read and Modify Jpeg EXIF Tags**
Almost all digital cameras (including smartphones), scanners and other systems handling image save images with EXIF (Exchangeable Image File) information. EXIF data segments contain useful information about the camera settings and scene, that is recorded by the camera into the image file. EXIF data also include shutter speed, date and time a photo was taken, focal length, exposure compensation, metering pattern and if a flash was used.

Aspose.Imaging APIs has made possible to extract the EXIF information from a given image in a very easy and simple manner. Developers may also write EXIF data to the images or modify the existing information as per their requirement. Aspose.Imaging has provided ExifData class for reading, writing and modifying the EXIF data, where as com.aspose.imaging.exif.enums package contains the relevant enumerations used in the process.
### **Reading EXIF Data**
Aspose.Imaging APIs provide means to read EXIF data from a given image. Below provided steps illustrate the usage of ExifData class to read the EXIF information from an image.

1. Load an image into an instance of Image using the factory method load.
1. Create an initialize an instance of ExifData class.
1. Fetch the required information.

The following piece of code demonstrates the usage of ExifData class to get the specific EXIF information from a JPEG image.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-ManipulatingJPEGImages-ReadJpegEXIFTags-ReadJpegEXIFTags.java" >}}
### **Writing & Modifying EXIF Data**
Using Aspose.Imaging APIs, developers can write new EXIF information and modify existing EXIF data of an image. Both processes (Writing & Modifying) requires loading of an image and getting the EXIF data into an instance of ExifData class. Then one can access properties exposed by ExifData class to set them accordingly.

Sample code to demonstrate the usage is as follow.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-ManipulatingJPEGImages-WritingAndModifyingEXIFData-WritingAndModifyingEXIFData.java" >}}
## **Creating Thumbnails from JPEG Images**
Thumbnails are reduced-size versions of pictures, used to display a significant part of the picture instead of the full frame. Some image files (especially the ones shot with a digital camera) have a thumbnail image embedded in the file. In such cases, Aspose.Imaging API retrieves the embedded thumbnail image and allows you to store it separately on disk.
### **Creating Thumbnails from JPEG Images**
With the release of Aspose.Imaging for Java 2.4.0, the JpegImage class contains the ExifData.Thumbnail property that allows to retrieve the thumbnail information from a JPEG image file.

The code snippet provided below demonstrates how to use it.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-ManipulatingJPEGImages-WritingAndModifyingEXIFData-WritingAndModifyingEXIFData.java" >}}



Use the approach discussed above to store the thumbnail to other supported file formats. The code snipped below demonstrates using the ExifData.Thumbnail property to retrieve a thumbnail's bitmap information and copying it to a new BMP image.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-ManipulatingJPEGImages-RetrieveThumbnailBitmapInformation-RetrieveThumbnailBitmapInformation.java" >}}

{{% alert color="primary" %}} 

If you wish to generate thumbnails from other image formats such as BMP & PNG, please refer to the [Resizing Images](/pages/createpage.action?spaceKey=imagingjava&title=Resizing+Images&linkCreation=true&fromPageId=15303065).

{{% /alert %}} 
## **Adding Thumbnails to JFIF and EXIF Segments of JPEG Images**
Since the release of Aspose.Imaging for Java 2.4.0, the developers can [create thumbnails from JPEG images](/pages/createpage.action?spaceKey=imagingjava&title=Creating+Thumbnails+from+JPEG+Images&linkCreation=true&fromPageId=15303065) using the ExifData.Thumbnail property. It is also possible to add thumbnails to the JFIF and EXIF segments of JPEG images regardless of the fact that a given JPEG image previously had thumbnail embedded in it.

There are additional thumbnail properties in the ExifData and Jfif classes, which are of the JpegImage type, that can can be used to store additional thumbnail images inside the original JPEG image.
### **Add Thumbnail to JFIF Segment**
The code snippet below demonstrates how to use the Jfif.Thumbnail property to add a thumbnail image to the JFIF segment of a new JPEG image.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-ManipulatingJPEGImages-AddThumbnailtoJFIFSegment-AddThumbnailtoJFIFSegment.java" >}}

Thumbnail images with other segment data cannot occupy more than 65,545 bytes because of the JPEG format specifications. In cases where large images are to be set as a thumbnail, exception may arise.
### **Add Thumbnail to EXIF Segment**
The code snippet below demonstrate how to use the ExifData.Thumbnail property to add a thumbnail image to the EXIF segment of a new JPEG image.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-ManipulatingJPEGImages-AddThumbnailtoEXIFSegment-AddThumbnailtoEXIFSegment.java" >}}



In this case, the Aspose.Imaging API cannot estimate the thumbnail image size, but it can check the size of the entire EXIF data segment. This cannot be bigger than 65,535 bytes.
## **Using JpegExifData Class to Read and Modify Jpeg EXIF Tags**
Aspose.Imaging APIs provide [JpegExifData](https://apireference.aspose.com/java/imaging/com.aspose.imaging.exif/JpegExifData) class that is exclusive to Jpeg image formats to retrieve & update EXIF information. This article demonstrates the usage of [JpegExifData](https://apireference.aspose.com/java/imaging/com.aspose.imaging.exif/JpegExifData) class to achieve the same. com.aspose.imaging.exif.JpegExifData class serves as EXIF data container for Jpeg images, and provide means to retrieve standard Jpeg EXIF tags as demonstrated below:


### **Complete List of EXIF Tags**
The above code snippet reads a few EXIF Tags using the properties offered by com.aspose.imaging.exif.JpegExifData class. Complete list of these properties is available [here](https://apireference.aspose.com/java/imaging/com.aspose.imaging.exif/JpegExifData).
## **Auto Correct Orientation of JPEG Images**
Photos can be shot with a camera rotated at 90°, 180°, 270°, or none (normal orientation). Most digital cameras stores the orientation information along with the image data as EXIF tags of the JEPG images. This information can be used to perform the auto rotation on the images to correct the orientation.

Aspose.Imaging for Java API provides the autoRotate method for JpegImage class to auto correct the orientation of JPEG images. Here is how you can use the autoRotate method with Aspose.Imaging for Java.
### **Programming Sample**
{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-ManipulatingJPEGImages-AutoCorrectOrientationOfJPEGImages-AutoCorrectOrientationOfJPEGImages.java" >}}
## **Support for JPEG-LS**
` `Aspose.Imaging for Java API now provide support for JPEG-LS. The code snippet below demonstrates how to use that support for JPEG-LS image and decode that and save into png.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-ManipulatingJPEGImages-SupportForJPEG-LS-SupportForJPEG-LS.java" >}}
## **Support for JPEG-LS with CMYK and YCCK**
` `Aspose.Imaging for Java API now provide support for CMYK color models with JPEG-LS. The code snippet below demonstrates how to use that support for JPEG-LS.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-ManipulatingJPEGImages-SupportForJPEG-LSWithCMYK-SupportForJPEG-LSWithCMYK.java" >}}

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-ManipulatingJPEGImages-SupportForCMYKAndYCCKColorModesInJPEGLosslessUsingRGBProfile-SupportForCMYKAndYCCKColorModesInJPEGLosslessUsingRGBProfile.java" >}}


## **Support for 2-7 bits per sample in JPEG-LS images**
Aspose.Imaging for Java now provide support for 2-7 bits per sample JPEG-LS images. The code snippet below demonstrates how to use that support for JPEG-LS.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-ManipulatingJPEGImages-SupportFor2-7BitsPerSampleInJPEG-LS-SupportFor2-7BitsPerSampleInJPEG-LS.java" >}}
## **Setting Color Type and Compression Type for JPEG Images**
Aspose.Imaging for Java API now provide support for Color Type and compression Type and set them as gray scale and progressive for JPEG images. The code snippet below demonstrates how to use that support.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-ManipulatingJPEGImages-ColorTypeAndCompressionType-ColorTypeAndCompressionType.java" >}}
## **Convert TIFF to JPEG image**
Using Aspose.Imaging for Java, developers can convert TIFF to JPEG format. This topic explains the approach to load existing TIFF image and convert it to JPEG using **JpegOptions** class.

The steps to convert TIFF image to JPEG are as simple as below:

- Create an instance of the TiffImage and load image using Load method of Image class
- Iterate over the collection of frames of type TiffFrame
- Create an instance of JpegOptions class and set ResolutionSettings
- Set the resolution unit explicitly
- Call TiffFrame.Save method with destination path and an instance JpegOptions

Below provided sample code demonstrate how to convert TIFF to JPEG.

{{< gist "aspose-com-gists" "07be292db0a393dc95f153f84b28c069" "Examples-src-main-java-com-aspose-imaging-examples-ManipulatingJPEGImages-ConvertTIFFToJPEG-ConvertTIFFToJPEG.java" >}}
## **Memory Strategy optimization**
Loading and creating of JPEG images can be proceeded using memory strategy optimization - i.e. limiting memory buffer size for operation.
