---
title: Compressed vector formats
type: docs
weight: 10
url: /net/compressed-vector-formats/
---

# **Overview**
Compressed vector images are vector images of the EMF, WMF, SVG formats compressed using a zip archiver. Their size averages from 30-70% of the original. This saves space on media and reduces file transfer time over the network. But you should pay attention to the fact that not all applications work with compressed vector formats. See below for more details. 
## **SVGZ**
SVGZ files are typically 50 to 80 percent smaller in size than SVG.

For example, take any SVG file and compress it to SVGZ:

![todo:image_alt_text](compressed-vector-formats_1.png)

As you can see the size of the source file is **369** kb

**Convert SVG to SVGZ** using the following code:

{{< gist "aspose-com-gists" "2d1bcb9853315458808ffbcd9e7e3e02" "Examples-Svg-to-Svgz-example.cs" >}}

![todo:image_alt_text](compressed-vector-formats_2.png)

The resulting file size is  ~**59%** of the original.
We can open this file using any of the above applications.

![todo:image_alt_text](compressed-vector-formats_3.png)

Using the following code, it is possible to **convert the SVGZ to SVG:**

{{< gist "aspose-com-gists" "2d1bcb9853315458808ffbcd9e7e3e02" "Examples-Svgz-to-Svg-example.cs" >}}
## **EMZ**
A file with the EMZ file extension is a  actually just GZIP compressed EMF files, which is a graphics format used by Microsoft (**MS Word, MS Visio**)

For example, take any EMF file and compress it to EMZ:

![todo:image_alt_text](compressed-vector-formats_4.png)

As you can see the size of the source file is **116** kb
**Convert EMF to EMZ** using the following code:

{{< gist "aspose-com-gists" "2d1bcb9853315458808ffbcd9e7e3e02" "Examples-Emf-to-Emz-example.cs" >}}

![todo:image_alt_text](compressed-vector-formats_5.png)

The resulting file size is  ~**14%** of the original.

Open result emz file in MS Word

Using the following code, it is possible to **convert the EMZ to EMF**

{{< gist "aspose-com-gists" "2d1bcb9853315458808ffbcd9e7e3e02" "Examples-Emz-to-Emf-example.cs" >}}
## **WMZ**
A file with the WMZ file extension is a  actually just GZIP compressed WMF files, which is a graphics format used by Microsoft (**MS Word, MS Visio**).

For example, take any WMF file and compress it to WMZ:

![todo:image_alt_text](compressed-vector-formats_6.png)

As you can see the size of the source file is **55.2** kb. **Convert WMF to WMZ** using the following code:

{{< gist "aspose-com-gists" "2d1bcb9853315458808ffbcd9e7e3e02" "Examples-Wmf-to-Wmz-example.cs" >}}



![todo:image_alt_text](compressed-vector-formats_7.png)


The resulting file size is  ~**49%** of the original.

Open result emz file in MS Word

![todo:image_alt_text](compressed-vector-formats_8.png)

Using the following code, it is possible to **convert the WMZ to WMF:**

{{< gist "aspose-com-gists" "2d1bcb9853315458808ffbcd9e7e3e02" "Examples-Wmz-to-Wmf-example.cs" >}}

