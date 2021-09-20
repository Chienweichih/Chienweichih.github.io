---
layout: post
title: "網站小小的大改版!"
description: "使用 Kiko Plus"
date: 2017-07-29 20:29:50 +0800
tags: [jekyll]
comments: true
share: true
---

久違的更新，距離上一篇文章已經快一年了。

上班兩個月以後就沒時間寫文章了，本來想說要寫一點NAND FLASH的東西。不過過了一年，現在對NAND FLASH的認識好像跟一開始上班的時候一樣，沒什麼進步。工作都是聚焦在FTL上，這一年寫了滿多的Code，主要是 MarkBad、Abnomal power fail的處理、控制流量(IW、UW)，之後再來整理一篇FTL的文章吧。(該不會是一年之後吧)

待了一年，部門RD來來去去好多人，主管也換人了，可是應該還撐得下去吧...應該吧

放上之前吃飯的照片來當作這一年的紀錄吧

![NP-Solution-II]({{ site.baseurl }}/images/2017-07-27-upgrade-site-to-1.0.1/NP-Solution-II.jpg){: .center-image}

---

再來才是這篇文章的主題! 我的簡單小網站終於小小的更新了，他變得比較沒有那麼陽春了，我這次使用[Kiko Plus][Kiko-plus]這個Jekyll的Template，讓我的網站變得好看一點又簡潔。

以下是 [Kiko Plus][Kiko-plus] 和 Markdown 的一些用法，就記錄在這裡吧:

---

### 可以把文章設成 Sample Link
在 YAML front matter (Markdown 最前面 `---` 的範圍裡面) 加上

``` yaml
link: 'http://url-you-want-linked'
```

就可以了

這樣可以做到像[湾区日报 APP][wanqu]的風格

---

### Markdown 的一些語法
以下貼了一些範例，有興趣的話可以到 Github 上看 Markdown 的 source code

## 1. Header 

# Header 1

## Header 2

### Header 3

#### Header 4

##### Header 5

###### Header 6

### 1-1. Header Alignment 

##### Left(Default)

##### Center
{: .center}

##### Right
{: .right}

## 2. Body Text

Lorem ipsum dolor sit amet, [test link](#) adipiscing elit. **This is strong.** Nullam dignissim convallis est. Quisque aliquam. *This is emphasized.* Donec faucibus. Nunc iaculis suscipit dui. 5<sup>3</sup> = 125. Water is H<sub>2</sub>O. Nam sit amet sem. Aliquam libero nisi, imperdiet at, tincidunt nec, gravida vehicula, nisl. <u>Underline</u>. Maecenas ornare tortor. Donec sed tellus eget `COPY filename` sapien fringilla nonummy. Mauris a ante. Suspendisse quam sem, consequat at, <del>Dinner’s at 5:00.</del> commodo vitae, feugiat in, nunc. Morbi imperdiet augue <mark>mark element</mark> quis tellus.

## 3. Images

![Large example image](http://placehold.it/800x400 "Large example image")
![Medium example image](http://placehold.it/400x200 "Medium example image")
![Small example image](http://placehold.it/200x200 "Small example image")

### 3-1. Image Alignment
![Center example image](http://placehold.it/200x200 "Center"){: .center-image}

## 4. Blockquotes

> Lorem ipsum dolor sit amet, test link adipiscing elit. Nullam dignissim convallis est. Quisque aliquam.

## 5. List Types

### Unordered List

* Lorem ipsum dolor sit amet, consectetur adipiscing elit.
* Nam ultrices nunc in nisi pellentesque ultricies. Cras scelerisque ipsum in ante laoreet viverra. Pellentesque eget quam et augue molestie tincidunt ac ut ex. Sed quis velit vulputate, rutrum nisl sit amet, molestie neque. Vivamus sed augue at turpis suscipit fringilla.
* Integer pretium nisl vitae justo aliquam, at varius nisi blandit.
  1. Nunc vehicula nulla ac odio gravida vestibulum sed nec mauris.
  2. Duis at diam eget arcu dapibus consequat.
* Etiam vel elit in purus iaculis pretium.

### Ordered List

1. Quisque ullamcorper leo non ex pretium, in fermentum libero imperdiet.
2. Donec eu nulla euismod, rhoncus ipsum nec, faucibus elit.
3. Nam blandit purus gravida, accumsan sem in, lacinia orci.
  * Duis congue dui nec nisi posuere, at luctus velit semper.
  * Suspendisse in lorem id lacus elementum pretium nec vel nibh.
4. Aliquam eget ipsum laoreet, maximus risus vitae, iaculis leo.

### Definition Lists

kramdown
: A Markdown-superset converter

Maruku
: Another Markdown-superset converter

## 6. Tables

| Header1 | Header2 | Header3 |
|:--------|:-------:|--------:|
| cell1   | cell2   | cell3   |
| cell4   | cell5   | cell6   |
|----
| cell1   | cell2   | cell3   |
| cell4   | cell5   | cell6   |
|=====
| Foot1   | Foot2   | Foot3

---

### Syntax Highlighting
修改 `/_sass/_highlighter.scss` 可以調整程式碼的顯示風格

```css
#container {
    float: left;
    margin: 0 -240px 0 0;
    width: 100%;
}
```

```html
{% raw %}<nav class="pagination" role="navigation">
    {% if page.previous %}
        <a href="{{ site.url }}{{ page.previous.url }}" class="btn" title="{{ page.previous.title }}">Previous article</a>
    {% endif %}
    {% if page.next %}
        <a href="{{ site.url }}{{ page.next.url }}" class="btn" title="{{ page.next.title }}">Next article</a>
    {% endif %}
</nav><!-- /.pagination -->{% endraw %}
```

```ruby
module Jekyll
  class TagIndex < Page
    def initialize(site, base, dir, tag)
      @site = site
      @base = base
      @dir = dir
      @name = 'index.html'
      self.process(@name)
      self.read_yaml(File.join(base, '_layouts'), 'tag_index.html')
      self.data['tag'] = tag
      tag_title_prefix = site.config['tag_title_prefix'] || 'Tagged: '
      tag_title_suffix = site.config['tag_title_suffix'] || '&#8211;'
      self.data['title'] = "#{tag_title_prefix}#{tag}"
      self.data['description'] = "An archive of posts tagged #{tag}."
    end
  end
end
```


### Standard Code Block

    {% raw %}<nav class="pagination" role="navigation">
        {% if page.previous %}
            <a href="{{ site.url }}{{ page.previous.url }}" class="btn" title="{{ page.previous.title }}">Previous article</a>
        {% endif %}
        {% if page.next %}
            <a href="{{ site.url }}{{ page.next.url }}" class="btn" title="{{ page.next.title }}">Next article</a>
        {% endif %}
    </nav><!-- /.pagination -->{% endraw %}

### GitHub Gist Embed

An example of a Gist embed below.

這可以放 Gist 在這

<script src="https://gist.github.com/Chienweichih/3a3982b318dc2fe3ea766edde18fb793.js"></script>

---

就這樣! 希望我下次可以寫多一點技術的文章，把FTL的東西整理一下寫上來吧...

[Kiko-plus]: https://aweekj.github.io/Kiko-plus/
[wanqu]: https://wanqu.co/
