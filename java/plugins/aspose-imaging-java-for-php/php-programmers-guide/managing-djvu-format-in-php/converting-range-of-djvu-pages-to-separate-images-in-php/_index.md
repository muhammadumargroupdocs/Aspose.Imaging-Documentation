---
title: Converting Range of DjVu Pages to Separate Images in PHP
type: docs
weight: 40
url: /java/converting-range-of-djvu-pages-to-separate-images-in-php/
---

## **Aspose.Imaging - Converting Range of DjVu Pages to Separate Images**
To Convert Range of DjVu Pages to Separate Images using **Aspose.Imaging Java for PHP**, simply invoke **ConvertingRangeOfDjVuPagesToSeparateImages** module. Here you can see example code.

**PHP Code**

{{< highlight php >}}

 # Load an existing image (of type bmp) in an instance of Image class

$image=new Image();

$image = $image->load($dataDir."demo.djvu");

\# Create an instance of BmpOptions

$export_options = new BmpOptions();

\# Set BitsPerPixel for resultant images

$export_options->setBitsPerPixel(32);

\# Create an instance of IntRange and initialize it with range of pages to be exported

$range = [0, 1]; #Export first 2 pages

$i = 0;

while ($i < 2) {

\# Save each page in separate file, as BMP do not support layering

$export_options->setMultiPageOptions(new DjvuMultiPageOptions($i));

$image->save($dataDir."djvupages#{i}.bmp", $export_options);

$i+= 1;

}

\# Display Status.

print "Converted range of DjVu pages to separate images successfully!".PHP_EOL;

{{< /highlight >}}
## **Download Running Code**
Download **Converting Range of DjVu Pages to Separate Images (Aspose.Imaging)** from any of the below mentioned social coding sites:

- [GitHub](https://github.com/asposeimaging/Aspose.Imaging-for-Java/blob/master/Plugins/Aspose_Imaging_Java_for_PHP/src/aspose/imaging/ManagingDjVuFormat/ConvertingRangeOfDjVuPagesToSeparateImages.php)
- [CodePlex](https://asposeimagingjavaphp.codeplex.com/SourceControl/latest#src/aspose/imaging/ManagingDjVuFormat/ConvertingRangeOfDjVuPagesToSeparateImages.php)
