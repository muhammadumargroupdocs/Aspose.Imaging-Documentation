---
title: Color Space Conversion for JPEG through ICC Profiles
type: docs
weight: 70
url: /net/color-space-conversion-for-jpeg-through-icc-profiles/
---

## **Color Management for JPEG Format**
This article discusses the usage of ICC profiles to perform the color space management while handling JPEG format with Aspose.Imaging APIs. JPEG’s inner color space is YCbCr however this format can also accommodate Grayscale, RGB, CMYK and YCCK color spaces to store the image’s metadata. Aspose.Imaging APIs mainly operate in RGB space therefore the API has to perform to and from color space conversion in order to properly handle JPEG files. Greyscale to RGB & YCbCr to RGB conversions can be done with mathematical transformations but CMYK & YCCK spaces cannot be easily converted to RGB space.

The Aspose.Imaging APIs has to perform direct RGB to CMYK color transformation for JPEG images having CMYK color space. On the other hand, the images having YCCK color space requires RGB to CMYK to YCCK color transformation, where CMYK to YCCK transformation uses the ITU-R BT.601 conversion applied for the first three channels, leaving the k-channel untouched. In short, Aspose.Imaging APIs have to perform interconversion of RGB and CMYK color spaces for both CMYK & YCCK images, and such transformations are performed with the help of ICC profiles that are basically look-up tables describing the properties of a color and helping in the color transformations.
## **ICC Profiles**
ICC conversion mechanism uses "Profiles" which maps the source color space to device-independent CIELAB or CIEXYZ color spaces. Aspose.Imaging can convert data into color space as required while using these two color spaces with additional profiles. Therefore, for ICC conversion the user needs to supply two profiles – one RGB profile to get to the inner CIE color space and one CMYK profile to get the CMYK color characteristics. In order to achieve the CMYK to RGB conversion, one need to swap profiles, that is; use CMYK profile as source profile and RGB profile as destination profile.
## **Color Conversion for JPEG through ICC Profiles**
Aspose.Imaging APIs conceal the ugly details, providing an easy to use mechanism to specify ICC profiles via JpegOptions class. Moreover, Aspose.Imaging uses the sample profiles of SWOP CMYK and sRGB embedded into it's core therefore in most common usage cases, the user does not need to seek for any specific profiles. There is a drawback of such corrections, that is; such color space conversions are irreversible because we cannot expect to get same color after RGB to CMYK to RGB conversion because of incompatible color spaces and different color profiles. The following code snippet demonstrates the usage of Aspose.Imaging for .NET API to specify RGB and CMYK color profiles for YCCK JPEG image loading process.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-ColorConversionUsingICCProfiles-ColorConversionUsingICCProfiles.cs" >}}

If no profiles are set then Aspose.Imaging for .NET API will use the default profiles instead.

{{< gist "aspose-imaging" "b93073a27bcdd4fefc2821e113f0cb3a" "Examples-CSharp-ModifyingAndConvertingImages-ColorConversionUsingDefaultProfiles-ColorConversionUsingDefaultProfiles.cs" >}}
