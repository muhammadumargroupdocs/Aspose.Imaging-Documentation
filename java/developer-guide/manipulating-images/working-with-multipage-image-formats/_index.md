---
title: Working with multipage image formats
type: docs
weight: 160
url: /java/working-with-multipage-image-formats/
---

Aspose.Imaging supports rich functionality to work with multipage image formats such as Gif, Tiff, Psd, Dicom, Cdr, WebP etc. Also, using Aspose.Imaging image can be exported also to multipage PDF document.

To indicate whether the image contains layers/pages/ frames the *IMultipageImage interface* has been introduced. All multi-page images such as PSD, CDR, GIF, etc. are descendants of this interface. Using Pages property, you can access the pages of any multi-page image in the library.
*Example of usage IMultipageImage interface:*



{{< highlight java >}}

 try (Image image = Image.load(fileName))

{

    if (image instanceof IMultipageImage)

    {

        Image[] pages = ((IMultipageImage)image).getPages();

    }

}

{{< /highlight >}}



**Export of multipage images** can be performed using MultiPageOptions class. With this option you can specify the pages that you want to export to another format. In the case of export to a single-page format, the 1st page of the range will be exported; in the case of export to a multi-page format, all pages of the range will be exported.

*Example of export from multi-page format to single-page image format:*



{{< highlight java >}}

 int startPage = 3;

int countPage = 1;

try (Image image = Image.load(fileName))

{

    PngOptions pngOptions = new PngOptions();

    pngOptions.setMultiPageOptions(new MultiPageOptions(new IntRange(startPage, countPage)));

    image.save(outFileName, pngOptions);

}

{{< /highlight >}}



*Example of export from multi-page format to multi-page*

{{< highlight java >}}

 int startPage = 3;

int countPage = 2;

try (Image image = Image.load(fileName))

{

    PngOptions pngOptions = new PngOptions();

    pngOptions.setMultiPageOptions(new MultiPageOptions(new IntRange(startPage, countPage)));

    image.save(outFileName, pngOptions);

}

{{< /highlight >}}



Here the 4th and 5th pages will be exported to the tiff format

Below presented *example of export from/to different multipage image formats*:



{{< highlight java >}}

 private void exportImage(ImageOptionsBase imageOptions, String ext)

{

    String baseFolder = "D:\\images\\";

    String inputFolderName = baseFolder;

    String outputFolderName = baseFolder + "out\\";

    String[] files = new File(inputFolderName).list();

    if (files == null)

    {

        System.err.println("No files are found!");

        return;

    }

    for (String inputFileName : files)

    {

        String fileName = new File(inputFolderName + inputFileName).getName();

        System.out.println(fileName);

        try (Image image = Image.load(inputFileName))

        {

            //export only 2 pages

            if (image instanceof IMultipageImage && ((IMultipageImage)image).getPages() != null && ((IMultipageImage)image).getPageCount() > 2)

            {

                imageOptions.setMultiPageOptions(new MultiPageOptions(new IntRange(0, 2)));

            }

          else

            {

                imageOptions.setMultiPageOptions(null);

            }

            if (image instanceof VectorImage)

            {

                VectorRasterizationOptions defaultOptions = (VectorRasterizationOptions) image.getDefaultOptions(new Object[]{Color.getWhite(), image.getWidth(), image.getHeight()});

                imageOptions.setVectorRasterizationOptions(defaultOptions);

                defaultOptions.setTextRenderingHint(TextRenderingHint.SingleBitPerPixel);

                defaultOptions.setSmoothingMode(SmoothingMode.None);

            }

            String outFileName = outputFolderName + fileName + ext;

            image.save(outFileName, imageOptions);

        }

    }

}

// Code for using ExportImage method

ImageOptionsBase[] imageOptions = new ImageOptionsBase[] {new PsdOptions(),  new WebPOptions(), new GifOptions(),

        new TiffOptions(TiffExpectedFormat.Default), new BmpOptions(), new JpegOptions(), new Jpeg2000Options(), new PngOptions(),

        new EmfOptions(), new SvgOptions(), new WmfOptions(), new PdfOptions(),

};

String[] imageExt = new String[] {".psd", ".webp", ".gif", ".tiff", ".bmp", ".jpeg", ".j2k", ".png", ".emf", ".svg", ".wmf",".pdf"};

if (imageOptions.length != imageExt.length)

{

    throw new RuntimeException("imageOptions length not equal imageExt length");

}

for (int i = 0; i < imageOptions.length; i++)

{

    this.exportImage(imageOptions[i], imageExt[i]);

}

{{< /highlight >}}
