---
title: "用 CSS 轉換 SVG 顏色"
date: 2022-07-13T07:00:00+08:00
draft: false
tags: ["CSS", "SVG"]
author: "Me"
showToc: true
TocOpen: false
draft: false
hidemeta: false
comments: false
description: "用 CSS value: currentColor 去改變 SVG fill property..."
canonicalURL: "https://littlecodeguy.com/post/2022-07-13-css-svg-fill-color"
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
    image: "/images/css-svg-fill-color.jpg" # image path/url
    alt: "Code screenshot" # alt text
    caption: "" # display caption under cover
    relative: false # when using page bundles set this to true
    hidden: false # only hide on current single page
editPost:
    URL: "https://github.com/littlecodeguy/littlecodeguy.com/blob/main/content"
    Text: "Suggest Changes" # edit text
    appendFilePath: true # to append file path to Edit link
---

而家做網頁時好多時都需要做 light/dark mode，除咗轉 text 顏色 仲要轉埋 icon 顏色，唔想下下改 <img /> src，可以用 CSS value: `currentColor` 去改變 SVG fill property，只要喺 parent dom 比個 `color: red`, svg fill color 就會跟個值改變，仲可以配合 transition / animation 玩。

<iframe height="300" style="width: 100%;" scrolling="no" title="CSS SVG fill color" src="https://codepen.io/littlecodeguy/embed/PoRGVXZ?default-tab=result" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/littlecodeguy/pen/PoRGVXZ">
  CSS SVG fill color</a> by littlecodeguy (<a href="https://codepen.io/littlecodeguy">@littlecodeguy</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>