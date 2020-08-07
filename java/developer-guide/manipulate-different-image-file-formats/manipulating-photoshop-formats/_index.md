---
title: Manipulating Photoshop Formats
type: docs
weight: 210
url: /java/manipulating-photoshop-formats/
---

## **Exporting Image to PSD**
PSD, Photoshop document, is the default file format used by Adobe Photoshop for working with images. Aspose.Imaging lets you save files in PSD format so that they can be opened and edited in Photoshop. This article shows how to save a file to PSD with Aspose.Imaging, and it also discusses some of the settings that can be used when saving to this format.

PsdOptions class is a specialized class in the com.aspose.imaging.imageoptions package used to export images to PSD. In order to export and image format to PSD, first create an instance of the Image class, either loaded from an existing image file or created from scratch. This article explains how.

In the examples below, an existing image is loaded by passing the file path to the Image class' static load method. Once it is loaded, save the image using the Image class' save method, and supply a PsdOptions object as the second argument.

Several of the PsdOptions class' properties can be set for advanced conversion. Some of the properties are ColorMode, CompressionMethod and Version.

Aspose.Imaging for Java supports the following compression methods through the CompressionMethod enumeration:

- CompressionMethod.Raw
- CompressionMethod.RLE
- CompressionMethod.ZipWithoutProtection
- CompressionMethod.ZipWithProtection

The following color modes are supported through the ColorModes enumeration:

- ColorModes.Bitmap
- ColorModes.Grayscale
- ColorModes.RGB

Additional resources can be added, such as thumbnail resources for PSD v4.0, v5.0 and higher, or grid and guide resources for PSD v4.0 and higher.

The code below opens a BMP file from disk and saves it to PSD with RLE compression and RGB color mode.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-export-ExportImageToPSD-ExportImageToPSD.java" >}}
## **Importing image to PSD layer**
This article demonstrates the usage of Aspose.Imaging for Java to add or import an image to a PSD layer. Aspose.Imaging API have exposed efficient & easy to use methods to achieve this goal.

Aspose.Imaging for Java has exposed the **DrawImage** method of the **Layer** class to add/import an image into a PSD file. **DrawImage** method needs location and image values to add/import an image into a PSD file.

The steps to import image into PSD layer are as simple as below:

1. Load a PSD file as an image using the factory method Load exposed by Image class.
1. Convert the image to **PsdImage**.
1. Create an instance of **Layer** class and assign the PSD image layer to it.
1. Load the image that is needed to be added.
1. Call the Layer.DrawImage method while specifying location and image instance.
1. Save the results.

The following code example demonstrates how to import an image.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-Photoshop-ImportanImageToPSDLayer-ImportanImageToPSDLayer.java" >}}
## **Color replacement in PSD layers**
This article demonstrates the usage of Aspose.Imaging for Java to replace color in PSD layers. Aspose.Imaging APIs have exposed efficient & easy to use methods to achieve this goal.The steps to replacement into PSD layer are as simple as below:

1. Load a PSD file as an image using the factory method Load exposed by Image class.
1. Traverse through layers of image and replace color.
1. Save the results.

The following code snippet shows you how to import image to PSD layer.

The following code example demonstrates how to import an image.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-ModifyingImages-ColorReplacement-ColorReplacement.java" >}}
## **Creating Thumbnails from PSD Files**
PSD is the native document format of Adobe's Photoshop application. Adobe Photoshop (version 5.0 and later) stores thumbnail information for preview display in an image resource block that consists of an initial 28-byte header, followed by a JFIF thumbnail in RGB (red, green, blue) order.

Aspose.Imaging for Java API provides an easy to use mechanism to access the resources of PSD file. These resources also include the thumbnail resource that in turn can be fetched and saved to disc as per application needs.

The following code snippet demonstrates the usage of Aspose.Imaging for Java API to achieve the same.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-Photoshop-CreateThumbnailsfromPSDFiles-CreateThumbnailsfromPSDFiles.java" >}}
## **Creating Indexed PSD Files**
Aspose.Imaging for Java API can create Indexed PSD files from scratch. This article demonstrates the use of PsdOptions and PsdImage classes to create an Indexed PSD while drawing some shapes over the newly created canvas.

The following simple steps are required to create an Indexed PSD file.

