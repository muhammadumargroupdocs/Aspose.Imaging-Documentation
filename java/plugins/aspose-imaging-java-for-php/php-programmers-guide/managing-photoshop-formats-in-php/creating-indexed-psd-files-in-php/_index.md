---
title: Creating Indexed PSD Files in PHP
type: docs
weight: 10
url: /java/creating-indexed-psd-files-in-php/
---

## **Aspose.Imaging - Creating Indexed PSD Files**
To Create Indexed PSD Files using **Aspose.Imaging Java for PHP**, simply invoke **CreadPSD** module. Here you can see example code.

**PHP Code**

{{< highlight php >}}

 # Create an instance of PsdOptions and set it's properties

$create_options = new PsdOptions();

\# Set source

$create_options->setSource(new FileCreateSource($dataDir . "CreatePSD.psd", false));

\# Set ColorMode to Indexed

$colorModes=new ColorModes();

$create_options->setColorMode($colorModes->Indexed);

\# Set PSD file version

$create_options->setVersion(5);

$color = new Color();

\# Create a new color patelle having RGB colors

$palette = [$color->getRed(), $color->getGreen(), $color->getBlue()];

\# Set Palette property to newly created palette

$create_options->setPalette(new PsdColorPalette($palette));

\# Set compression method

$compressionMethod=new CompressionMethod();

$create_options->setCompressionMethod($compressionMethod->RLE);

\# Create a new PSD with PsdOptions created previously

$psdImage=new PsdImage();

$psd = $psdImage->create($create_options, 500, 500);

\# Draw some graphics over the newly created PSD

$graphics = new Graphics($psd);

$graphics->clear($color->getWhite());

$graphics->drawEllipse(new Pen($color->getRed(), 6), new Rectangle(0, 0, 400, 400));

$psd->save();

\# Display Status.

print "Created PSD successfully!".PHP_EOL;

{{< /highlight >}}
## **Download Running Code**
Download **Creating Indexed PSD Files (Aspose.Imaging)** from any of the below mentioned social coding sites:

- [GitHub](https://github.com/asposeimaging/Aspose.Imaging-for-Java/blob/master/Plugins/Aspose_Imaging_Java_for_PHP/src/aspose/imaging/ManagingPhotoshopFormats/CreadPSD.php)
- [CodePlex](https://asposeimagingjavaphp.codeplex.com/SourceControl/latest#src/aspose/imaging/ManagingPhotoshopFormats/CreadPSD.php)
