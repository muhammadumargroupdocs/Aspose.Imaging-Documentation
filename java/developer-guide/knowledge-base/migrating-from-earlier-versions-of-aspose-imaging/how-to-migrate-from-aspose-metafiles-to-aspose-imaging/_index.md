---
title: How to Migrate from Aspose.Metafiles to Aspose.Imaging
type: docs
weight: 190
url: /java/how-to-migrate-from-aspose-metafiles-to-aspose-imaging/
---

{{% alert color="primary" %}} 

From the release of Aspose.Imaging for Java 2.1.0, all Aspose.Metafile for Java packages have been merged and moved into Aspose.Imaging for Java. Migrating from legacy Aspose.Metafiles code to Aspose.Imaging 2.1.x or higher only requires a few changes in the existing code. This article provides a list of those changes and a class mapping for an overview of the changes.

{{% /alert %}} 
### **Notable Changes for Existing Users**
Since Aspose.Imaging has taken over the Aspose.Metafiles API, we have tried to keep everything as it was in Aspose.Metafiles API. However, a few changes were necessary. When migrating from Aspose.Metafiles to Aspose.Imaging, the following should be taken into account:

- The MetafileImage class no longer contains the write method, instead use the standard Aspose.Imaging approach using save method which provides the same functionality.
- The MetafileImage class no longer contains the static LoadMetafile method, instead use the standard factory method, Load, which provides the same functionality.
- The EmfMetafile and WmfMetafile classes have been renamed EmfMetafileImage and WmfMetafileImage respectively.
### **Import Statement**
**Java**

{{< highlight csharp >}}

 import com.aspose.imaging.*;

{{< /highlight >}}
### **Class Mapping Aspose.Metafiles to Aspose.Imaging**

|**Aspose.Metafiles** |**Aspose.Imaging** |**Remarks** |
| :- | :- | :- |
|com.aspose.metafiles.License|com.aspose.imaging.License|There is only one License class in the Aspose.Imaging for Java API to apply the license for all features including the ones related to metafiles. |
|com.aspose.metafiles.EmfMetafile|aspose.imaging.fileformats.metafile.EmfMetafileImage|The base class EmfMetafile has been renamed to EmfMetafileImage. All methods previously available under EmfMetafile class are now available in the EmfMetafileImage class. |
|com.aspose.metafiles.WmfMetafile|com.aspose.imaging.fileformats.metafile.WmfMetafileImage|The base class WmfMetafile has been renamed to WmfMetafileImage. All methods previously available under WmfMetafile class are now available in the WmfMetafileImage class. |
|com.aspose.metafiles.ColorMap|com.aspose.imaging.fileformats.metafile.ColorMap|Just the package was changed without any other notable changes in the interfaces or methods. |
|com.aspose.metafiles.MetafileCharsetCollection|com.aspose.imaging.fileformats.metafile.MetafileCharsetCollection|Just the package was changed without any other notable changes in the interfaces or methods. |
|com.aspose.metafiles.MetafileComment|com.aspose.imaging.fileformats.metafile.MetafileComment|Just the package was changed without any other notable changes in the interfaces or methods. |
|com.aspose.metafiles.TextOutOperation|com.aspose.imaging.fileformats.metafile.TextOutOperation|Just the package was changed without any other notable changes in the interfaces or methods. |
|com.aspose.metafiles.MetafilesException|com.aspose.imaging.exceptions.imageformats.MetafilesException|MetafilesException extends ImageException and handles all errors detected with metafiles. |
|com.aspose.metafiles.AsposeLicenseException|com.aspose.imaging.PleaseReportException|AsposeLicenseException class was removed when the Aspose.Metafiles packages were merged into Aspose.Imaging because Aspose.Imaging already handles license related errors through PleaseReportException class. |

