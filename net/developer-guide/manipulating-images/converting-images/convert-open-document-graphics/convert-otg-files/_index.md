---
title: Convert OTG files
type: docs
weight: 20
url: /net/convert-otg-files/
---

## **Convert OTG files**
Aspose.Imaging for .NET now supports converting images from OTG to PDF and other image formats. Following code snippet demonstrates the said functionality.

{{< highlight java >}}

 			string fileName = "VariousObjectsMultiPage.otg";

            string inputFileName = Path.Combine(dataDir, fileName);

            ImageOptionsBase[] options = { new PngOptions(), new PdfOptions() };

            foreach (ImageOptionsBase item in options)

            {                

                string fileExt = item is PngOptions ? ".png" : ".pdf";                

                using (Image image = Image.Load(inputFileName))

                {

                    OtgRasterizationOptions otgRasterizationOptions = new OtgRasterizationOptions();

                    otgRasterizationOptions.PageSize = image.Size;

                    item.VectorRasterizationOptions = otgRasterizationOptions;

                    image.Save(Path.Combine("c:/", "output" + fileExt), item);

                }

            }

{{< /highlight >}}
