---
title: "Figma小貼士：複製 SVG"
date: 2022-07-09T11:00:00+08:00
draft: false
tags: ["Figma小貼士"]
author: "Me"
showToc: true
TocOpen: false
draft: false
hidemeta: false
comments: false
description: "直接 copy & paste SVG 作為 React Component..."
canonicalURL: "https://littlecodeguy.com/post/2022-07-09-figma-svg-tips.md"
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
    image: "/images/figma-svg.jpg" # image path/url
    alt: "Code screenshot" # alt text
    caption: "" # display caption under cover
    relative: false # when using page bundles set this to true
    hidden: false # only hide on current single page
editPost:
    URL: "https://github.com/littlecodeguy/littlecodeguy.com/blob/main/content"
    Text: "Suggest Changes" # edit text
    appendFilePath: true # to append file path to Edit link
---

今日想介紹一個 Figma 小貼士，除咗 export 圖片，我哋都可以 copy as SVG 之後直接貼到 editor 作為 .svg file 或放入 React component，但前提 designer 要用 vector 而唔係 raster 圖。

```typescript
export const Logo: FC<SVGProps<SVGSVGElement>> = props => (
  // 貼上 SVG
  <svg
    xmlns="http://www.w3.org/2000/svg"
    viewBox="0 0 484.88 461.23"
    preserveAspectRatio="none" // proportionally scale
    {...props} // spread props
  >
    <path d="M255.53,446.23c-102.85-1.19-193..." />
    <path d="M161.57,461.23c-6.15-1.96-12.62..." />
  </svg>
);
```