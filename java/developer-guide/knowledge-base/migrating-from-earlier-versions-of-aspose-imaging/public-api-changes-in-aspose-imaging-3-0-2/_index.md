---
title: Public API Changes in Aspose.Imaging 3.0.2
type: docs
weight: 120
url: /java/public-api-changes-in-aspose-imaging-3-0-2/
---

{{% alert color="primary" %}} 

This document describes the changes to the Aspose.Imaging API from version 3.0.1 to 3.0.2 that may be of interest to module/application developers. It includes new and updated public methods, [added APIs](/imaging/java/public-api-changes-in-aspose-imaging-3-0-2-html/) and [removed APIs](/imaging/java/public-api-changes-in-aspose-imaging-3-0-2-html/), but also a description of any changes in the behavior behind the scenes in Aspose.Imaging.

{{% /alert %}} 
## **Added Methods**
### **Support for Metafile Font Information**
Aspose.Imaging for Java 3.0.2 has introduced a series of new classes & methods access the metafile font related information. Details of newly added APIs are as follow:

- Method com.aspose.imaging.fileformats.metafile.EmfMetafileImage.getUsedFonts
- Method com.aspose.imaging.fileformats.metafile.EmfMetafileImage.getMissedFonts
- Class com.aspose.imaging.fileformats.metafile.FontSettings
- Method com.aspose.imaging.fileformats.metafile.FontSettings.getFontsSources
- Method com.aspose.imaging.fileformats.metafile.FontSettings.removeFontsFolder(java.lang.String)
- Method com.aspose.imaging.fileformats.metafile.FontSettings.useJavaFontEngine(boolean)
- Method com.aspose.imaging.fileformats.metafile.FontSettings.isJavaFontEngineUsed
- Method com.aspose.imaging.fileformats.metafile.FontSettings.resetFontSources
- Method com.aspose.imaging.fileformats.metafile.FontSettings.findFont(java.util.Map)
- Method com.aspose.imaging.fileformats.metafile.FontSettings.findFont(java.lang.String,int,int)
- Method com.aspose.imaging.fileformats.metafile.FontSettings.getAllFonts
- Method com.aspose.imaging.fileformats.metafile.MetafileImage.getUsedFonts
- Method com.aspose.imaging.fileformats.metafile.MetafileImage.getMissedFonts
- Method com.aspose.imaging.fileformats.metafile.WmfMetafileImage.getUsedFonts
- Method com.aspose.imaging.fileformats.metafile.WmfMetafileImage.getMissedFonts
- Method com.aspose.imaging.fileformats.metafile.FontSettings.addFontsFolder(java.lang.String)
- Method com.aspose.imaging.fileformats.metafile.FontSettings.setFontsFolders(java.lang.String[])
- Method com.aspose.imaging.fileformats.metafile.FontSettings.setFontsFolder(java.lang.String)
- Method com.aspose.imaging.fileformats.metafile.FontSettings.addFontSubstitutes(java.lang.String,java.lang.String[])
- Method com.aspose.imaging.fileformats.metafile.FontSettings.getFontSubstitutes(java.lang.String)
- Method com.aspose.imaging.fileformats.metafile.FontSettings.setFontSubstitutes(java.lang.String,java.lang.String[])
- Method com.aspose.imaging.fileformats.metafile.FontSettings.getDefaultFontName
- Method com.aspose.imaging.fileformats.metafile.FontSettings.setDefaultFontName(java.lang.String)
