---
title: "Javascript中伏記：sorting default behavior"
date: 2022-07-05T07:00:00+08:00
draft: false
tags: ["Javascript中伏記"]
author: "Me"
showToc: true
TocOpen: false
draft: false
hidemeta: false
comments: false
description: "Javascript 嘅 Sorting behavior 好有趣，唔比 args 會當 int 係 string 咁 sort，一不小心好易舐嘢。"
canonicalURL: "https://littlecodeguy.com/post/2022-07-05-js-sorting-behavior"
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
    image: "/images/sorting-behavior.js.png" # image path/url
    alt: "Code screenshot" # alt text
    caption: "" # display caption under cover
    relative: false # when using page bundles set this to true
    hidden: false # only hide on current single page
editPost:
    URL: "https://github.com/littlecodeguy/littlecodeguy.com/blob/main/content"
    Text: "Suggest Changes" # edit text
    appendFilePath: true # to append file path to Edit link
---

```javascript
const nums = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12];

nums.sort();
// [1, 10, 11, 12, 2, 3, 4, 5, 6, 7, 8, 9] 🤯

nums.sort((a, b) => a - b);
// [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12] 😌
```