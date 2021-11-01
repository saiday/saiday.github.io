---
layout: post
title:  "Bilinear filtering on image downscaling?"
date:   2021-11-01 17:16:26 +0800
categories: ""
---

Android 的 Bitmap 有個 helper method 專門產生 scaled bitmap
```
public static Bitmap createScaledBitmap(@NonNull Bitmap src, int dstWidth, int dstHeight, boolean filter) { ... }
```

`filter` 的 argument 就是 Bilinear filtering (雙線性插值)
文件上的說明是這樣：
> filter – Whether or not bilinear filtering should be used when scaling the bitmap. If this is true then bilinear filtering will be used when scaling which has better image quality at the cost of worse performance. If this is false then nearest-neighbor scaling is used instead which will have worse image quality but is faster. Recommended default is to set filter to 'true' as the cost of bilinear filtering is typically minimal and the improved image quality is significant.

文件的說明上直接提供了建議，除非有效能考量否則 enable Bilinear filtering；但其實如果是 downscaling 的 case，不要 enable Bilinear filtering 應該是更好的選擇。

<br>

#### Billinear 不適合做 downscaling

> Bilinear is a poor choice for downscaling because it leads to aliasing artifacts. This is when you attempt to create spatial frequencies that are beyond the Nyquist sampling limit, and high frequency detail turns into low frequency artifacts. 
> You can minimize this by blurring the image before you downscale it.
> Or you can choose an interpolation algorithm that incorporates some low pass filtering.

如果需要低通濾波器的話，[Lanczos resampling](https://en.wikipedia.org/wiki/Lanczos_resampling) 似乎是合理的選項？

ref:  
[How bilinear interpolation works when down scaling?](https://stackoverflow.com/a/64841829/1554531)
