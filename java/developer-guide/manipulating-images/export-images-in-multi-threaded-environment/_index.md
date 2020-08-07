---
title: Export Images in Multi Threaded Environment
type: docs
weight: 110
url: /java/export-images-in-multi-threaded-environment/
---

## **Export Images in Multi Threaded Environment**
Aspose.Imaging for Java now supports converting images in multi threaded environment. Aspose.Imaging for Java ensure the optimized performance of operations during execution of code in multi-threaded environment. All imaging option classes (e.g. BmpOptions, TiffOptions, JpegOptions, etc.) in the Aspose.Imaging for Java now implement **com.aspose.imaging.system.IDisposable** interface. Therefore it is a must that developer properly dispose off the imaging options class object in case **Source** property is set. Following code snippet demonstrates the said functionality.

{{< gist "aspose-com-gists" "07be292db0a393dc95f153f84b28c069" "Examples-src-main-java-com-aspose-imaging-examples-ConvertingImages-ExportImagesInMultiThreadedEnvironment-ExportImagesInMultiThreadedEnvironment.java" >}}
## **Synchronize Access to Source Stream**
Aspose.Imaging now supports **getSyncRoot** property while working in multi-threaded environment. Developer can use this property to synchronize access to the source stream. Following code snippet demonstrates how the **getSyncRoot** property can be used.

{{< gist "aspose-com-gists" "07be292db0a393dc95f153f84b28c069" "Examples-src-main-java-com-aspose-imaging-examples-ConvertingImages-SyncRootProperty-ExportImagesInMultiThreadedEnvironment.java" >}}