1. Create an instance of PsdOptions and set it's source.
1. Set ColorMode property of the PsdOptions to ColorModes.Indexed.
1. Create a new palette of colors from RGB space and set it as Palette property of PsdOptions.
1. Set CompressionMethod property to required compression algorithm.
1. Create a new PSD image by calling the PsdImage.create method.
1. Draw graphics or perform other operations as per requirement.
1. Call PsdImage.save method to commit all changes.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-Photoshop-CreatIndexedPSDFiles-CreatIndexedPSDFiles.java" >}}
## **Exporting PSD Layer to Raster Image**
Aspose.Imaging allows you to export layers in a PSD file into raster images. Please use the com.aspose.imaging.fileformats.psd.layers.Layer.save method to export the layer to image.

The following sample code loads a PSD file and exports each of its layer into a PNG image using com.aspose.imaging.fileformats.psd.layers.Layer.save. Once all layers are exported into PNG images, you can open them using your favorite image viewer.

Here is sample code.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-Photoshop-ExportPSDLayertoRasterImage-ExportPSDLayertoRasterImage.java" >}}
## **Update Text Layer In PSD File**
Aspose.Imaging for Java allows you to manipulate the text in the text layer of a PSD file. Please use the com.aspose.imaging.fileformats.psd.Layers.TextLayer class to update text in PSD layer.
### **Exporting PSD Layer to Raster Image**
The following sample code loads a PSD file, access the text layer, update the text and save the PSD file with a new name using com.aspose.imaging.fileformats.psd.Layers.TextLayer.UpdateText method.

Here is sample code.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-Photoshop-ExportPSDLayertoRasterImage-ExportPSDLayertoRasterImage.java" >}}
## **Detecting Flattened PSD**
Aspose.Imaging for Java allows you to detect whether a given PSD file is flatten or not. IsFlatten property has been introduced in the com.aspose.imaging.fileformats.psd.PsdImage class to achieve this functionality.

The following sample code loads a PSD file and access the property isFlatten.

Here is sample code.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-Photoshop-DetectFlattenedPSD-DetectFlattenedPSD.java" >}}
## **Merge PSD layers While Converting PSD to JPG**
This article shows how to merge layers in a PSD file while converting a PSD file to JPG with Aspose.Imaging.

In the example below, an existing PSD file is loaded by passing the file path to the Image class' static Load method. Once it is loaded, convert/cast the image to PsdImage. Create a JPG file stream. Create an instance of the JpegOptions class. Set the Source property to JPG file stream. Now call the Save method of the PsdImage instance.

