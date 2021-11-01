---
layout: post
title:  "Bilinear filtering on downscaling case"
date:   2021-11-01 17:16:26 +0800
categories: TIL, Android
---

Android 的 Bitmap 有個 helper method 
```
public static Bitmap createScaledBitmap(@NonNull Bitmap src, int dstWidth, int dstHeight, boolean filter) { ... }
```

`filter` 的 argument 就是 Bilinear filtering (雙線性插值)
文件上的說明是這樣：
> filter – Whether or not bilinear filtering should be used when scaling the bitmap. If this is true then bilinear filtering will be used when scaling which has better image quality at the cost of worse performance. If this is false then nearest-neighbor scaling is used instead which will have worse image quality but is faster. Recommended default is to set filter to 'true' as the cost of bilinear filtering is typically minimal and the improved image quality is significant.

從文件的說明來看幾乎是除非有效能考量否則推薦 enable Bilinear filtering，但其實如果是 downscaling 的 case，不要 enable Bilinear filtering 應該是更好的選擇。

<br>

#### 但其實 downscaling 的情況不適合 Billinear

> Bilinear is a poor choice for downscaling because it leads to aliasing artifacts. This is when you attempt to create spatial frequencies that are beyond the Nyquist sampling limit, and high frequency detail turns into low frequency artifacts. 
> You can minimize this by blurring the image before you downscale it. Or you can choose an interpolation algorithm that incorporates some low pass filtering.

ref:  
[How bilinear interpolation works when down scaling?](https://stackoverflow.com/a/64841829/1554531)
