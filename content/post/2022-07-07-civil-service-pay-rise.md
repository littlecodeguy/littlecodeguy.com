---
title: "Javascript 入門：Object.keys() vs Object.getOwnPropertyNames()"
date: 2022-07-07T11:08:00+08:00
draft: false
tags: ["Javascript入門"]
author: "Me"
showToc: true
TocOpen: false
draft: false
hidemeta: false
comments: false
description: "一般情況用 Object.keys 就可以滿足到返回自定義 property names，但有時你想得到..."
canonicalURL: "https://littlecodeguy.com/post/2022-07-07-civil-service-pay-rise"
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
    image: "/images/2022-07-07-civil-service-pay-rise.png" # image path/url
    alt: "Code screenshot" # alt text
    caption: "" # display caption under cover
    relative: false # when using page bundles set this to true
    hidden: true # only hide on current single page
editPost:
    URL: "https://github.com/littlecodeguy/littlecodeguy.com/blob/main/content"
    Text: "Suggest Changes" # edit text
    appendFilePath: true # to append file path to Edit link
---

一般情況用 Object.keys 就可以滿足到返回自定義 property names，但有時你想得到所有 inherited 嘅 property 比如 Array.prototype.length, Object.keys 就滿足唔到，又或者 object 本身有 define 咗 non-enumerable property。

```typescript
const 公務員加薪 = { 加幅: 0.025 };

Object.keys(公務員加薪); // ['加幅']
Object.getOwnPropertyNames(公務員加薪); // ['加幅']

// Array
const 公務員團體 = ['失望', '驚訝', '要求追回通脹'];

Object.keys(公務員團體); // ['0', '1', '2']
Object.getOwnPropertyNames(公務員團體); // ['0', '1', '2', 'length']

// Non-enumerable property
Object.defineProperties(公務員加薪, {
    林志偉: {
        enumerable: false,
        value: '要見特首',
    },
});

Object.keys(公務員加薪); // ['加幅']
Object.getOwnPropertyNames(公務員加薪); // ['加幅', '林志偉']
```