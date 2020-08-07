---
title: Public API Changes in Aspose.Imaging 3.1.0
type: docs
weight: 120
url: /net/public-api-changes-in-aspose-imaging-3-1-0/
---

{{% alert color="primary" %}} 

This document describes the changes to the Aspose.Imaging API from version 3.0.0 to 3.1.0 that may be of interest to module/application developers. It includes not only new and updated public methods, [added APIs](/imaging/net/public-api-changes-in-aspose-imaging-3-1-0-html/) and [removed APIs](/imaging/net/public-api-changes-in-aspose-imaging-3-1-0-html/), but also a description of any changes in the behavior behind the scenes in Aspose.Imaging.

{{% /alert %}} 
## **Added Classes, Enumerations and Methods**
### **Support for Raster Operations on PSD Layers**
Aspose.Imaging for .NET 3.1.0 has introduced a series of new classes, methods, enumerations and properties to process PSD layers as raster images. The class Aspose.Imaging.FileFormats.Psd.Layers.Layer is now inherited from Aspose.Imaging.RasterCachedImage. This means that all operations that we could do on a raster image are now possible on each layer of a PSD image. Details of newly added APIs are as follow:

- Method Aspose.Imaging.FileFormats.Psd.PsdImage.AdjustBrightness(System.Int32)
- Method Aspose.Imaging.FileFormats.Psd.PsdImage.AdjustContrast(System.Single)
- Method Aspose.Imaging.FileFormats.Psd.PsdImage.AdjustGamma(System.Single)
- Method Aspose.Imaging.FileFormats.Psd.PsdImage.AdjustGamma(System.Single,System.Single,System.Single)
- Method Aspose.Imaging.FileFormats.Psd.PsdImage.BinarizeFixed(System.Byte)
- Method Aspose.Imaging.FileFormats.Psd.PsdImage.BinarizeOtsu
- Method {{Aspose.Imaging.FileFormats.Psd.PsdImage.Dither(Aspose.Imaging.DitheringMethod,System.Int32,Aspose.Imaging.IColorPalette)
- Method Aspose.Imaging.FileFormats.Psd.PsdImage.Grayscale
- Property Aspose.Imaging.FileFormats.Psd.Layers.Layer.BitsPerPixel
- Property Aspose.Imaging.FileFormats.Psd.Layers.Layer.Height
- Property Aspose.Imaging.FileFormats.Psd.Layers.Layer.LayerBounds
- Property Aspose.Imaging.FileFormats.Psd.Layers.Layer.LayerOptions
- Property Aspose.Imaging.FileFormats.Psd.Layers.Layer.Width
- Property Aspose.Imaging.FileFormats.Psd.PsdImage.ActiveLayer
### **Export AutoCAD 3D Entities to PDF**
Aspose.Imaging for .NET 3.1.0 has introduced some new classes, methods, enumerations and properties to add support for conversion of 3D entities in AutoCAD DXF drawings. Now 3D entities can be exported into PDF CadRasterizationOptions.

- Class Aspose.Imaging.ImageOptions.TypeOfEntities
- Field/Enum Aspose.Imaging.FileFormats.Cad.CadConsts.CadEntityTypeName.EXTRUDEDSURFACE
- Field/Enum Aspose.Imaging.FileFormats.Cad.CadConsts.CadEntityTypeName.PLANESURFACE
- Field/Enum Aspose.Imaging.FileFormats.Cad.CadConsts.CadEntityTypeName.REVOLVEDSURFACE
- Field/Enum Aspose.Imaging.FileFormats.Cad.CadConsts.CadEntityTypeName.SWEPTSURFACE
- Field/Enum Aspose.Imaging.FileFormats.Cad.CadConsts.CadSubClassName.SURFACEPLANAR
- Field/Enum Aspose.Imaging.ImageOptions.TypeOfEntities.Entities2D
- Field/Enum Aspose.Imaging.ImageOptions.TypeOfEntities.Entities3D
- Property Aspose.Imaging.ImageOptions.CadRasterizationOptions.TypeOfEntities
## **Removed Classes and Properties**
### **Class CadSurfaceBase**
The class Aspose.Imaging.FileFormats.Cad.CadObjects.CadSurfaceBase was unused, and so removed. Details of related removed APIs are as follow:

- Class Aspose.Imaging.FileFormats.Cad.CadObjects.CadSurfaceBase
- Field/Enum Aspose.Imaging.FileFormats.Cad.CadConsts.CadSubClassName.SURFACEBASE
- Method Aspose.Imaging.FileFormats.Cad.CadObjects.CadSurfaceBase.#ctor
### **Old Dithering Properties**
The dithering process is now more optimized and predictable. All you need to do is use a new Dither() method instead the old DitheringSettings and RawDitheringMethod properties. The dithering then performed right in-place and you can then review the dithering results by loading pixels or raw data. Additionally the DitheringMethod enum is moved to Aspose.Imaging namespace.

- Property Aspose.Imaging.FileFormats.Gif.GifImage.DitheringSettings
- Property Aspose.Imaging.FileFormats.Tiff.TiffImage.DitheringSettings
- Property Aspose.Imaging.RasterImage.DitheringSettings
- Property Aspose.Imaging.RasterImage.RawDitheringMethod
