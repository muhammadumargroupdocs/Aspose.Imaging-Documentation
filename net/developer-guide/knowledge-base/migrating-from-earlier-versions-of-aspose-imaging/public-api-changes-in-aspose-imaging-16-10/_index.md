---
title: Public API Changes in Aspose.Imaging 16.10
type: docs
weight: 80
url: /net/public-api-changes-in-aspose-imaging-16-10/
---

{{% alert color="primary" %}} 

This document describes changes to the Aspose.Imaging API in version 16.10, that may be of interest to module/application developers. It includes not only new and updated public methods, but also a description of any changes in the behavior behind the scenes in Aspose.Imaging.

{{% /alert %}} 
### **Added APIs:**
Class Aspose.Imaging.FileFormats.Wmf.Graphics.WmfRecorderGraphics2D
Method Aspose.Imaging.FileFormats.Emf.Graphics.MetafileRecorderGraphics2D.DrawString (System.String,Aspose.Imaging.Font,Aspose.Imaging.Color,System.Int32,System.Int32,System.Single)
Method Aspose.Imaging.FileFormats.Emf.Graphics.MetafileRecorderGraphics2D.FillEllipse (Aspose.Imaging.Brush,Aspose.Imaging.Rectangle)
Method Aspose.Imaging.FileFormats.Psd.PsdImage.Crop(Aspose.Imaging.Rectangle)
Method Aspose.Imaging.FileFormats.Psd.PsdImage.ResizeHeightProportionally](System.Int32,Aspose.Imaging.ImageResizeSettings)
Method Aspose.Imaging.FileFormats.Psd.PsdImage.ResizeHeightProportionally](System.Int32,Aspose.Imaging.ResizeType)
Method Aspose.Imaging.FileFormats.Psd.PsdImage.ResizeWidthProportionally](System.Int32,Aspose.Imaging.ImageResizeSettings)
Method Aspose.Imaging.FileFormats.Psd.PsdImage.ResizeWidthProportionally](System.Int32,Aspose.Imaging.ResizeType)
Method Aspose.Imaging.FileFormats.Psd.PsdImage.Rotate(System.Single)
Method Aspose.Imaging.FileFormats.Psd.PsdImage.Rotate(System.Single,System.Boolean,Aspose.Imaging.Color)
Method Aspose.Imaging.FileFormats.Wmf.Graphics.WmfRecorderGraphics2D.#ctor(Aspose.Imaging.Rectangle,System.Int32)
Method Aspose.Imaging.FileFormats.Wmf.Graphics.WmfRecorderGraphics2D.EndRecording
Property Aspose.Imaging.FileFormats.Psd.Layers.Layer.IsVisible
Property Aspose.Imaging.FileFormats.Psd.Layers.Layer.IsVisibleInGroup
Property Aspose.Imaging.FileFormats.Wmf.Graphics.WmfRecorderGraphics2D.BackgroundMode
Property Aspose.Imaging.ImageOptions.PsdOptions.RefreshImagePreviewData
Property Aspose.Imaging.ImageOptions.PsdOptions.RemoveGlobalTextEngineResource
### **Removed APIs:**
Method Aspose.Imaging.FileFormats.Emf.Graphics.MetafileRecorderGraphics2D.FillEllipse(Aspose.Imaging.Brush,Aspose.Imaging.RectangleF)
Property Aspose.Imaging.FileFormats.Emf.Emf.Records.EmfCommentMultiFormats.CountFormats
Property Aspose.Imaging.FileFormats.Emf.EmfPlus.Objects.EmfPlusBlendBase.PositionCount
Property Aspose.Imaging.FileFormats.Emf.EmfPlus.Objects.EmfPlusBoundaryPathData.BoundaryPathSize
Property Aspose.Imaging.FileFormats.Emf.EmfPlus.Objects.EmfPlusBoundaryPointData.BoundaryPointCount
Property Aspose.Imaging.FileFormats.Emf.EmfPlus.Objects.EmfPlusCompoundLineData.CompoundLineDataSize
Property Aspose.Imaging.FileFormats.Emf.EmfPlus.Objects.EmfPlusCustomEndCapData.CustomEndCapSize
Property Aspose.Imaging.FileFormats.Emf.EmfPlus.Objects.EmfPlusCustomStartCapData.CustomStartCapSize
Property Aspose.Imaging.FileFormats.Emf.EmfPlus.Objects.EmfPlusDashedLineData.DashedLineDataSize
Property Aspose.Imaging.FileFormats.Emf.EmfPlus.Objects.EmfPlusFillPath.FillPathLength
Property Aspose.Imaging.FileFormats.Emf.EmfPlus.Objects.EmfPlusLinePath.LinePathLength
Property Aspose.Imaging.FileFormats.Emf.EmfPlus.Objects.EmfPlusPalette.PaletteCount
Property Aspose.Imaging.FileFormats.Emf.EmfPlus.Objects.EmfPlusPathGradientBrushData.SurroundingColorCount
Property Aspose.Imaging.FileFormats.Emf.EmfPlus.Objects.EmfPlusRegion.RegionNodeCount
Property Aspose.Imaging.FileFormats.Emf.EmfPlus.Objects.EmfPlusRegionNodePath.RegionNodePathLength
