---
title: Applying Median and Wiener Filters
type: docs
weight: 20
url: /java/applying-median-and-wiener-filters/
---

## **Applying Median and Wiener Filters**
The median filter is a nonlinear digital filtering technique, often used to remove noise. Such noise reduction is a typical pre-processing step to improve the results of later processing.

The Wiener filter is the MSE(mean squared error) optimal stationary linearfilter for images degraded by additive noise and blurring.

Using Aspose.Imaging for Java API developers can apply median filter to denoise the image and can apply gauss wiener filter on images. This article demonstrates how median filter and gauss wiener filter can be applied to images.
### **Applying Median Filter**
Aspose.Imaging provides MedianFilterOptions class to apply filter on a RasterImage. The code snippet provided below demonstrates how to apply median filter to a raster image.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-ConvertingImages-ApplyMedianFilter-ApplyMedianFilter.java" >}}


### **Applying Gauss Wiener Filter**
Aspose.Imaging provides GaussWienerFilterOptions class to apply filter on a RasterImage. The code snippet provided below demonstrates how to apply gauss wiener filter to a raster image.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-ConvertingImages-ApplyingGaussWienerFilter-ApplyingGaussWienerFilter.java" >}}


### **Applying Gauss Wiener Filter For Colored image**
{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-ConvertingImages-ApplyingGaussWienerFilterForColoredimage-ApplyingGaussWienerFilterForColoredimage.java" >}}


### **Applying Motion Wiener Filter**
Aspose.Imaging provides MotionWienerFilterOptions class to apply filter on a RasterImage. The code snippet provided below demonstrates how to apply motion wiener filter to a raster image.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-ConvertingImages-ApplyMotionWienerFilter-ApplyMotionWienerFilter.java" >}}


## **Apply Correction Filter On An Image**
This article demonstrates the usage of Aspose.Imaging for Java to perform correction filters on an image. Aspose.Imaging API have exposed efficient & easy to use methods to achieve this goal.

Aspose.Imaging for Java has exposed the **BilateralSmoothingFilterOptions** and **SharpenFilterOptions** classes for filtration. **BilateralSmoothingFilterOptions** class needs an integer as size.

The steps to perform Resize are as simple as below:

1. Load an image using the factory method Load exposed by Image class.
1. Convert the image into [RasterImage](http://www.aspose.com/api/java/imaging/com.aspose.imaging/classes/Image).
1. Create an instances of **BilateralSmoothingFilterOptions** and **SharpenFilterOptions** classes.
1. Call the RasterImage.Filter method while specifying rectangle as image bounds and **BilateralSmoothingFilterOptions** class instance.
1. Call the RasterImage.Filter method while specifying rectangle as image bounds and **SharpenFilterOptions** class instance.
1. Adjust the contrast
1. Set brightness
1. Save the results.

The following code example demonstrates how to apply correction filter.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-ConvertingImages-ApplyCorrectionFilterOnImage-ApplyCorrectionFilterOnImage.java" >}}
## **Use Bradley threshold algorithm**
Image thresholding is used in graphics applications. The goal of thresholding an image is to classify pixels as either “dark” or “light”. Aspose.Imaging API allows you to use Bradley thresholding while converting images. The following code snippet shows you how to define the threshold value and then invoke the Bradley’s threshold algorithm.

{{< gist "aspose-imaging" "8c9bd83e0d07145ba0c1" "Examples-src-main-java-com-aspose-imaging-examples-export-UseBradleythresholding-UseBradleythresholding.java" >}}
