---
title: Public API Changes in Aspose.Imaging 2.7.0
type: docs
weight: 160
url: /net/public-api-changes-in-aspose-imaging-2-7-0/
---

{{% alert color="primary" %}} 

This document describes the changes to the Aspose.Imaging API from version 2.6.0 to 2.7.0 that may be of interest to module/application developers. It includes not only new and updated public methods, [added classes etc.](/imaging/net/public-api-changes-in-aspose-imaging-2-7-0-html/) and [removed classes etc.](/imaging/net/public-api-changes-in-aspose-imaging-2-7-0-html/), but also a description of any changes in the behavior behind the scenes in Aspose.Imaging.

{{% /alert %}} 
## **Added Classes, Enumerations and Methods**
### **Classes CadRenderHandler, CadRenderResult, RenderErrorCode & RenderResult Added**
Aspose.Imaging for .NET 2.7.0 has introduced a series of new classes to assist with tracking of CAD rendering process. Newly added classes and few supporting enumeration fields are listed below.

- Aspose.Imaging.ImageOptions.CadRasterizationOptions.CadRenderHandler Class
- Aspose.Imaging.ImageOptions.CadRenderResult Class
- Aspose.Imaging.ImageOptions.RenderErrorCode Class
- Aspose.Imaging.ImageOptions.RenderResult Class
- Aspose.Imaging.ImageOptions.CadRasterizationOptions.RenderResult Enumeration Field
- Aspose.Imaging.ImageOptions.CadRenderResult.Failures Enumeration Field
- Aspose.Imaging.ImageOptions.RenderErrorCode.MissingBlocks Enumeration Field
- Aspose.Imaging.ImageOptions.RenderErrorCode.MissingDimensionStyles Enumeration Field
- Aspose.Imaging.ImageOptions.RenderErrorCode.MissingHeader Enumeration Field
- Aspose.Imaging.ImageOptions.RenderErrorCode.MissingLayouts Enumeration Field
- Aspose.Imaging.ImageOptions.RenderErrorCode.MissingStyles Enumeration Field

With these changes in place, the CAD to PDF conversion can now be achieved as follow while enabling the tracking.

**C#**

{{< highlight csharp >}}

 using (Image image = Image.Load(sourceImage))

{

    MemoryStream stream = new MemoryStream();

    PdfOptions pdfOptions = new PdfOptions();

    CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();

    pdfOptions.VectorRasterizationOptions = cadRasterizationOptions;

    cadRasterizationOptions.PageWidth = 800;

    cadRasterizationOptions.PageHeight = 600;

    cadRasterizationOptions.RenderResult += new CadRasterizationOptions.CadRenderHandler(this.delegateRenderResult);

    image.Save(stream, pdfOptions);

}

{{< /highlight >}}

**Visual Basic**

{{< highlight csharp >}}

 Using image As Image = Image.Load(sourceImage)

	Dim stream As New MemoryStream()

	Dim pdfOptions As New PdfOptions()

	Dim cadRasterizationOptions As New CadRasterizationOptions()

	pdfOptions.VectorRasterizationOptions = cadRasterizationOptions

	cadRasterizationOptions.PageWidth = 800

	cadRasterizationOptions.PageHeight = 600

	cadRasterizationOptions.RenderResult += New CadRasterizationOptions.CadRenderHandler(Me.delegateRenderResult)

	image.Save(stream, pdfOptions)

End Using

{{< /highlight >}}
### **Method GifImage.InsertBlock Added**
Method Aspose.Imaging.FileFormats.Gif.GifImage.InsertBlock enables the developers to insert a GIF block at a particular position of blocks array. The said method accepts an integer as first parameter to insert the block at specified index.

**C#**

{{< highlight csharp >}}

 gifImage.InsertBlock(index, block);

{{< /highlight >}}

**Visual Basic**

{{< highlight csharp >}}

 gifImage.InsertBlock(index, block)

{{< /highlight >}}
### **Property License.IsLicensed Added**
The Aspose.Imaging.License class has exposed the IsLicensed property that will return true if license has been properly set.

**C#**

{{< highlight csharp >}}

 License license = new License();

license.SetLicense(licensePath);

if (license.IsLicensed)

{

    Console.WriteLine("License is Set!");

}

{{< /highlight >}}

**Visual Basic**

{{< highlight csharp >}}

 Dim license As New License()

license.SetLicense(licensePath)

If license.IsLicensed Then

	Console.WriteLine("License is Set!")

End If

