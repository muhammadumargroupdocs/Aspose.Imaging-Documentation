---
title: Converting DjVu to PDF Format in PHP
type: docs
weight: 10
url: /java/converting-djvu-to-pdf-format-in-php/
---

## **Aspose.Imaging - Converting DjVu to PDF Format**
To Convert DjVu to PDF Format using **Aspose.Imaging Java for PHP**, simply invoke **ConvertingDjVuToPdf** module. Here you can see example code.

**PHP Code**

{{< highlight php >}}

 # Load an existing image (of type bmp) in an instance of Image class

$image=new Image();

$image = $image->load($dataDir."demo.djvu");

\# Create an instance of PdfOptions

$export_options = new PdfOptions();

\# Initialize the metadata for Pdf document

$export_options->setPdfDocumentInfo(new PdfDocumentInfo());

\# Create an instance of IntRange and initialize it with the range of DjVu pages to be exported

#range = Rjb::import('com.aspose.imaging.IntRange').new(0, 5) # Export first 5 pages

$range = array(0,1,2,3,4);

\# Initialize an instance of DjvuMultiPageOptions with range of DjVu pages to be exported

$export_options->setMultiPageOptions(new DjvuMultiPageOptions($range));

\# Save the result in PDF format

$image->save($dataDir."djvu.pdf", $export_options);

\# Display Status.

print "Converted DjVu to PDF successfully!".PHP_EOL;

{{< /highlight >}}
## **Download Running Code**
Download **Converting DjVu to PDF Format (Aspose.Imaging)** from any of the below mentioned social coding sites:

- [GitHub](https://github.com/asposeimaging/Aspose.Imaging-for-Java/blob/master/Plugins/Aspose_Imaging_Java_for_PHP/src/aspose/imaging/ManagingDjVuFormat/ConvertingDjVutoPDF.php)
- [CodePlex](https://asposeimagingjavaphp.codeplex.com/SourceControl/latest#src/aspose/imaging/ManagingDjVuFormat/ConvertingDjVutoPDF.php)
