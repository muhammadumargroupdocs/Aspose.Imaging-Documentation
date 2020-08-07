---
title: Drawing Vector Images
type: docs
weight: 100
url: /java/drawing-vector-images/
---





{{% alert color="primary" %}} 

Drawing a vector image is not supported at now. It needs to convert the drawn vector image to a raster before drawing.

{{% /alert %}} 
## **Draw Vector Image**
Using Aspose.Imaging for Java you can draw vector image on another vector image. With a few simple steps, you will be able to draw a vector image on another vector image.

- Create ByteArrayOutputStream object
- Load a SVG image
- Rasterize SVG to PNG and write the result to a stream
- Load a PNG image from stream for further drawing
- Draw PNG image on existing SVG image
- Save the results



{{< gist "aspose-com-gists" "07be292db0a393dc95f153f84b28c069" "Examples-src-main-java-com-aspose-imaging-examples-images-DrawVectorImageToRasterImage-DrawVectorImageToRasterImage.java" >}}
