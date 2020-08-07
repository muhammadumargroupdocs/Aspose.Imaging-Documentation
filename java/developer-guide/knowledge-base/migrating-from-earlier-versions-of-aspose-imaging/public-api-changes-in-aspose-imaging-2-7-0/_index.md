---
title: Public API Changes in Aspose.Imaging 2.7.0
type: docs
weight: 160
url: /java/public-api-changes-in-aspose-imaging-2-7-0/
---

{{% alert color="primary" %}} 

This document describes the changes to the Aspose.Imaging API from version 2.6.0 to 2.7.0 that may be of interest to module/application developers. It includes not only new and updated public methods, [added classes etc.](/imaging/java/public-api-changes-in-aspose-imaging-2-7-0-html/) and [removed classes etc.](/imaging/java/public-api-changes-in-aspose-imaging-2-7-0-html/), but also a description of any changes in the behavior behind the scenes in Aspose.Imaging.

{{% /alert %}} 
## **Added Classes, Enumerations and Methods**
### **Method GifImage.insertBlock Added**
Method com.aspose.imaging.fileformats.gif.GifImage.insertBlock enables the developers to insert a GIF block at a particular position of blocks array. The said method accepts an integer as first parameter to insert the block at specified index.

**Java**

{{< highlight csharp >}}

 gifImage.insertBlock(index, block);

{{< /highlight >}}
### **Method License.isLicensed Added**
The com.aspose.imaging.License class has exposed the isLicensed method that will return true if license has been properly set.

**C#**

{{< highlight csharp >}}

 License license = new License();

license.setLicense(licensePath);

if (License.isLicensed())

{

    System.out.println("License is Set!");

} Console.WriteLine("License is Set!");

{{< /highlight >}}
### **Property CadRasterizationOptions.Layouts Added**
Newly added property com.aspose.imaging.imageoptions.CadRasterizationOptions.Layouts allows to specify one or more CAD layouts for possible conversion to PDF or raster image formats. Layout names can be specified as a list of strings whereas the expected results are multipage for PDF & TIFF formats, multiframe for GIF and multilayered PSD if more than one layouts have been specified.

Specified ordering of layouts during the rendering is preserved.

**Java**

{{< highlight csharp >}}

 PdfOptions pdfOptions = new PdfOptions();

CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();

pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);

cadRasterizationOptions.setLayouts(new String[] { "Layout1", "Model", "Layout2" });

{{< /highlight >}}
### **Property RasterImage.HasTransparentColor Added**
The com.aspose.imaging.RasterImage class has exposed the HasTransparentColor property to ease the access of image's transparent color value. The boolean type property return true or false depending if the image has transparent color data or not, whereas the property works only for PNG & GIF file formats.
### **Property RasterImage.HasTransparentColor Added**
The com.aspose.imaging.RasterImage class has exposed the TransparentColor property to get/set the image's transparent color, whereas the property works only for PNG & GIF file formats.
### **Properties Image.HasBackgroundColor & RasterImage.HasBackgroundColor Added**
The com.aspose.imaging.Image & com.aspose.imaging.RasterImage classes have added the HasBackgroundColor property. The boolean type property return true or false depending if the block has background color data or not, whereas the property works only for PNG & GIF file formats.
### **Properties Image.BackgroundColor & RasterImage.BackgroundColor Added**
The com.aspose.imaging.Image & com.aspose.imaging.RasterImage classes have exposed the BackgroundColor property to get/set the image's background color, whereas the property works only for PNG & GIF file formats.
### **Property GifFrameBlock.HasTransparentColor Added**
The com.aspose.imaging.fileformats.gif.blocks.GifFrameBlock class has now exposed the HasTransparentColor property with the release of Aspose.Imaging 2.7.0 to ease the access of GIF block transparent color value. The boolean type property return true or false depending if the block has transparent color data or not.
### **Property GifFrameBlock.TransparentColor Added**
The com.aspose.imaging.fileformats.gif.blocks.GifFrameBlock class has now exposed the TransparentColor property to get/set the image's transparent color.
### **Property GifFrameBlock.HasBackgroundColor Added**
The com.aspose.imaging.fileformats.gif.blocks.GifFrameBlock class has added the HasBackgroundColor property. The boolean type property return true or false depending if the block has background color data or not.
### **Property GifFrameBlock.BackgroundColor Added**
The com.aspose.imaging.fileformats.gif.blocks.GifFrameBlock class has now exposed the BackgroundColor property to get/set the image's background color.
### **Property PngImage.HasTransparentColor Added**
The com.aspose.imaging.fileformats.png.PngImage class has now exposed the HasTransparentColor property with the release of Aspose.Imaging 2.7.0 to ease the access of PNG image's transparent color value. The boolean type property return true or false depending if the block has transparent color data or not.
### **Property PngImage.TransparentColor Added**
The com.aspose.imaging.fileformats.png.PngImage class has now exposed the TransparentColor property to get/set the PNG image's transparent color.
### **Property PngImage.HasBackgroundColor Added**
The com.aspose.imaging.fileformats.png.PngImage class has added the HasBackgroundColor property. The boolean type property return true or false depending if the PNG image has background color data or not.
### **Property PngImage.BackgroundColor Added**
The com.aspose.imaging.fileformats.png.PngImage class has now exposed the BackgroundColor property to get/set the PNG image's background color.
## **Removed Properties**
### **Property CadRasterizationOptions.LayoutName Removed**
The property com.aspose.imaging.imageoptions.CadRasterizationOptions.LayoutName has been replaced by the com.aspose.imaging.imageoptions.CadRasterizationOptions.Layouts property that can be used to specify one or more layout names for the CAD to PDF & CAD to raster image conversion.
### **Property PngOptions.TransparentColor Removed**
The property com.aspose.imaging.imageoptions.PngOptions.TransparentColor has been replaced by the com.aspose.imaging.fileformats.png.PngImage.HasTransparentColor and com.aspose.imaging.fileformats.png.PngImage.TransparentColor properties for better understanding.
