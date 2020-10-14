---
title: Deskewing a scanned image
type: docs
weight: 30
url: /java/deskewing-a-scanned-image/
---

Skew is an artifact that might appear during document scanning process and it consists of getting the document’s text/images be rotated at a slight angle. It can have various causes but the most common are paper getting misplaced during a scan. Therefore, **deskew** is the process of detecting and fixing this issue on scanned files (ie, bitmap) so deskewed images will have the text/images correctly and horizontally aligned.

Deskewing an image can help a lot, if you want to improve the readability of scanned images. For example, think of a camera that automatically takes photos of goods with a barcode. If the skew angle is too high, the barcode can not be detected. After deskewing, the barcode can be read.

{{< gist "aspose-com-gists" "07be292db0a393dc95f153f84b28c069" "Deskew.java" >}}


Below is an example of skewed scanned text and deskewed output.

| ![todo:image_alt_text](deskewing-a-scanned-image_1.png) | ![todo:image_alt_text](deskewing-a-scanned-image_2.png) |
| ------------------------------------------------------- | ------------------------------------------------------- |
| Skewed image                                            | Deskewed image                                          |