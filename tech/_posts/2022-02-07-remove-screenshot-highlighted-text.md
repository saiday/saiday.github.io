---
layout: post
title:  "利用 HSV 色域消除電子書截圖的重點標註"
date:   2022-02-07 01:23:15 +0800 
category: tech
---

![執行成果](/tech/assets/remove-screenshot-highlighted-text/text_process.png)

當要做 OCR 時，如果原始圖片的文字有被加工，可能導致辨識的準確度下降。
將輸入的圖片的加工清除，是必要的步驟。

我試著要處理的資料是電子書的截圖中的筆記標註。
通常電子書軟體提供的重點標註都是像實體的螢光筆記號一樣，其特色是帶透明度的顏色覆蓋 (overlay)。

研究的過程發現了非常聰明的方式，只要將圖片的色域切換到 [HSV](https://en.wikipedia.org/wiki/HSL_and_HSV) ，並且只取 V channel 的值後再輸出一張即可得到去除透明度覆蓋的圖檔了。

因為重點標註僅會出現在 hue 及 saturation channel。如果只輸出 value channel，那我們就會得到去除重點標註的黑白圖片，如圖所示。

ref: [Removing Text highlighter using Colorspace OpenCV-Python](https://theailearner.com/tag/text-highlighter-image-processing/)
