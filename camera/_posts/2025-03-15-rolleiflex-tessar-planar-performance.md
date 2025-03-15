---
layout: post
title:  "Rolleiflex 蔡司鏡頭表現差異"
date:    2025-03-15 15:54:53 +0800
category: camera 
tags: [Rolleiflex, Tessar, Planar]
---

我保管過許多不同 Zeiss 版本的 Rolleiflex，在找資料時看到了這篇文章 [articolo Rolleiflex TLR vs Hasselblad: schemi ottici ed MTF originali delle Rollei biottiche antiche e moderne
confrontati con quelli di analoghe focali del sistema Zeiss Hasselblad: chi vince?](http://www.marcocavina.com/articoli_fotografici/Rolleiflex_vs_Hasselblad_2/00_pag.htm)，哎呀，簡直是寶藏啊。  
這篇文章中收錄了幾乎所有 Rolleiflex 蔡司鏡頭的結構、光學設計圖及 MTF 圖表，也有許多第一手資料，非常有收穫。基於個人的學習紀錄及心得我對原始文章感興趣的內容節錄及擴充。


若這篇文章內容讓你覺得有趣，強烈推薦看參考文章，雖然是義大利文寫的，但，感謝這個 AI 翻譯時代吧。  
本篇全部的圖表都引用自參考文章，與作者取得授權中。

### Rolleiflex 上的 Tessar 結構
除了最早期的 Rolleiflex 是用 Triotar 結構外，有大量的 Rolleicord 及 Rolleiflex 型號都是搭配 Tessar 鏡頭 （Rolleiflex: Original, Automat, T; Rolleicord），是 Rolleiflex 上最經典的鏡頭結構。

{% include lazyload.html image_src="/camera/assets/rolleiflex-lens/tessar_75_35.jpeg" %}

Tessar 75/3.5 MTF：  

{% include lazyload.html image_src="/camera/assets/rolleiflex-lens/tessar_75_35_mtf.jpeg" %}

在成像中央對比、解析力良好，但從偏離中心約 25% 的位置開始影像品質即大幅下滑；特別是在畫面邊緣區域，切線方向（tangenziale）的解析力下降更為明顯，這也是典型 Tessar 設計特有的邊緣畫質衰退現象。  
相較於用於更小底片格式的 Tessar 鏡頭，Rolleiflex 用的 75/3.5 Tessar 邊緣下降還算溫和？

### Rolleiflex 上的 Planar 結構
從 1954 年的 2.8C/3.5C 版本開始，Rolleiflex 將鏡頭結構由 Tessar 「升級」成 Planar，而在 Rolleiflex 雙眼相機歷史中，出現過以下幾種 Planar 鏡頭：  
1. 前期 Planar 3.5（5 片 4 組）
2. 後期 Planar 3.5（6 片 4 組）
3. Planar 2.8（5 片 4 組）
4. 復刻限定版 FX, GX 用的 Planar 2.8 made by Rollei（5 片 4 組）

蔡司經典的 Planar 是 6 片 4 組，從上面的列舉可以發現除了 2. 之外，其他都是經典 Planar 結構的變形或者說簡化設計。  

#### 5 片 4 群的 Planar 們
生產年代重疊的前期 Planar 75/3.5 及 Planar 80/2.8 雖然都是 5 片 4 群的 Planar，但鏡頭結構是不一樣的。

前期 Planar 3.5 結構粗略上看像是一個前後顛倒的 Xenotar 設計；Planar 2.8 則像是 Xenotar。但都帶有 Planar 的影像風格。

> 標準的 Xenotar 通常是 5 片 4 組或 6 片 4 組，其中最經典的是 5 片結構版本。  
> Xenotar 在靠近光圈的位置只有單獨一片鏡片，不像 Planar 兩側鏡組都使用雙片膠合鏡。

Planar 75/3.5（5 片 4 組）：  
{% include lazyload.html image_src="/camera/assets/rolleiflex-lens/planar_75_35_5.jpeg" %}
Planar 80/2.8：  
{% include lazyload.html image_src="/camera/assets/rolleiflex-lens/planar_80_28.jpeg" %}

至於 Rollei 自己復刻限量版的 Planar 80/2.8 在光學結構上與蔡司提供的 Planar 80/2.8 是一模一樣的僅加上了 HFT 鍍膜，但在最終的光學表現上卻有影像風格的差異。  
在成像中心的清晰度不如蔡司版本的 80/2.8，但畫面邊緣的表現明顯改善，超過蔡司的版本。原因不明，但原文作者認為可能是環保玻璃的特性或焦點偏移造成。  
鏡頭結構與蔡司版本對比：
{% include lazyload.html image_src="/camera/assets/rolleiflex-lens/planar_28_zeiss_rollei.jpeg" %}

MTF 差異：

| 蔡司 Planar 80/2.8 | Rollei Planar 80/2.8 |
|----------------------|----------------------|
| ![](/camera/assets/rolleiflex-lens/planar_80_28_mtf.jpeg) | ![](/camera/assets/rolleiflex-lens/planar_80_28_rollei_mtf.jpeg) |


#### 6 片版的 Planar 在光學表現上有比較好嗎？

這是 6 片版 Planar 的結構圖：

{% include lazyload.html image_src="/camera/assets/rolleiflex-lens/planar_75_35_6.jpeg" %}

在 Rolleiflex 3.5F 1960 後就開始改成 6 片 4 組 的 Planar 鏡頭。與前期的 75/3.5（5 片）相比，透過下方的重疊 MTF 比較圖，可以看到紅線的 6 片版在中心、邊緣及解析度都有明顯的改善：  
{% include lazyload.html image_src="/camera/assets/rolleiflex-lens/planar_75_35_5_6_mtf.jpeg" %}

而與 Planar 80/2.8 重疊的 MTF 圖表也可看出，這兩顆都非常優異的鏡頭在縮小到最佳光圈後，6 片版的 Planar 3.5 代表的黑線在像散及解析度上更好一些。不過 80/2.8 Planar 在 MTF 表上可以看到即便是光圈全開都有很驚人的成像中心對比：  

{% include lazyload.html image_src="/camera/assets/rolleiflex-lens/planar_75_80_mtf.jpeg" %}

回到疑問的解答，有，Planar 的 6 片版本明顯比同樣 f/3.5 光圈的 Planar 有成像表現上的改善。與 80/2.8 的 Planar 在伯仲之間，邊緣解析度更好一些。  
社群上廣為流傳的 Planar 6 片版本是設計最好的 Rolleiflex 鏡頭是有一定的根據。

#### 那麼，我要怎麼知道我的 Planar 3.5 是 6 片的呢？
辨別 Rolleiflex 的版本簡直是一門技藝了，我自己會透過 [tlr.rolleigraphy.eu](https://tlr.rolleigraphy.eu/sn75.php) 社群整理的表格來確認，表格對應機身序號的的 Taking Lens 若有標注 6 elements 就代表是 6 片版 Planar。


#### 6 片版 Planar 那麼好，為什麼 80/2.8 Planar 從頭到尾都維持 5 片？
誰知道呢？但考慮到 5 片 的 80/2.8 鏡頭已經在體積上大那麼多了，或許空間上真的塞不下了？或許 80/2.8 的成像風格 Rollei 已經非常滿意了？


## 結論

有機會看到詳盡有根據的資料總是讓人興奮，但興奮也往往放大了對結果的期待。  
在一樣的前後期條件下，我相信有意識的攝影愛好者能從成像風格上區分出是 Tessar 或 Planar 拍攝的，但我不認為 5 片及 6 片的 Planar 在觀賞情境下能被區分出來，即便在大圖輸出情境。  
若透過冷冰冰的 MTF 數據說出哪顆鏡頭勝過哪顆鏡頭會天真地讓人同情。
