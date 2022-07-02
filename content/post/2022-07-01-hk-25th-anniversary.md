---
title: "香港回歸廿五年有冇變？"
date: 2022-07-01T11:03:47+08:00
draft: false
aliases: ["/hk-25th-anniversary"]
tags: ["Naming Convention", "Typescript", "ShowMeTheCode"]
author: "Me"
showToc: true
TocOpen: false
draft: false
hidemeta: false
comments: false
description: "今日係香港大日子，見周圍都好多國旗，紅噹啷咁好喜慶，有感而發想出個 PR 加個新 method 比 HongKong 個 class，順手講下我平時嘅 naming convention， 麻煩大家 review:"
canonicalURL: "https://littlecodeguy.com/post/hk-25th-anniversary"
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
    image: "/images/hk-25th-anniversary.ts.png" # image path/url
    alt: "Code screenshot" # alt text
    caption: "" # display caption under cover
    relative: false # when using page bundles set this to true
    hidden: false # only hide on current single page
editPost:
    URL: "https://github.com/littlecodeguy/littlecodeguy.com/blob/main/content"
    Text: "Suggest Changes" # edit text
    appendFilePath: true # to append file path to Edit link
---

```typescript
import HongKong from 'asia/HongKong';

// constants 用全大階同 underscores
const DATE_OF_HANDOVER = new Date(1997, 6, 1); // 1997-07-01T00:00:00.000Z
const YEARS_NO_CHANGE = 50; // 說好的50年
const now = new Date(); // 2022-07-01T00:00:00.000Z

// return boolean 可以用 prefix
function isHongKongNoChange(date: Date): Boolean {
  const diffInYear = now.getFullYear() - DATE_OF_HANDOVER.getFullYear();
  const withInNoChangePeriod = diffInYear < YEARS_NO_CHANGE;
  // HongKong class 有 static method 類似 Date 可以 instantize 喺指定時間
  const oldHongKong = HongKong.from(DATE_OF_HANDOVER);
  const nowHongKong = HongKong.now();
  
  if (!withInNoChangePeriod) {
    return false; // 過咗就算啦...
  }
  
  // 用量化嘅 core values 做比對
  return nowHongKong.getCoreValues() < oldHongKong.getCoreValues()
}

console.log(isHongKongNoChange(now)); // true
// 變咗啲咩呢？要睇下 HongKong.prototype.getCoreValues() 點 implement 先知
```