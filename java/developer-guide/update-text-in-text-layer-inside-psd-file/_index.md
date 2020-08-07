---
title: Update Text In Text Layer Inside PSD File
type: docs
weight: 60
url: /java/update-text-in-text-layer-inside-psd-file/
---

{{% alert color="primary" %}} 

Aspose.Imaging for Java allows you to manipulate the text in the text layer of a PSD file. com.aspose.imaging.fileformats.psd.Layers.TextLayer class can be used to update text in text layer inside PSD.

{{% /alert %}} 
#### **Updating Text In Text Layer Inside PSD File**
The following sample code loads a PSD file, access the text layer, update the text and save the PSD file with a new name using com.aspose.imaging.fileformats.psd.Layers.TextLayer.UpdateText method.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-Photoshop-UpdateTextInTextLayerInsidePSDFile-UpdateTextInTextLayerInsidePSDFile.java" >}}
#### **Additional Options**
Some times while updating text in text layer may damage file and you may not be able to view the updated result. To avoid/correct such behavior Aspose.Imaging has introduced some additional options.

- Method **setRemoveGlobalTextEngineResource** has been introduced. The purpose of this method is to inform that global text resources must be removed. By default its value is FALSE. You may call this method and pass TRUE to remove global text resources.
- Method **setRefreshImagePreviewData** has been introduced. The purpose of this method is to render final image data section. This will make PSD file compatible with image viewing tools that uses only Image data section. By default its value is TRUE.

Following is the sample code demonstrating how to call **setRemoveGlobalTextEngineResource** method.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-Photoshop-AdditionalOptions-AdditionalOptions.java" >}}
