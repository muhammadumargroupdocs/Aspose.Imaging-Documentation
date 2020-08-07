---
title: Opening Image files in PHP
type: docs
weight: 10
url: /java/opening-image-files-in-php/
---

## **Aspose.Imaging - Opening an Image File from Disk**
To Open an Image File from Disk using **Aspose.Imaging Java for PHP**, you can use following example code.

**PHP Code**

{{< highlight php >}}

 # Create an Image object and load an existing file using the file path

$image=new Image();

$image = $image->load($dataDir + "test.jpg");

\# do some image processing

{{< /highlight >}}
## **Aspose.Imaging - Opening an Image using a Stream**
To Open an Image using a Stream using **Aspose.Imaging Java for PHP**, you can use following example code.

**PHP Code**

{{< highlight php >}}

 # Create a Stream Object

$stream = new Stream($dataDir + "test.jpg")

\# Create an Image object and load an existing file using the Stream object

$image=new Image();

$image = $image->load($stream);

\# do some image processing

{{< /highlight >}}
