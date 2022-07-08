---
title: "CSS 入門：background-clip: text"
date: 2022-07-08T11:00:00+08:00
draft: false
tags: ["CSS入門"]
author: "Me"
showToc: true
TocOpen: false
draft: false
hidemeta: false
comments: false
description: "background-clip: text，可以為文字加上背景圖片。"
canonicalURL: "https://littlecodeguy.com/post/2022-07-08-css-background-text-clip"
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
    image: "/images/background-text-clip.jpg" # image path/url
    alt: "Code screenshot" # alt text
    caption: "" # display caption under cover
    relative: false # when using page bundles set this to true
    hidden: true # only hide on current single page
editPost:
    URL: "https://github.com/littlecodeguy/littlecodeguy.com/blob/main/content"
    Text: "Suggest Changes" # edit text
    appendFilePath: true # to append file path to Edit link
---

今次介紹 background-clip: text，可以為文字加上背景圖片，或者配合 `background: linear-gradient();` 做漸變色文字。

```css
.text-bg-clip {
  background-clip: text;
  -webkit-background-clip: text;
  -webkit-text-fill-color: rgba(0, 0, 0, 0);
}
```

<iframe height="800" style="width: 100%;" scrolling="no" title="CSS Text Portrait" src="https://codepen.io/littlecodeguy/embed/abYNBBM?default-tab=result" frameborder="no" loading="lazy" allowtransparency="true" allowfullscreen="true">
  See the Pen <a href="https://codepen.io/littlecodeguy/pen/abYNBBM">
  CSS Text Portrait</a> by littlecodeguy (<a href="https://codepen.io/littlecodeguy">@littlecodeguy</a>)
  on <a href="https://codepen.io">CodePen</a>.
</iframe>