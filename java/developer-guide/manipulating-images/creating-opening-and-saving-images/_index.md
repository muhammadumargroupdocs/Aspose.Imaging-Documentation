---
title: Creating, Opening and Saving Images
type: docs
weight: 50
url: /java/creating-opening-and-saving-images/
---

## **Creating Image Files**
Aspose.Imaging for .Java allows developers to create their own images. Use the static [Create](http://www.aspose.com/api/java/imaging/com.aspose.imaging/classes/image/methods/create\(com.aspose.imaging.ImageOptionsBase,int,int\)/) method exposed by the [Image](http://www.aspose.com/api/java/imaging/com.aspose.imaging/classes/Image) class to create new images. All you need to do is to supply the appropriate object of one of the classes from the [ImageOptions](http://www.aspose.com/api/java/imaging/com.aspose.imaging.imageoptions/index) namespace for the desired output image format.

To create an image file, first create an instance of one of the classes from the ImageOptions namespace. These classes determine output image format.

Below are some classes from the [ImageOptions](http://www.aspose.com/api/java/imaging/com.aspose.imaging.imageoptions/index) namespace:

- [BmpOptions](http://www.aspose.com/api/java/imaging/com.aspose.imaging.imageoptions/classes/BmpOptions) sets the options for creating a BMP file
- [GifOptions](http://www.aspose.com/api/java/imaging/com.aspose.imaging.imageoptions/classes/GifOptions) sets the options for creating a GIF file
- [JpegOptions](http://www.aspose.com/api/java/imaging/com.aspose.imaging.imageoptions/classes/JpegOptions) sets the options for creating a JPEG file
- [PngOptions](http://www.aspose.com/api/java/imaging/com.aspose.imaging.imageoptions/classes/PngOptions) sets the options for creating a PNG file
- [TiffOptions](http://www.aspose.com/api/java/imaging/com.aspose.imaging.imageoptions/classes/TiffOptions) sets the options for creating a TIFF file
- [PsdOptions](http://www.aspose.com/api/java/imaging/com.aspose.imaging.imageoptions/classes/PsdOptions) sets the options for creating a PSD file

Image files can be created [setting an output path](http://www.aspose.com/docs/display/imagingnet/Drawing+and+Formatting+Images#DrawingandFormattingImages-CreatingbySettingPath) or by [setting a stream](http://www.aspose.com/docs/display/imagingnet/Drawing+and+Formatting+Images#DrawingandFormattingImages-CreatingUsingStream). Both examples are described below.

Aspose.Imaging for Java allows developers to create their own images. Use the static create method exposed by the Image class to create new images. All you need to do is to supply the appropriate object of one of the classes from the imageoptions namespace for the desired output image format.
### **Creating an Image by Setting a Path**
Create an object of any desired class from the imageoptions namespace and set the various properties like dimension (width, height) of the new image. The width and height are defined in pixels. The most important property to set is the Source property. This property specifies where the image data resides (in a file or a stream). In the example below, the source is a file. After setting the properties, pass the object to one of the static create methods. In the example below, we are creating a BMP file so we need to create an instance of imageoptions.BmpOptions.

{{< gist "aspose-com-gists" "07be292db0a393dc95f153f84b28c069" "CreatingAnImageBySettingPath.java" >}}
### **Creating through Stream**
The process for creating an image using a stream is same as for using a path. The only difference is that you need to create an instance of StreamSource by passing a Stream object to its constructor and assigning it to the Source property. Below is an example.

{{< gist "aspose-com-gists" "07be292db0a393dc95f153f84b28c069" "Examples-src-main-java-com-aspose-imaging-examples-files-CreatingImageUsingStream-CreatingImageUsingStream.java" >}}


## **Opening Image Files**
The Image class is Aspose.Imaging's core class. The Image class provides methods for manipulating a single image frame, for example a JPEG image. Use the Image class to load existing image files to add effects to the image or to convert a file to another format, for example. Whatever the purpose is, Aspose.Imaging provides two standard ways to open existing files: from file or from a stream. They are discussed below with examples.
### **Opening an Image File from Disk**
Open an image file by passing the path and file name as a parameter to the static method load exposed by the Image class as shown below.

{{< gist "aspose-com-gists" "07be292db0a393dc95f153f84b28c069" "Examples-src-main-java-com-aspose-imaging-examples-files-OpeningImagefilesfromdisk-OpeningImagefilesfromdisk.java" >}}


### **Opening an Image using a Stream**
Sometimes the image that we need to open is stored as a stream of bytes.When this is the case, use the overloaded version of the load method. This accepts a Stream object as an argument to open the image.

{{< gist "aspose-com-gists" "07be292db0a393dc95f153f84b28c069" "Examples-src-main-java-com-aspose-imaging-examples-files-OpeningImageusingaStream-OpeningImageusingaStream.java" >}}
## **Saving Image Files**
Aspose.Imaging lets you create image files from scratch. It also provides the means to edit existing image files. Once the image is created or modified, the file is usually saved to disk.

Aspose.Imaging provides you with methods for saving images to a [disk by specifying a path](/imaging/java/creating-2c-opening-and-saving-images-html/) or [using a Stream object](/imaging/java/creating-2c-opening-and-saving-images-html/).

{{% alert color="primary" %}} 

If the image is created by specifying any of the ImageOptions in the Image.create static method, the image is automatically saved to the path or stream supplied during the initialization of the Image class.

{{% /alert %}} 
### **Saving to Disk**
The Image class represents an image object, so this class provides all the tools needed to create, load and save an image file. Use the Image class' Save method to save images. One overloaded version of the Save method accepts the file location as a string. Below is an example of how this can be used.

{{< gist "aspose-com-gists" "07be292db0a393dc95f153f84b28c069" "Examples-src-main-java-com-aspose-imaging-examples-files-SavingtoDisk-SavingtoDisk.java" >}}


### **Saving to a Stream**
Another overloaded version of the Save method accepts the Stream object as an argument and saves the image file to the stream.

{{< gist "aspose-com-gists" "07be292db0a393dc95f153f84b28c069" "Examples-src-main-java-com-aspose-imaging-examples-files-SavingtoStream-SavingtoStream.java" >}}
### **Setting for Replacing Missing Fonts**
Developers can use Aspose.Imaging for Java API to load existing image files for different purposes, than with that developers will be able to set default font name when saving PSD documents as raster image (into PNG, JPG and BMP formats). This default font should be used as a replacement for all missing fonts (fonts that are not found in current Operating System). Once the image is modified, the file will be saved to disk.

{{< gist "aspose-com-gists" "07be292db0a393dc95f153f84b28c069" "Examples-src-main-java-com-aspose-imaging-examples-ModifyingImages-SupportForReplacingMissingFonts-SupportForReplacingMissingFonts.java" >}}
## **Image load/save indication progress**
{{< gist "aspose-com-gists" "07be292db0a393dc95f153f84b28c069" "ProgressCallback.java" >}}



