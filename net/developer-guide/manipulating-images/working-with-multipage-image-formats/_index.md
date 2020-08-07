---
title: Working with multipage image formats
type: docs
weight: 90
url: /net/working-with-multipage-image-formats/
---

Aspose.Imaging supports rich functionality to work with multipage image formats such as Gif, Tiff, Psd, Dicom, Cdr, WebP etc. Also, using Aspose.Imaging image can be exported also to multipage PDF document.

To indicate whether the image contains layers/pages/ frames the *IMultipageImage interface* has been introduced. All multi-page images such as PSD, CDR, GIF, etc. are descendants of this interface. Using Pages property, you can access the pages of any multi-page image in the library.
*Example of usage IMultipageImage interface:*

{{< highlight java >}}

 using (Image image = Image.Load(fileName)) 

{ 

    if (image is IMultipageImage) 

    { 

        var pages = ((IMultipageImage)image).Pages; 

    } 

} 

{{< /highlight >}}



**Export of multipage images** can be performed using MultiPageOptions class. With this option you can specify the pages that you want to export to another format. In the case of export to a single-page format, the 1st page of the range will be exported; in the case of export to a multi-page format, all pages of the range will be exported.
*Example of export from multi-page format to single-page image format:*

{{< highlight java >}}

 int startPage = 3;

int countPage = 1;

using (Image image = Image.Load(fileName))

{

    PngOptions pngOptions = new PngOptions();

    pngOptions.MultiPageOptions = new MultiPageOptions(new IntRange(startPage, countPage));

    image.Save(outFileName, pngOptions);

}

{{< /highlight >}}

*Example of export from multi-page format to multi-page*

{{< highlight java >}}

 int startPage = 3;

int countPage = 2;

using (Image image = Image.Load(fileName))

{

    TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.TiffDeflateRgb);

    tiffOptions.MultiPageOptions = new MultiPageOptions(new IntRange(startPage, countPage));

    image.Save(outFileName, tiffOptions);

}

{{< /highlight >}}

Here the 4th and 5th pages will be exported to the tiff format

Below presented *example of export from/to different multipage image formats*:

{{< highlight java >}}

 private void ExportImage(ImageOptionsBase imageOptions, string ext)

{

     string baseFolder = "D:\\images";

     string inputFolderName = baseFolder;

     string outputFolderName = Path.Combine(baseFolder, "out");

     string[] files = Directory.GetFiles(inputFolderName, "*.*");

     foreach (string inputFileName in files)

     {

         Console.WriteLine(Path.GetFileName(inputFileName));

         using (Image image = Image.Load(inputFileName))

         {                   

              //export only 2 pages

              if (image is IMultipageImage && ((IMultipageImage)image).Pages != null && ((IMultipageImage)image).PageCount > 2)

              {

                  imageOptions.MultiPageOptions = new MultiPageOptions(new IntRange(0, 2));

              }

              else

              {

                  imageOptions.MultiPageOptions = null;

              }

              if (image is VectorImage)

              {

                  imageOptions.VectorRasterizationOptions = (VectorRasterizationOptions)image.GetDefaultOptions(new object[] { Color.White, image.Width, image.Height });

                  imageOptions.VectorRasterizationOptions.TextRenderingHint = TextRenderingHint.SingleBitPerPixel;

                  imageOptions.VectorRasterizationOptions.SmoothingMode = SmoothingMode.None;

              }

              string outFileName = Path.Combine(outputFolderName, Path.GetFileName(inputFileName) + ext);

              image.Save(outFileName, imageOptions);

         }

     }

}

 // Code for using ExportImage method

 ImageOptionsBase[] imageOptions = new ImageOptionsBase[] {new PsdOptions(),  new WebPOptions(), new GifOptions(),

                new TiffOptions(TiffExpectedFormat.Default), new BmpOptions(), new JpegOptions(), new Jpeg2000Options(), new PngOptions(),

                new EmfOptions(), new SvgOptions(), new WmfOptions(), new PdfOptions(),

            };

 string[] imageExt = new string[] {".psd", ".webp", ".gif", ".tiff", ".bmp", ".jpeg", ".j2k", ".png", ".emf", ".svg", ".wmf",".pdf"};

 if (imageOptions.Length != imageExt.Length)

 {

      throw new Exception("imageOptions length not equal imageExt length");

 }

 for (int i = 0; i < imageOptions.Length; i++)

 {

      this.ExportImage(imageOptions[i], imageExt[i]);

 }

{{< /highlight >}}
