---
title: Public API Changes in Aspose.Imaging 2.6.0
type: docs
weight: 170
url: /net/public-api-changes-in-aspose-imaging-2-6-0/
---

{{% alert color="primary" %}} 

This document describes the changes to the Aspose.Imaging API from version 2.5.0 to 2.6.0 that may be of interest to module/application developers. It includes not only new and updated public methods, [added classes etc.](/imaging/net/public-api-changes-in-aspose-imaging-2-6-0-html/) and [renamed classes etc.](/imaging/net/public-api-changes-in-aspose-imaging-2-6-0-html/), but also a description of any changes in the behavior behind the scenes in Aspose.Imaging.

{{% /alert %}} 
## **Added Classes, Enumerations and Methods**
### **Classes VectorRasterizationOptions & CadRasterizationOptions Added**
The new classes VectorRasterizationOptions and CadRasterizationOptions has been added to the Aspose.Imaging.ImageOptions in order to facilitate the user with CAD to vector & CAD to raster conversion. Moreover, some members of the PdfOptions class has been moved to the aforesaid classes.

With these changes in place, the CAD to PDF conversion can now be achieved as follow.

**C#**

{{< highlight csharp >}}

 string sourceFilePath = myDir + "office.dwg";

using (Aspose.Imaging.Image image = Aspose.Imaging.Image.Load(sourceFilePath))

{

    //Create an instance of CadRasterizationOptions and set its various properties

    Aspose.Imaging.ImageOptions.CadRasterizationOptions rasterizationOptions = new Aspose.Imaging.ImageOptions.CadRasterizationOptions();

    rasterizationOptions.BackgroundColor = Aspose.Imaging.Color.White;

    rasterizationOptions.PageWidth = 1600;

    rasterizationOptions.PageHeight = 1600;

    rasterizationOptions.DrawType = Aspose.Imaging.FileFormats.Cad.CadDrawTypeMode.UseObjectColor;

    rasterizationOptions.Layers = new List<string> { "layer1" };

    rasterizationOptions.LayoutName = "layout1";

    //Create an instance of PdfOptions

    Aspose.Imaging.ImageOptions.PdfOptions pdfOptions = new Aspose.Imaging.ImageOptions.PdfOptions();

    //Set the VectorRasterizationOptions property

    pdfOptions.VectorRasterizationOptions = rasterizationOptions;

    //Export the DWG to PDF

    image.Save(myDir + "result.pdf", pdfOptions);

}

{{< /highlight >}}

**Visual Basic**

{{< highlight csharp >}}

 Dim sourceFilePath As String = myDir & "office.dwg"

Using image As Aspose.Imaging.Image = Aspose.Imaging.Image.Load(sourceFilePath)

	'Create an instance of CadRasterizationOptions and set its various properties

	Dim rasterizationOptions As New Aspose.Imaging.ImageOptions.CadRasterizationOptions()

	rasterizationOptions.BackgroundColor = Aspose.Imaging.Color.White

	rasterizationOptions.PageWidth = 1600

	rasterizationOptions.PageHeight = 1600

	rasterizationOptions.DrawType = Aspose.Imaging.FileFormats.Cad.CadDrawTypeMode.UseObjectColor

	rasterizationOptions.Layers = New List(Of String) (New String() {"layer1"})

	rasterizationOptions.LayoutName = "layout1"

	'Create an instance of PdfOptions

	Dim pdfOptions As New Aspose.Imaging.ImageOptions.PdfOptions()

	'Set the VectorRasterizationOptions property

	pdfOptions.VectorRasterizationOptions = rasterizationOptions

	'Export the DWG to PDF

	image.Save(myDir & "result.pdf", pdfOptions)

End Using

{{< /highlight >}}
### **Support for Binary DXF Format Added**
In order to provide the support for Binary DXF file format, Aspose.Imaging for .NET 2.6.0 has added the following classes & enumerations to the public API.

1. Class Aspose.Imaging.FileFormats.Cad.CadBinaryCodeValue
1. Class Aspose.Imaging.FileFormats.Cad.CadConsts.DxfFileFormat
1. Class Aspose.Imaging.FileFormats.Cad.CadParameters.CadBinaryParameter
1. Enum Aspose.Imaging.FileFormats.Cad.CadConsts.CadGroupCodeTypes
### **Methods ResizeWidthProportionally & ResizeHeightProportionally Added**
The Aspose.Imaging.Image class has now exposed the ResizeWidthProportionally and ResizeHeightProportionally with the release of Aspose.Imaging 2.6.0 to assist with the re-sizing operation while keeping the aspect ratio. The aforesaid methods requires only one parameter (either Height or Width) and automatically calculates the other value.
### **Methods GetProportionalWidth & GetProportionalHeight Added**
The class Aspose.Imaging.Image has exposed GetProportionalWidth & GetProportionalHeight methods to calculate proportional width or height.

**C#**

{{< highlight csharp >}}

 int newHeight = Image.GetProportionalHeight(150, 120, 100);  // 80

int newWIdth = Image.GetProportionalWidth(150, 120, 60);  // 75

{{< /highlight >}}

**Visual Basic**

{{< highlight csharp >}}

 Dim newHeight As Integer = Image.GetProportionalHeight(150, 120, 100) ' 80

Dim newWIdth As Integer = Image.GetProportionalWidth(150, 120, 60) ' 75

{{< /highlight >}}
## **Renamed Properties, Enumerations and Parameters**
### **Enumeration CadIntegralParamType Renamed to CadIntegralParameterType**
Use new CadIntegralParameterType definition as follow.

**C#**

{{< highlight csharp >}}

 CadBinaryCodeValue binaryCode = new CadBinaryCodeValue(CadIntegralParameterType.Boolean, this.code, this.buffer, dataSize);

{{< /highlight >}}

**Visual Basic**

{{< highlight csharp >}}

 Dim binaryCode As New CadBinaryCodeValue(CadIntegralParameterType.Boolean, Me.code, Me.buffer, dataSize)

{{< /highlight >}}
### **Property CadParameter.Setted Renamed to CadParameter.IsSet**
The Aspose.Imaging.FileFormats.Cad.CadParameters.CadParameter.Setted property has been renamed to Aspose.Imaging.FileFormats.Cad.CadParameters.CadParameter.IsSet for better understanding.

**C#**

{{< highlight csharp >}}

 if(this.scaleX.IsSet)

{

  // Scale check

}

{{< /highlight >}}

**Visual Basic**

{{< highlight csharp >}}

 If Me.scaleX.IsSet Then

  ' Scale check

End If

{{< /highlight >}}
### **Parameter Changed from System.IO.SeekOrigin to Aspose.Imaging.SeekOrigin**
Since v2.6.0 of Aspose.Imaging for .NET, the StreamContainer.Seek parameter changed from System.IO.SeekOrigin to Aspose.Imaging.SeekOrigin.

**C#**

{{< highlight csharp >}}

 streamContainer.Seek(14, Aspose.Imaging.SeekOrigin.Begin);

{{< /highlight >}}

**Visual Basic**

{{< highlight csharp >}}

 streamContainer.Seek(14, Aspose.Imaging.SeekOrigin.Begin)

{{< /highlight >}}
