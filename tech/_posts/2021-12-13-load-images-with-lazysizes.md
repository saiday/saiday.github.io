---
layout: post
title:  "用 lazysizes 延遲載入 Jekyll 站上的圖片，加速頁面載入速度"
date:   2021-12-13 02:17:37 +0800 
category: tech
---

TL;DR

[Lazy Loading your images in Jekyll blog](https://ranvir.xyz/blog/lazy-loading-your-images-in-jekyll-blog-improving-page-speed/)

### 為什麼需要 lazysizes

弄了這個 site 最主要的目的是想要分享一些[自己拍照的紀錄]({{ site.url }}/photography)，感謝簡易的 GitHub pages 跟易用的 Jekyll，一下就設定好了。

但後續發現在手機上瀏覽時包含圖片的頁面載入得非常慢。這是因為 static page 的關係，在頁面的初始載入時就被圖片載入給拖慢了速度。

利用 [lazysizes](https://github.com/aFarkas/lazysizes) 來達成圖片的延遲載入，讓頁面的初始載入僅需負責 DOM 的部分就好。


#### 設定方法

下載 [lazysizes.min.js](https://afarkas.github.io/lazysizes/lazysizes.min.js) 並放置於 project 內 （我放在 `/javascripts/lazysizes.min.js`）。

在 `_layouts/default.html` 中載入 `lazysizes.min.js`：

```html
{% raw %}
    <!DOCTYPE html>
    <script src="/javascripts/lazysizes.min.js" async=""></script>
    <html lang="{{ page.lang | default: site.lang | default: "en" }}">
    ...
{% endraw %}
```

新建 `_includes/lazyload.html`：

```html
{% raw %}
    {% if include.image_src %}
      <!-- If javascript is not on. -->
      <noscript><img src="{{include.image_src}}" /></noscript>

      <!-- If javascript is present. -->
      <img data-src="{{include.image_src}}" class="blur-up lazyload" />
    {% endif %}
{% endraw %}
```

在 `post` 中使用 `lazysizes`：

```markdown
{% raw %}
    {% include lazyload.html image_src="/photography/assets/DgiyaqBburaw/DgiyaqBburaw_1.jpg" %}
{% endraw %}
```
