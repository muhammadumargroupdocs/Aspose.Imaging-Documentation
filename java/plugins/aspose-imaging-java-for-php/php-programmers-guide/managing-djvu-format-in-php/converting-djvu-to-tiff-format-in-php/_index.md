---
title: Converting DjVu to TIFF Format in PHP
type: docs
weight: 20
url: /java/converting-djvu-to-tiff-format-in-php/
---

## **Aspose.Imaging - Converting DjVu to TIFF Format**
To Convert DjVu to TIFF Format using **Aspose.Imaging Java for PHP**, simply invoke **ConvertingDjVuToTiff** module. Here you can see example code.

**PHP Code**

{{< highlight php >}}

 # Load an existing image (of type bmp) in an instance of Image class

$image=new Image();

$image = $image->load($dataDir . "Sample.djvu");

\# Create an instance of TiffOptions & use preset options for Black n While with Deflate compression

$tiff_expected_format = new TiffExpectedFormat();

$export_options = new TiffOptions($tiff_expected_format->TiffDeflateBW);

\# Initialize an instance of DjvuMultiPageOptions

$export_options->setMultiPageOptions(new DjvuMultiPageOptions());

\# Save the result in PDF format

$image->save($dataDir."djvu.tiff", $export_options);

\# Display Status.

print "Converted DjVu to Tiff successfully!".PHP_EOL;

{{< /highlight >}}
## **Download Running Code**
Download **Converting DjVu to TIFF Format (Aspose.Imaging)** from any of the below mentioned social coding sites:

- [GitHub](https://github.com/asposeimaging/Aspose.Imaging-for-Java/blob/master/Plugins/Aspose_Imaging_Java_for_PHP/src/aspose/imaging/ManagingDjVuFormat/ConvertingDjVuToTiff.php)
- [CodePlex](https://asposeimagingjavaphp.codeplex.com/SourceControl/latest#src/aspose/imaging/ManagingDjVuFormat/ConvertingDjVuToTiff.php)
