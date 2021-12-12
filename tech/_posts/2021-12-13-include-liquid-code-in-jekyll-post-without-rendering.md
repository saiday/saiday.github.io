---
layout: post
title:  "在 Jekyll post 中貼 Liquid code 避免被 render 的方法"
date:   2021-12-13 02:58:19 +0800 
category: tech
---

當想要紀錄 Jekyll 的設定在 Jekyll post 時，若包含了 Liquid 的語法，那將會無可避免地被 render 出來。

那麼就需要在 Liquid 的語法出現之前先用 Liquid 提供的 {% raw %} `{% raw %}` {% endraw %} tag 包起來。

就像是：

```
{% assign openTag = '{%' %}
{% raw %}
    {% raw %}
        {% if include.image_src %}
          <!-- If javascript is not on. -->
          <noscript><img src="{{include.image_src}}" /></noscript>

          <!-- If javascript is present. -->
          <img data-src="{{include.image_src}}" class="blur-up lazyload" />
        {% endif %}
    {% endraw %}{{ openTag }} endraw %}{% raw %}
{% endraw %}
```
