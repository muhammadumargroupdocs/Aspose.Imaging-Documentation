---
title: Public API Changes in Aspose.Imaging 17.01
type: docs
weight: 70
url: /net/public-api-changes-in-aspose-imaging-17-01/
---

{{% alert color="primary" %}} 

This document describes changes to the Aspose.Imaging API in version 17.01, that may be of interest to module/application developers. It includes not only new and updated public methods, but also a description of any changes in the behavior behind the scenes in Aspose.Imaging.

{{% /alert %}} 
## **Added APIs:**
Class Aspose.Imaging.FileFormats.Pdf.PdfCoreOptions
Class Aspose.Imaging.FileFormats.Psd.Layers.LayerFlags
Class Aspose.Imaging.FileFormats.Psd.Layers.LayerGroup
Field/Enum Aspose.Imaging.FileFormats.Jpeg.JpegCompressionMode.Lossless
Field/Enum Aspose.Imaging.FileFormats.Psd.Layers.LayerFlags.HasUsefulInformation
Field/Enum Aspose.Imaging.FileFormats.Psd.Layers.LayerFlags.Obsolete
Field/Enum Aspose.Imaging.FileFormats.Psd.Layers.LayerFlags.PixelDataIrrelevantToAppearenceInDocument
Field/Enum Aspose.Imaging.FileFormats.Psd.Layers.LayerFlags.TransparencyProtected
Field/Enum Aspose.Imaging.FileFormats.Psd.Layers.LayerFlags.Undocumented
Field/Enum Aspose.Imaging.FileFormats.Psd.Layers.LayerFlags.Visible
Method Aspose.Imaging.FileFormats.Pdf.PdfCoreOptions.#ctor
Method Aspose.Imaging.FileFormats.Psd.Layers.Layer.#ctor(Aspose.Imaging.Rectangle,System.Byte[],System.Byte[],System.Byte[],System.String)
Method Aspose.Imaging.FileFormats].Psd.Layers.Layer.AddLayerMask(Aspose.Imaging.FileFormats.Psd.Layers.LayerMaskData)
Method Aspose.Imaging.FileFormats.Psd.Layers.Layer.Equals(System.Object)
Method Aspose.Imaging.FileFormats.Psd.Layers.Layer.GetHashCode
Method Aspose.Imaging.FileFormats.Psd.Layers.LayerGroup.AddLayer(Aspose.Imaging.FileFormats.Psd.Layers.Layer)
Method Aspose.Imaging.FileFormats].Psd.[PsdImage](/pages/createpage.action?spaceKey=imagingnet&title=PsdImage&linkCreation=true&fromPageId=22971011).[AddLayerGroup](/pages/createpage.action?spaceKey=imagingnet&title=AddLayerGroup&linkCreation=true&fromPageId=22971011)(System.String,System.Int32,System.Boolean)
Property Aspose.Imaging.FileFormats.Pdf.PdfCoreOptions.BookmarksOutlineLevel
Property Aspose.Imaging.FileFormats.Pdf.PdfCoreOptions.ExpandedOutlineLevels
Property Aspose.Imaging.FileFormats.Pdf.PdfCoreOptions.HeadingsOutlineLevels
Property Aspose.Imaging.FileFormats.Pdf.PdfCoreOptions.JpegQuality
Property Aspose.Imaging.FileFormats.Png.PngImage.Interlaced
Property Aspose.Imaging.FileFormats.Psd.Layers.LayerGroup.Layers
Property Aspose.Imaging.FileFormats.Psd.Layers.LayerMaskData.ImageData
Property Aspose.Imaging.ImageOptions.JpegOptions.BitsPerChannel
Property Aspose.Imaging.ImageOptions.PdfOptions.PdfCoreOptions
## **Removed APIs:**
Property Aspose.Imaging.ImageOptions.PdfOptions.CorePdfOptions
