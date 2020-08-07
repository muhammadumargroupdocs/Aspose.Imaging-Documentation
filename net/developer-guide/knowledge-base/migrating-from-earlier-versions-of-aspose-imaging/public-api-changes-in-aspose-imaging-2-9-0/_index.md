---
title: Public API Changes in Aspose.Imaging 2.9.0
type: docs
weight: 140
url: /net/public-api-changes-in-aspose-imaging-2-9-0/
---

{{% alert color="primary" %}} 

This document describes the changes to the Aspose.Imaging API from version 2.8.0 to 2.9.0 that may be of interest to module/application developers. It includes not only new and updated public methods, [added APIs](/imaging/net/public-api-changes-in-aspose-imaging-2-9-0-html/) but also a description of any changes in the behavior behind the scenes in Aspose.Imaging.

{{% /alert %}} 
## **Added Methods and Properties**
### **Methods GetDefaultRawData Added**
Aspose.Imaging for .NET 2.9.0 has introduced two overload version of Aspose.Imaging.RasterImage.GetDefaultRawData method that could be of help in retrieving empty raw data when image is created from scratch. Below are the signature for both overloads.

- Aspose.Imaging.RasterImage.GetDefaultRawData(Aspose.Imaging.Rectangle,Aspose.Imaging.IPartialRawDataLoader,Aspose.Imaging.RawDataSettings)
- Aspose.Imaging.RasterImage.GetDefaultRawData(Aspose.Imaging.Rectangle,Aspose.Imaging.RawDataSettings)
### **Property AutomaticLayoutsScaling Added**
Property Aspose.Imaging.ImageOptions.CadRasterizationOptions.AutomaticLayoutsScaling has been added to perform auto layouts scaling for CAD images. This property could be of help in scenarios where scale for layouts differs from the scale for Model sheet. 

Default value is false and layouts are scaled in a same manner as Model sheet.

**C#**

{{< highlight csharp >}}

 using (CadImage cadImage = (CadImage)Image.Load(fileName))

{

    PdfOptions pdfOptions = new PdfOptions();

    pdfOptions.VectorRasterizationOptions = new CadRasterizationOptions();

    CadRasterizationOptions cadRasterizationOptions = (CadRasterizationOptions)pdfOptions.VectorRasterizationOptions;

    cadRasterizationOptions.AutomaticLayoutsScaling = true;

    cadImage.Save(outPath, pdfOptions);

}

{{< /highlight >}}

**VB.NET**

{{< highlight csharp >}}

 Using cadImage As CadImage = CType(Image.Load(fileName), CadImage)

	Dim pdfOptions As New PdfOptions()

	pdfOptions.VectorRasterizationOptions = New CadRasterizationOptions()

	Dim cadRasterizationOptions As CadRasterizationOptions = CType(pdfOptions.VectorRasterizationOptions, CadRasterizationOptions)

	cadRasterizationOptions.AutomaticLayoutsScaling = True

	cadImage.Save(outPath, pdfOptions)

End Using

{{< /highlight >}}
