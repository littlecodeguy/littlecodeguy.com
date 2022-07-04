---
title: "css 一行 reset 所有 element properties"
date: 2022-07-04T09:06:16+08:00
draft: false
tags: ["CSS"]
author: "Me"
showToc: true
TocOpen: false
draft: false
hidemeta: false
comments: false
description: "最近發現 css 有個 property 叫「all」，可以用嚟一次過賦值比所有 element’s properties, 非常適合用嚟 reset element。"
canonicalURL: "https://littlecodeguy.com/post/2022-06-04-how-to-reset-css-in-oneline"
disableShare: false
disableHLJS: false
hideSummary: false
searchHidden: true
ShowReadingTime: true
ShowBreadCrumbs: true
ShowPostNavLinks: true
ShowWordCount: true
ShowRssButtonInSectionTermList: true
UseHugoToc: true
cover:
    image: "/images/all-unset.css.png" # image path/url
    alt: "Code screenshot" # alt text
    caption: "" # display caption under cover
    relative: false # when using page bundles set this to true
    hidden: false # only hide on current single page
editPost:
    URL: "https://github.com/littlecodeguy/littlecodeguy.com/blob/main/content"
    Text: "Suggest Changes" # edit text
    appendFilePath: true # to append file path to Edit link
---

最近發現 css 有個 property 叫「all」，可以用嚟一次過賦值比所有 element’s properties, 非常適合用嚟 reset element。

```css
button {
  all: unset;
}
```

<iframe height="300" style="width: 100%;" scrolling="no" title="css all unset" src="https://codepen.io/littlecodeguy/embed/xxWGzQq?default-tab=result" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/littlecodeguy/pen/xxWGzQq">
  css all unset</a> by littlecodeguy (<a href="https://codepen.io/littlecodeguy">@littlecodeguy</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>