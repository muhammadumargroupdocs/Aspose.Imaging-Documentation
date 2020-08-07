---
title: Cropping Metafiles in PHP
type: docs
weight: 20
url: /java/cropping-metafiles-in-php/
---

## **Aspose.Imaging - Cropping Metafiles**
To Crop Metafiles using **Aspose.Imaging Java for PHP**, simply invoke **CropMetafile** module. Here you can see example code.

**PHP Code**

{{< highlight php >}}

 # Load an existing image in an instance of Image class

$image=new Image();

$image = $image->load($dataDir . "sample1.emf");

\# Create an instance of Rectangle class with desired size

$rectangle = new Rectangle(10, 10, 100, 100);

\# Perform the crop operation on object of Rectangle class

$image->crop($rectangle);

\# Save the result in PNG format

$image->save($dataDir . "CropMetafile.png");

\# Display Status.

print "Saved crop emf image to PNG successfully!".PHP_EOL;

{{< /highlight >}}
## **Download Running Code**
Download **Cropping Metafiles (Aspose.Imaging)** from any of the below mentioned social coding sites:

- [GitHub](https://github.com/asposeimaging/Aspose.Imaging-for-Java/blob/master/Plugins/Aspose_Imaging_Java_for_PHP/src/aspose/imaging/ConvertingMetafilestoOtherImageFormats/CropMetafile.php)
- [CodePlex](https://asposeimagingjavaphp.codeplex.com/SourceControl/latest#src/aspose/imaging/ConvertingMetafilestoOtherImageFormats/CropMetafile.php)
