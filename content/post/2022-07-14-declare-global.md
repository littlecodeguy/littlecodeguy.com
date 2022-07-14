---
title: "Typescript小貼士：Declare globals"
date: 2022-07-14T07:00:00+08:00
draft: false
tags: ["Typescript小貼士"]
author: "Me"
showToc: true
TocOpen: false
draft: false
hidemeta: false
comments: false
description: "declare globals 可以喺 window object 自定義 type"
canonicalURL: "https://littlecodeguy.com/post/2022-07-14-declare-global"
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
    image: "/images/declare-global.ts.jpg" # image path/url
    alt: "Code screenshot" # alt text
    caption: "" # display caption under cover
    relative: false # when using page bundles set this to true
    hidden: false # only hide on current single page
editPost:
    URL: "https://github.com/littlecodeguy/littlecodeguy.com/blob/main/content"
    Text: "Suggest Changes" # edit text
    appendFilePath: true # to append file path to Edit link
---

唔好咩都 `as any` 啦，用得 Typescript 就係為咗 type safe 同更 declarative，如果要加一個 object 比 window 我哋可以用 declare global 去 extends Window interface，咁咪唔使咩都 any 囉。