Here is sample code.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-Photoshop-MergPSDlayers-MergPSDlayers.java" >}}
## **Grayscale Support with Alpha for PSD**
This article shows how to support Grayscale with alpha for PSD file while converting a PSD file to PNG with Aspose.Imaging. In the example below, an existing PSD file is loaded by passing the file path to the Image class static Load method. Once it is loaded, convert/cast the image to PsdImage. Create an instance of the PngOptions class. Set the color property to PNG file . Now call the [Save](http://www.aspose.com/api/net/imaging/aspose.imaging/image/methods/save/index) method of the PngOptions instance. The following code snippet shows you how to support Grayscale with Alpha.

Here is sample code.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-ModifyingImages-SupportGrayScaleWithAlpha-SupportGrayScaleWithAlpha.java" >}}
## **Support for Subscript PSD**
This article shows how to add the Subscript option parsing and rendering for PSD text layer. The following code snippet shows you how to support Subscript.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-ModifyingImages-SupportForSubscript-SupportForSubscript.java" >}}
## **Support for EPS Format**
This article shows how to support Formats like EPS in Aspose.Imaging. The following code snippet shows you how to support EPS.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-EPS-SupportForEPS-SupportForEPS.java" >}}
## **Support for SmallCap PSD**
This article shows how to add the SmallCap option parsing and rendering for PSD text layer. The following code snippet shows you how to support SmallCap.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-ModifyingImages-SupportForSmallCap-SupportForSmallCap.java" >}}
## **Support Layer Effects For PSD**
This article shows how support different effects like **Blur, Inner Glow, Outer Glow** for PSD layer. The following code snippet shows you how to support layer effects.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-Photoshop-SupportEffectsforPSD-SupportEffectsforPSD.java" >}}
## **Specifying a Font Folder**
The **FontSettings.** **addFontsFolder()** method is used to indicate where Aspose.Imaging should look for fonts. When a valid path is passed to this method, Aspose.Imaging no longer looks in the registry or the Windows\Font folder to look for fonts and only scans for fonts within the specified folder. When a custom font folder is set using this method, the folder is checked that it exists and is accessible. If the folder cannot be found, then it sets the default folder.

The following examples demonstrates how to set the folder

{{< gist "aspose-com-gists" "07be292db0a393dc95f153f84b28c069" "Examples-src-main-java-com-aspose-imaging-examples-Photoshop-SetFontsFolder-SetFontsFolder.java" >}}
## **Rendering of Rotated Text Layers**
` `Aspose.Imaging for Java provides the feature of rendering of rotated Text layers. In the example below, an existing PSD file is loaded by passing the file path to the Image class static Load method. Now call the Save method of the PsdImage instance.

The following code snippet shows you how to render rotated Text layers.

{{< gist "aspose-com-gists" "07be292db0a393dc95f153f84b28c069" "Examples-src-main-java-com-aspose-imaging-examples-Photoshop-RenderingOfRotatedTextLayerByTransformMatrix-RenderingOfRotatedTextLayerByTransformMatrix.java" >}}
## **Support of Fill Layers With Gradient Fill**
This article demonstrates the usage of Gradient fill to fill PSD layer. Aspose.Imaging for Java APIs have exposed efficient and easy to use methods to achieve this goal. Aspose.Imaging has exposed the **GradientColorPoint** and **GradientTransparencyPoint** classes to add Gradient effect into a layer.

` `The steps to fill PSD layer with Gradient fill are as simple as below:

- Load a PSD file as an image using the factory method Load exposed by Image class.
- Set settings properties of FillLayer object.
- Create list of ColorPoints with required colors and position of color.
- Create list of TransparencyPoints with required opacity and position of transparency point.
- Call the FillLayer.Update method
- Save the results.

The following code snippet shows you how to add Gradient fill to PSD layer.  

{{< gist "aspose-com-gists" "07be292db0a393dc95f153f84b28c069" "Examples-src-main-java-com-aspose-imaging-examples-Photoshop-SupportOfGradientFillLayer-SupportOfGradientFillLayer.java" >}}
## **Support of Fill Layers With Color Fill**
This article demonstrates how to fill PSD layer with Color. Please use the **Aspose.Imaging.FileFormats.Psd.Layers.FillLayer** to add Color in PSD layer. The following code snippets loads a PSD file, access the **Filllayer** class and sets the color using the **FillLayer.FillSettings** property.

{{< gist "aspose-com-gists" "07be292db0a393dc95f153f84b28c069" "Examples-src-main-java-com-aspose-imaging-examples-Photoshop-SupportOfColorFillLayer-SupportOfColorFillLayer.java" >}}
## **Support of VmskResource**
This article shows support of **VmskResource** in a PSD file with Aspose.Imaging.

- Load a PSD file as an image using the factory method Load exposed by Image class
- Get VmskResource from image layer
- Set required properties of VmskResource
- Save the results

The following code snippet shows you how Aspose.Imaging supports VmskResource. 

{{< gist "aspose-com-gists" "07be292db0a393dc95f153f84b28c069" "Examples-src-main-java-com-aspose-imaging-examples-Photoshop-SupportOfVmskResource-SupportOfVmskResource.java" >}}

{{< gist "aspose-com-gists" "07be292db0a393dc95f153f84b28c069" "Examples-src-main-java-com-aspose-imaging-examples-Photoshop-SupportOfVmskResource-VmskResource.java" >}}
## **Support of GdFlResource**
This article demonstrates how Aspose.Imaging for Java supports **GdFIResource** in a PSD file. **GdFIResource** contains information about blending of clipped element.

- Load a PSD file as an image using the factory method Load exposed by Image class.
- Get GdFlResource from image layer
- Create list of ColorPoints with required colors and position of color.
- Create list of TransparencyPoints with required opacity and position of transparency point.
- Save the results.

The following code snippet shows how Aspose.Imaging for Java supports GdFIResource.

{{< gist "aspose-com-gists" "07be292db0a393dc95f153f84b28c069" "Examples-src-main-java-com-aspose-imaging-examples-Photoshop-SupportOfGdFlResource-SupportOfGdFlResource.java" >}}
## **Support of SoCoResource**
This article demonstrates how Aspose.Imaging for Java supports **SoCoResource** in a PSD file. 

- Load a PSD file as an image using the factory method Load exposed by Image class.
- Get SoCoResource from image layer
- Set required properties
- Save the results

` `The following code snippet shows how Aspose.Imaging for Java supports SoCoResource. 

{{< gist "aspose-com-gists" "07be292db0a393dc95f153f84b28c069" "Examples-src-main-java-com-aspose-imaging-examples-Photoshop-SupportOfSoCoResource-SupportOfSoCoResource.java" >}}
