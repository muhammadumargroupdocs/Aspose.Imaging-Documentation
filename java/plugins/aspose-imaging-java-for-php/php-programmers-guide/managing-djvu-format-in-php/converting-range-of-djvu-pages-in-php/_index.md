---
title: Converting Range of DjVu Pages in PHP
type: docs
weight: 30
url: /java/converting-range-of-djvu-pages-in-php/
---

## **Aspose.Imaging - Converting Range of DjVu Pages**
To Convert Range of DjVu Pages using **Aspose.Imaging Java for PHP**, simply invoke **ConvertingRangeOfDjVuPages** module. Here you can see example code.

**PHP Code**

{{< highlight php >}}

 # Load an existing image (of type bmp) in an instance of Image class

$image=new Image();

$image = $image->load($dataDir."demo.djvu");

\# Create an instance of TiffOptions & use preset options for Black n While with Deflate compression

$tiff_expected_format = new TiffExpectedFormat();

$export_options = new TiffOptions($tiff_expected_format->TiffDeflateBW);

\# Create an instance of IntRange and initialize it with range of pages to be exported

$range = [0,1]; #Export first 2 pages

\# Initialize an instance of DjvuMultiPageOptions

$export_options->setMultiPageOptions(new DjvuMultiPageOptions($range));

\# Save the result in PDF format

$image->save($dataDir."PagesRange.tiff", $export_options);

\# Display Status.

print "Converted range of DjVu pages successfully!".PHP_EOL;

{{< /highlight >}}
## **Download Running Code**
Download **Converting Range of DjVu Pages (Aspose.Imaging)** from any of the below mentioned social coding sites:

- [GitHub](https://github.com/asposeimaging/Aspose.Imaging-for-Java/blob/master/Plugins/Aspose_Imaging_Java_for_PHP/src/aspose/imaging/ManagingDjVuFormat/ConvertingRangeOfDjVuPages.php)
- [CodePlex](https://asposeimagingjavaphp.codeplex.com/SourceControl/latest#src/aspose/imaging/ManagingDjVuFormat/ConvertingRangeOfDjVuPages.php)