{{< /highlight >}}
### **Property CadRasterizationOptions.Layouts Added**
Newly added property Aspose.Imaging.ImageOptions.CadRasterizationOptions.Layouts allows to specify one or more CAD layouts for possible conversion to PDF or raster image formats. Layout names can be specified as a list of strings whereas the expected results are multipage for PDF & TIFF formats, multiframe for GIF and multilayered PSD if more than one layouts have been specified.

Specified ordering of layouts during the rendering is preserved.

**C#**

{{< highlight csharp >}}

 PdfOptions pdfOptions = new PdfOptions();

CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();

pdfOptions.VectorRasterizationOptions = cadRasterizationOptions;

cadRasterizationOptions.Layouts = new string[] { "Layout1", "Model", "Layout2" };

{{< /highlight >}}

**Visual Basic**

{{< highlight csharp >}}

 Dim pdfOptions As New PdfOptions()

Dim cadRasterizationOptions As New CadRasterizationOptions()

pdfOptions.VectorRasterizationOptions = cadRasterizationOptions

cadRasterizationOptions.Layouts = New String() { "Layout1", "Model", "Layout2" }

{{< /highlight >}}
### **Property RasterImage.HasTransparentColor Added**
The Aspose.Imaging.RasterImage class has exposed the HasTransparentColor property to ease the access of image's transparent color value. The boolean type property return true or false depending if the image has transparent color data or not, whereas the property works only for PNG & GIF file formats.
### **Property RasterImage.HasTransparentColor Added**
The Aspose.Imaging.RasterImage class has exposed the TransparentColor property to get/set the image's transparent color, whereas the property works only for PNG & GIF file formats.
### **Properties Image.HasBackgroundColor & RasterImage.HasBackgroundColor Added**
The Aspose.Imaging.Image & Aspose.Imaging.RasterImage classes have added the HasBackgroundColor property. The boolean type property return true or false depending if the block has background color data or not, whereas the property works only for PNG & GIF file formats.
### **Properties Image.BackgroundColor & RasterImage.BackgroundColor Added**
The Aspose.Imaging.Image & Aspose.Imaging.RasterImage classes have exposed the BackgroundColor property to get/set the image's background color, whereas the property works only for PNG & GIF file formats.
### **Property GifFrameBlock.HasTransparentColor Added**
The Aspose.Imaging.FileFormats.Gif.Blocks.GifFrameBlock class has now exposed the HasTransparentColor property with the release of Aspose.Imaging 2.7.0 to ease the access of GIF block transparent color value. The boolean type property return true or false depending if the block has transparent color data or not.
### **Property GifFrameBlock.TransparentColor Added**
The Aspose.Imaging.FileFormats.Gif.Blocks.GifFrameBlock class has now exposed the TransparentColor property to get/set the image's transparent color.
### **Property GifFrameBlock.HasBackgroundColor Added**
The Aspose.Imaging.FileFormats.Gif.Blocks.GifFrameBlock class has added the HasBackgroundColor property. The boolean type property return true or false depending if the block has background color data or not.
### **Property GifFrameBlock.BackgroundColor Added**
The Aspose.Imaging.FileFormats.Gif.Blocks.GifFrameBlock class has now exposed the BackgroundColor property to get/set the image's background color.
### **Property PngImage.HasTransparentColor Added**
The Aspose.Imaging.FileFormats.Png.PngImage class has now exposed the HasTransparentColor property with the release of Aspose.Imaging 2.7.0 to ease the access of PNG image's transparent color value. The boolean type property return true or false depending if the block has transparent color data or not.
### **Property PngImage.TransparentColor Added**
The Aspose.Imaging.FileFormats.Png.PngImage class has now exposed the TransparentColor property to get/set the PNG image's transparent color.
### **Property PngImage.HasBackgroundColor Added**
The Aspose.Imaging.FileFormats.Png.PngImage class has added the HasBackgroundColor property. The boolean type property return true or false depending if the PNG image has background color data or not.
### **Property PngImage.BackgroundColor Added**
The Aspose.Imaging.FileFormats.Png.PngImage class has now exposed the BackgroundColor property to get/set the PNG image's background color.
## **Removed Properties**
### **Property CadRasterizationOptions.LayoutName Removed**
The property Aspose.Imaging.ImageOptions.CadRasterizationOptions.LayoutName has been replaced by the Aspose.Imaging.ImageOptions.CadRasterizationOptions.Layouts property that can be used to specify one or more layout names for the CAD to PDF & CAD to raster image conversion.
### **Property PngOptions.TransparentColor Removed**
The property Aspose.Imaging.ImageOptions.PngOptions.TransparentColor has been replaced by the Aspose.Imaging.FileFormats.Png.PngImage.HasTransparentColor and Aspose.Imaging.FileFormats.Png.PngImage.TransparentColor properties for better understanding.
