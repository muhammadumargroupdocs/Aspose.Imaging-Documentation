---
title: Convert OTG files
type: docs
weight: 20
url: /java/convert-otg-files/
---

## **Convert OTG files**
Aspose.Imaging for Java now supports converting images from OTG to PDF and other image formats. Following code snippet demonstrates the said functionality.

{{< highlight java >}}

 import com.aspose.imaging.Image;

import com.aspose.imaging.ImageOptionsBase;

import com.aspose.imaging.Size;

import com.aspose.imaging.imageoptions.OtgRasterizationOptions;

import com.aspose.imaging.imageoptions.PdfOptions;

import com.aspose.imaging.imageoptions.PngOptions;


String dataDir = "D:/workDir/"; 

String fileName = "VariousObjectsMultiPage.otg";

String inputFileName = dataDir + fileName;

ImageOptionsBase[] options = { new PngOptions(), new PdfOptions() };

for (ImageOptionsBase item : options)

{

    String fileExt = item instanceof PngOptions ? ".png" : ".pdf";

    try (Image image = Image.load(inputFileName))

    {

        OtgRasterizationOptions otgRasterizationOptions = new OtgRasterizationOptions();

        otgRasterizationOptions.setPageSize(Size.to_SizeF(image.getSize()));

        item.setVectorRasterizationOptions(otgRasterizationOptions);

        image.save(dataDir + "output" + fileExt), item);

    }

}

{{< /highlight >}}




