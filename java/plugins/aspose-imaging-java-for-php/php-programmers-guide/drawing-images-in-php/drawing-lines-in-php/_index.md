---
title: Drawing Lines in PHP
type: docs
weight: 50
url: /java/drawing-lines-in-php/
---

## **Aspose.Imaging - Drawing Lines**
To Draw Lines using **Aspose.Imaging Java for PHP**, simply invoke **DrawingLines** module. Here you can see example code.

**PHP Code**

{{< highlight php >}}

 # Create an instance of BmpOptions and set its various properties

$create_options = new BmpOptions();

$create_options->setBitsPerPixel(32);

\# Define the source property for the instance of BmpOptions

$ary=array();

$create_options->setSource(new StreamSource(new ByteArrayInputStream($ary)));

\# Create an instance of Image

$image=new Image();

$image = $image->create($create_options,100,100);

\# Create an instance of Color

$color = new Color();

\# Create an instance of Pen

$pen = new Pen();

\# Create and initialize an instance of Graphics class

$graphic = new Graphics($image);

\# Clear the image surface with Yellow color

$graphic->clear($color->getYellow());

\# Draw a dotted line by specifying the Pen object having blue color and co-ordinate Points

$graphic->drawLine(new Pen($color->getBlue()), 9, 9, 90, 90);

$graphic->drawLine(new Pen($color->getBlue()), 9, 90, 90, 9);

$solid_brush = new SolidBrush();

$point = new Point();

\# Draw a continuous line by specifying the Pen object having Solid Brush with red color and two point structures

$graphic->drawLine(new Pen(new SolidBrush($color->getRed())), new Point(9, 9), new Point(9, 90));

\# Draw a continuous line by specifying the Pen object having Solid Brush with aqua color and two point structures

$graphic->drawLine(new Pen(new SolidBrush($color->getAqua())), new Point(9, 90), new Point(90, 90));

\# Draw a continuous line by specifying the Pen object having Solid Brush with black color and two point structures

$graphic->drawLine(new Pen(new SolidBrush($color->getBlack())), new Point(90,90), new Point(90,9));

\# Draw a continuous line by specifying the Pen object having Solid Brush with white color and two point structures

$graphic->drawLine(new Pen(new SolidBrush($color->getWhite())), new Point(90,9), new Point(9,9));

\# Save all changes.

$image->save($dataDir."DrawLinesExample.bmp");

print "Lines have been drawn in image successfully!".PHP_EOL;

{{< /highlight >}}
## **Download Running Code**
Download **Drawing Lines (Aspose.Imaging)** from any of the below mentioned social coding sites:

- [GitHub](https://github.com/asposeimaging/Aspose.Imaging-for-Java/blob/master/Plugins/Aspose_Imaging_Java_for_PHP/src/aspose/imaging/DrawingImages/DrawingLines.php)
- [CodePlex](https://asposeimagingjavaphp.codeplex.com/SourceControl/latest#src/aspose/imaging/DrawingImages/DrawingLines.php)
