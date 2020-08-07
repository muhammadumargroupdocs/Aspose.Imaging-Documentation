---
title: Manipulating Metafiles
type: docs
weight: 200
url: /java/manipulating-metafiles/
---

## **Converting Metafiles to Other Image Formats**
Using Aspose.Imaging for Java, developers can convert EMF and WMF (placeable and unplaceable) metafiles to other supported image formats. This topic explains the approach to load existing metafiles and convert them to other image format such as PNG and BMP.
### **Converting EMF to BMP using File Path Location**
Aspose.Imaging for Java provides the EmfMetafileImage class to load EMF files and same can be used to save the image in BMP format by passing an instance of BMPOptions class to the EmfMetafileImage.save method.

Below provided sample code uses the File Location Path to load and save the files on disk.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-metafile-ConvertEMFtoBMPusingFilePathLocation-ConvertEMFtoBMPusingFilePathLocation.java" >}}
### **Converting EMF to PNG using Byte Array**
Sometimes developers may need to load the images from an Array of Bytes to process them using Aspose.Imaging for Java API. In order to accomplish such requirements, EmfMetafileImage class provides a constructor accepting an object of InputStream, and an overload version on EmfMetafileImage.save method accepting an object of OutputStream.

Below provided sample code demonstrates the usage of Aspose.Imaging for Java API to load and save the images using Array of Bytes.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-metafile-ConvertEMFtoPNGusingByteArray-ConvertEMFtoPNGusingByteArray.java" >}}

{{% alert color="primary" %}} 

Above sample code uses the Files.readAllBytes method to read all the bytes from a file. The method ensures that the file is closed when all bytes have been read or an I/O error, or other runtime exception, is thrown. Please note, Files class was recently added in JDK 7 under package java.nio.file therefore you have to target JDK 7 if you intend to use the above sample as it is.

{{% /alert %}} 
### **Converting EMF To PDF**
Using Aspose.Imaging for Java, developers can convert EMF metafile to PDF format. This topic explains the approach to load existing metafiles and convert it to PDF.

Aspose.Imaging for .Net provides the **EmfImage** class to load EMF files and same can be used to save the image to PDF format.

Below provided sample code demonstrate how to convert EMF to PDF.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-metafile-ConvertEMFtoPDF-ConvertEMFtoPDF.java" >}}
### **Cropping EMF Image**
This article demonstrates the usage of Aspose.Imaging for Java API to crop Metafiles. Aspose.Imaging for Java has exposed the crop method for MetafileImage class that can be used to perform cropping on Metafiles.

The Aspose.Imaging for Java API supports two different approaches to Metafile cropping: by [shifts](/imaging/java/manipulating-metafiles-html/) and [rectangle](/imaging/java/manipulating-metafiles-html/).
#### **Cropping by Shifts**
The MetafileImage class provides an overload of the crop method that accepts 4 integer values denoting Left, Right, Top & Bottom. Based on these four values, the crop method moves the image boundaries toward the center of the image while discarding the outer portion.

The code snippet below demonstrates how to crop an image by shifts.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-metafile-ConvertEMFtoPDF-ConvertEMFtoPDF.java" >}}
#### **Cropping by Rectangle**
The MetafileImage class provides another overloaded version of the crop method that accepts an instance of the Rectangle class. You can cut out any portion of an image by providing the desired boundaries to the Rectangle object.

The code snippet below demonstrates how.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-metafile-CropbyRectangle-CropbyRectangle.java" >}}

The crop feature works only for export to raster format. In case the resultant image is stored back in Metafile format the crop method will have no effect.
### **Export MetaFile To Raster Formats**
Using Aspose.Imaging for Java, developers can convert metafile (Emf/Emf+) to raster formats. This article shows how to export/convert metafile file to raster image formats with Aspose.Imaging.
#### **Converting EMF to All Raster Image Formats**
It is easy to export metafiles with Aspose.Imaging for Java API. All you need is an object of the appropriate class from [com.aspose.imaging.imageoptions](/pages/createpage.action?spaceKey=imagingjava&title=com.aspose.imaging.imageoptions+package&linkCreation=true&fromPageId=15303059) package. By using these classes, you can easily export any EMF loaded with Aspose.Imaging for Java to any supported raster image format. Below is an example that demonstrates this simple procedure.

In the example, an EMF image is loaded by passing the file path as a parameter to the Image.load method. It is then exported to various image formats using the EmfMetafileImage ctor.

The examples here show how to load an EMF and save it to BMP, JPEG, PNG, GIF and finally TIFF using Aspose.Imaging for Java.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-metafile-ConvertEMFtoAllRasterImageFormats-ConvertEMFtoAllRasterImageFormats.java" >}}
#### **Converting Emf/Emf+ to Raster images**
Using Aspose.Imaging for Java, developers can convert metafile (Emf/Emf+) to raster formats. This article shows how to export/convert metafile file to raster image formats with Aspose.Imaging.

