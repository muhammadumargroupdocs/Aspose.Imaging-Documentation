---
title: Converting Specific Portion of DjVu Page in Php
type: docs
weight: 50
url: /java/converting-specific-portion-of-djvu-page-in-php/
---

## **Aspose.Imaging - Converting Specific Portion of DjVu Page**
To Convert Specific Portion of DjVu Page using **Aspose.Imaging Java for PHP**, simply invoke **ConvertingSpecificPortionOfDjvuPage** module. Here you can see example code.

**PHP Code**

{{< highlight php >}}

 # Load an existing image (of type bmp) in an instance of Image class

$image=new Image();

$image = $image->load($dataDir."demo.djvu");

\# Create an instance of PngOptions

$export_options = new PngOptions();

\# Set ColorType to Grayscale

$pngColorType=new PngColorType();

$export_options->setColorType($pngColorType->Grayscale);

\# Create an instance of Rectangle and specify the portion on DjVu page

$export_area = new Rectangle(20, 20, 500, 500);

\# Specify the DjVu page index

$export_page_index = 2;

\# Initialize an instance of DjvuMultiPageOptions

\# while passing index of DjVu page index and instance of Rectangle covering the area to be exported

$export_options->setMultiPageOptions(new DjvuMultiPageOptions($export_page_index, $export_area));

\# Save the result in PDF format

$image->save($dataDir."SpecificPagePortion.png", $export_options);

\# Display Status.

print "Converted specific page portion DjVu page to image successfully!".PHP_EOL;

{{< /highlight >}}
## **Download Running Code**
Download **Converting Specific Portion of DjVu Page (Aspose.Imaging)** from any of the below mentioned social coding sites:

- [GitHub](https://github.com/asposeimaging/Aspose.Imaging-for-Java/blob/master/Plugins/Aspose_Imaging_Java_for_PHP/src/aspose/imaging/ManagingDjVuFormat/ConvertingSpecificPortionOfDjvuPage.php)
- [CodePlex](https://asposeimagingjavaphp.codeplex.com/SourceControl/latest#src/aspose/imaging/ManagingDjVuFormat/ConvertingSpecificPortionOfDjvuPage.php)