Aspose.Imaging for Java provides the **EmfImage** class to load EMF files and same can be used to convert the Emf to raster formats.

Below provided sample code demonstrate how to convert Emf/Emf+ to raster images.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-metafile-ConvertEmftoRasterimages-ConvertEmftoRasterimages.java" >}}
### **Specifying Font Folder While Converting**
Using Aspose.Imaging for Java, developers can specify the font folder path used while converting CAD (DXF) files. This topic explains the approach to specify the font folder that should be used.

Aspose.Imaging for Java provides the FontSettings class to manage font settings. Using FontSettings class you can specify the font folder that should be used while converting CAD (DXF) file. Note that this allows to add folder with TrueType fonts that will have the priority over other fonts on the system.

Below is the complete syntax to access the FontSettings class and set the font folder.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-metafile-SpecifyFontFolder-SpecifyFontFolder.java" >}}
## **Watermarking Metafiles**
This article demonstrates the usage of Aspose.Imaging for Java API to watermark Metafiles. Aspose.Imaging for Java has exposed the getWatermarkDrawer method for all classes that represent Metafiles.

The getWatermarkDrawer method returns an instance of Graphics2D object which allows to create custom watermarks.

The following code example demonstrates how to watermark EMF images and store the result in raster image format.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-metafile-WatermarkMetafiles-WatermarkMetafiles.java" >}}

{{% alert color="primary" %}} 

The watermarked image cannot be stored back to Metafile format.

{{% /alert %}} 

The getWatermarkDrawer method is available for EmfMetafileImage, MetafileImage and WmfMetafileImage classes.
## **Adding Raster Images to EMF Images**
This article demonstrates the usage of Aspose.Imaging for Java API to add raster images to EMF images.

Aspose.Imaging for Java has exposed the EmfMetafileImage.createEmfRecorderGraphics method that returns an instance of EmfRecorderGraphics2D that in turn can be used to call the drawImage method while specifying the instance of Image to be inserted in EMF image.

The following code example demonstrates how to add a raster image to EMF file.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-metafile-AddRasterImagestoEMFImages-AddRasterImagestoEMFImages.java" >}}
## **Getting Font Information**
Using Aspose.Imaging for Java, developers can get information about the font used in the WMF file while converting WMF file. This topic explains, how one can get information about missing fonts and how to get the list of all fonts used in the WMF file.

Aspose.Imaging for Java provides the **FontSettings** class to get font information. **FontSettings** provides the functionality to get

- A list of font names accessible to Aspose.Imaging API.
- A list of font names used in the metafile.
- A list of font names that are missing in the environment with respect to WMF file loaded.

Below is the complete syntax to access the **FontSettings** class and get the font information.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-metafile-GetFontInfo-GetFontInfo.java" >}}
## **Specifying Substitute Fonts**
Using Aspose.Imaging for Java, developers can specify the substitute fonts instead of original font while converting WMF file. This topic explains the approach how to specify the substitute fonts.

Aspose.Imaging for Java provides the FontSettings class to manage font settings. Using FontSettings class you can specify the substitute fonts that should be used instead of original one while converting WMF file. Method addFontSubstitutes can be used that takes in **originalFontName** string as first parameter and an array of strings **substituteFontNames** as second parameter.

Below is the complete syntax to access the FontSettings class and supply the substitute Fonts.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-metafile-SpecifySubstituteFonts-SpecifySubstituteFonts.java" >}}
## **Applying Font Settings For Metafiles**
Using Aspose.Imaging for Java, developers can add fonts folder path into the existing font folder settings used while converting metafiles (EMF) files. This topic explains the approach to apply the font settings that should be used while converting metafiles.

Aspose.Imaging for Java provides the FontSettings class to manage font settings. Using FontSettings class you can specify the font folder that should be used while converting metafiles (EMF).

Below is the complete syntax to access the FontSettings class and set/add the font folder path.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-metafile-ApplyFontSettings-ApplyFontSettings.java" >}}
## **Managing resources while saving Metafile as SVG**
Using Aspose.Imaging for Java, developers can manage resources (fonts and internal images) when saving Metafile images (emf and wmf) into SVG file stream. This topic explains that there should be a setting that will let us specify whether to save contained image as a separate file and provide a stream for saving it, or to embed image as base64 string inside of SVG. The following code snippet demonstrates the usage of Aspose.Imaging for Java API to manage resources.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-metafile-MetaFilesAsSVG-MetaFilesAsSVG.java" >}}
## **Support For Replacing Missing Fonts**
Using Aspose.Imaging for Java, developers can replace missing fonts when saving ODG, SVG and MetaFile images. This topic explains the approach to replace the fonts that should be used. The following code snippet demonstrates the usage of Aspose.Imaging for Java API to replace the font while saving ODG images.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-metafile-MetaFilesAsSVG-MetaFilesAsSVG.java" >}}
