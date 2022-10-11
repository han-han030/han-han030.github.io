---
title: "直播小工具"
description: 一些直播會用的東西，聊天室、彈幕、插件等等
date: 2022-10-08T21:29:13+08:00
draft: false
# weight: 1
# aliases: ["/AirTag"]
tags: ["obs", "工具"]
author: "Me"
# author: ["Me", "You"] # multiple authors
showToc: false
TocOpen: false
hidemeta: false
comments: true
description: "一些直播會用的東西，聊天室、彈幕、插件等等"
#canonicalURL: "https://canonical.url/to/page"
disableHLJS: true # to disable highlightjs
disableShare: false
disableHLJS: false
hideSummary: false
searchHidden: false
ShowReadingTime: true
ShowBreadCrumbs: true
ShowPostNavLinks: true
#cover:
#    image: "https://i.imgur.com/RKpc8dT.jpg" # image path/url
#    alt: "<alt text>" # alt text
#    caption: "<text>" # display caption under cover
#    relative: true # when using page bundles set this to true
#    hidden: false # only hide on current single page
#editPost:
#    URL: "https://github.com/<path_to_repo>/content"
#    Text: "Suggest Changes" # edit text
#    appendFilePath: false # to append file path to Edit link
---

**大部分的工具都是給OBS用的，不知道Twitch Studio或StreamLabs可不可以用**


## YT聊天室
### 字體+特效
<details>
  <summary>Noto Sans Traditional Chinese 淡入滑進</summary>
  ```css=
  @import url("https://fonts.googleapis.com/css?family=Noto Sans TC");

  /* Background colors*/
  body {
    overflow: hidden;
    background-color: rgba(0,0,0,0);
  }
  /* Transparent background. */
  yt-live-chat-renderer {
    background-color: transparent !important;
  }
  yt-live-chat-text-message-renderer,
  yt-live-chat-text-message-renderer[is-highlighted] {
    background-color: transparent !important;
  }

  yt-live-chat-text-message-renderer[author-type="owner"],
  yt-live-chat-text-message-renderer[author-type="owner"][is-highlighted] {
    background-color: transparent !important;
  }

  yt-live-chat-text-message-renderer[author-type="moderator"],
  yt-live-chat-text-message-renderer[author-type="moderator"][is-highlighted] {
    background-color: transparent !important;
  }

  yt-live-chat-text-message-renderer[author-type="member"],
  yt-live-chat-text-message-renderer[author-type="member"][is-highlighted] {
    background-color: transparent !important;
  }


  yt-live-chat-author-chip #author-name {
    background-color: transparent !important;
  }
  /* Outlines */
  yt-live-chat-renderer * {
    text-shadow: -2px -2px #000000,-2px -1px #000000,-2px 0px #000000,-2px 1px #000000,-2px 2px #000000,-1px -2px #000000,-1px -1px #000000,-1px 0px #000000,-1px 1px #000000,-1px 2px #000000,0px -2px #000000,0px -1px #000000,0px 0px #000000,0px 1px #000000,0px 2px #000000,1px -2px #000000,1px -1px #000000,1px 0px #000000,1px 1px #000000,1px 2px #000000,2px -2px #000000,2px -1px #000000,2px 0px #000000,2px 1px #000000,2px 2px #000000;
    font-family: "Noto Sans TC";
    font-size: 18px !important;
    line-height: 18px !important;
  }

  yt-live-chat-text-message-renderer #content,
  yt-live-chat-legacy-paid-message-renderer #content {
    overflow: initial !important;
  }

  /* Hide scrollbar. */
  yt-live-chat-item-list-renderer #items{
    overflow: hidden !important;
  }

  yt-live-chat-item-list-renderer #item-scroller{
    overflow: hidden !important;
  }

  /* Hide header and input. */
  yt-live-chat-header-renderer,
  yt-live-chat-message-input-renderer {
    display: none !important;
  }

  /* Reduce side padding. */
  yt-live-chat-text-message-renderer,
  yt-live-chat-legacy-paid-message-renderer {
      padding-left: 4px !important;
    padding-right: 4px !important;
  }

  yt-live-chat-paid-message-renderer #header {
      padding-left: 4px !important;
    padding-right: 4px !important;
  }

  /* Avatars. */
  yt-live-chat-text-message-renderer #author-photo,
  yt-live-chat-paid-message-renderer #author-photo,
  yt-live-chat-legacy-paid-message-renderer #author-photo {
    
    width: 24px !important;
    height: 24px !important;
    border-radius: 24px !important;
    margin-right: 6px !important;
  }

  /* Hide badges. */
  yt-live-chat-text-message-renderer #author-badges {
    display: none !important;
    vertical-align: text-top !important;
  }

  /* Timestamps. */
  yt-live-chat-text-message-renderer #timestamp {
    
    color: #999999 !important;
    font-family: "Noto Sans TC";
    font-size: 16px !important;
    line-height: 16px !important;
  }

  /* Badges. */
  yt-live-chat-text-message-renderer #author-name[type="owner"],
  yt-live-chat-text-message-renderer #author-name.owner,
  yt-live-chat-text-message-renderer yt-live-chat-author-badge-renderer[type="owner"] {
    color: #ffd600 !important;
  }

  yt-live-chat-text-message-renderer #author-name[type="moderator"],
  yt-live-chat-text-message-renderer #author-name.moderator,
  yt-live-chat-text-message-renderer yt-live-chat-author-badge-renderer[type="moderator"] {
    color: #5e84f1 !important;
  }

  yt-live-chat-text-message-renderer #author-name[type="member"],
  yt-live-chat-text-message-renderer #author-name.member,
  yt-live-chat-text-message-renderer yt-live-chat-author-badge-renderer[type="member"] {
    color: #0f9d58 !important;
  }

  /* Channel names. */
  yt-live-chat-text-message-renderer #author-name {
    color: #cccccc !important;
    font-family: "Noto Sans TC";
    font-size: 20px !important;
    line-height: 20px !important;
  }

  yt-live-chat-text-message-renderer #author-name::after {
    content: ":";
    margin-left: 2px;
  }

  /* Messages. */
  yt-live-chat-text-message-renderer #message,
  yt-live-chat-text-message-renderer #message * {
    color: #ffffff !important;
    font-family: "Noto Sans TC";
    font-size: 18px !important;
    line-height: 18px !important;
  }


  /* SuperChat/Fan Funding Messages. */
  yt-live-chat-paid-message-renderer #author-name,
  yt-live-chat-paid-message-renderer #author-name *,
  yt-live-chat-legacy-paid-message-renderer #event-text,
  yt-live-chat-legacy-paid-message-renderer #event-text * {
    color: #ffffff !important;
    font-family: "Noto Sans TC";
    font-size: 20px !important;
    line-height: 20px !important;
  }

  yt-live-chat-paid-message-renderer #purchase-amount,
  yt-live-chat-paid-message-renderer #purchase-amount *,
  yt-live-chat-legacy-paid-message-renderer #detail-text,
  yt-live-chat-legacy-paid-message-renderer #detail-text * {
    color: #ffffff !important;
    font-family: "Noto Sans TC";
    font-size: 18px !important;
    line-height: 18px !important;
  }

  yt-live-chat-paid-message-renderer #content,
  yt-live-chat-paid-message-renderer #content * {
    color: #ffffff !important;
    font-family: "Noto Sans TC";
    font-size: 18px !important;
    line-height: 18px !important;
  }

  yt-live-chat-paid-message-renderer {
    margin: 4px 0 !important;
  }

  yt-live-chat-legacy-paid-message-renderer {
    background-color: #0f9d58 !important;
    margin: 4px 0 !important;
  }

  yt-live-chat-text-message-renderer a,
  yt-live-chat-legacy-paid-message-renderer a {
    text-decoration: none !important;
  }

  yt-live-chat-text-message-renderer[is-deleted],
  yt-live-chat-legacy-paid-message-renderer[is-deleted] {
    display: none !important;
  }

  yt-live-chat-ticker-renderer {
    background-color: transparent !important;
    box-shadow: none !important;
  }
  yt-live-chat-ticker-renderer {
    display: none !important;
  }


  yt-live-chat-ticker-paid-message-item-renderer,
  yt-live-chat-ticker-paid-message-item-renderer *,
  yt-live-chat-ticker-sponsor-item-renderer,
  yt-live-chat-ticker-sponsor-item-renderer * {
    color: #ffffff !important;
    font-family: "Noto Sans TC";
  }

  yt-live-chat-mode-change-message-renderer, 
  yt-live-chat-viewer-engagement-message-renderer, 
  yt-live-chat-restricted-participation-renderer {
    display: none !important;
  }

  yt-live-chat-banner-manager {
    display: none !important;
  }
  @keyframes anim {
  0% { opacity: 0; transform: translateX(-16px); }
  100% { opacity: 1; transform: none;}
  }

  yt-live-chat-text-message-renderer,
  yt-live-chat-legacy-paid-message-renderer {
    animation: anim 200ms;
    animation-fill-mode: both;
  }


  yt-live-chat-action-panel-renderer, 
  yt-live-chat-renderer #action-panel {
    display: none !important;
  }

  ```

</details>
})

### 樣式
#### 兩條線+半透明背景
> 來源:[左右二重線の背景半透明.css](https://github.com/yuki-natsuno-vt/YoutubeLiveChatBGCustomCSS/blob/main/sample/%E5%B7%A6%E5%8F%B3%E4%BA%8C%E9%87%8D%E7%B7%9A%E3%81%AE%E8%83%8C%E6%99%AF%E5%8D%8A%E9%80%8F%E6%98%8E.css)
* 預覽
![](https://i.imgur.com/hXmN7fG.png)
* CSS

```css=
yt-live-chat-text-message-renderer,
yt-live-chat-text-message-renderer[author-type="owner"],
yt-live-chat-text-message-renderer[author-type="moderator"],
yt-live-chat-text-message-renderer[author-type="member"] {
  /* 色は rgba(255,255,255,1) か #16進数カラーコード で指定 */

  /* 背景色： RGB は 0～255、A は 0.0～1.0 */
  background-color: rgba(255,255,255,0.3) !important;
  
  /* 全体の横幅： ※可変にしたい場合は auto と書き換える*/
  width: 300px !important;

  /* 塗りつぶし余白： 上側から時計回り */
  padding: 5px 8px 5px 8px !important;

  /* コメント間の余白： */
  margin-bottom: 5px !important;

  /* 枠線： */
  /* 上下左右でコードが分かれているので枠を付けたい方向のコメントアウトを解除する.
   * 全方向に付けたい場合は一番下の border のみを使う.
   * solid(1本線) の代わりに double(2本線)、dashed(破線)、dotted(点線) などが使える.
   */
  border-left: double 10px rgba(215,0,53,1) !important;
  border-right: double 10px rgba(215,0,53,1) !important;
}

/* 名前の後ろで改行したい場合はこの部分も使う*/
yt-live-chat-text-message-renderer #message {
  display: block;
  margin-top: 5px; /*名前とメッセージの間隔*/
}

```

#### spoiler 透明
>來源[左縁付き透明背景](https://github.com/yuki-natsuno-vt/YoutubeLiveChatBGCustomCSS/blob/main/sample/%E5%B7%A6%E7%B8%81%E4%BB%98%E3%81%8D%E9%80%8F%E6%98%8E%E8%83%8C%E6%99%AF.css)
* 預覽
![](https://i.imgur.com/IN44R3Q.png)
* CSS
```css=
/*
  以下のコードを「Chat v2.0 Style Generator」で生成したCSSコードの最下部にコピペしてください.
*/
/* コメント部全体の背景をカスタマイズする */
yt-live-chat-text-message-renderer,
yt-live-chat-text-message-renderer[author-type="owner"],
yt-live-chat-text-message-renderer[author-type="moderator"],
yt-live-chat-text-message-renderer[author-type="member"] {
  /* 色は rgba(255,255,255,1) か #16進数カラーコード で指定 */

  /* 全体の横幅： ※可変にしたい場合は auto と書き換える*/
  width: 300px !important;

  /* 塗りつぶし余白： 上側から時計回り */
  padding: 5px 8px 5px 8px !important;

  /* コメント間の余白： */
  margin-bottom: 5px !important;

  /* 枠線： */
  /* 上下左右でコードが分かれているので枠を付けたい方向のコメントアウトを解除する.
   * 全方向に付けたい場合は一番下の border のみを使う.
   * solid(1本線) の代わりに double(2本線)、dashed(破線)、dotted(点線) などが使える.
   */
  border-left: solid 5px rgba(255,255,255,1) !important;
}

/* 名前の後ろで改行したい場合はこの部分も使う*/
yt-live-chat-text-message-renderer #message {
  display: block;
  margin-top: 5px; /*名前とメッセージの間隔*/
}
```
:::
### 彈幕(本地)
* 預覽
![](https://i.imgur.com/GmSnFqj.gif)
![](https://i.imgur.com/FFNIFIk.png)
* 安裝
1. 點擊[這裡](https://github.com/fiahfy/youtube-live-chat-flow/releases/download/v0.0.51/archive.zip)下載
2. 解壓縮
3. 打開`edge://extensions/`並開啟`開發人員模式`
4. 點擊`載入解壓縮`並選擇解壓縮過的資料夾
## OBS插件
### Move transition
>來源: [OBS論壇](https://obsproject.com/forum/resources/move-transition.913/)
* 安裝
1. [下載](https://obsproject.com/forum/resources/move-transition.913/download)並解壓縮檔案到OBS的資料夾:
`C:\Program Files\obs-studio\`
或
`C:\Program Files (x86)\obs-studio`
2. 安裝最新的[visual c++ redistributable for visual studio 2019](https://aka.ms/vs/16/release/vc_redist.x64.exe)
3. 開啟OBS
4. 從轉場特效新增Move transition
### spectralizer
>來源: [OBS論壇](https://obsproject.com/forum/resources/spectralizer.861/)

#### 安裝
1. 關閉OBS
2. [下載](https://github.com/univrsal/spectralizer/releases/download/v1.3.4/spectralizer.v1.3.4.installer.windows.exe)
3. 開啟exe就會自動安裝
4. 到OBS新增來源的地方就會有了
![](https://i.imgur.com/GWhnwhe.png)
### Stream Timer
![](https://i.imgur.com/2qT0K0L.png)
>來源: [OBS論壇](https://obsproject.com/forum/resources/countdown-timer-stream-timer.713/)

#### 安裝
1. 下載[這個檔案](https://drive.google.com/file/d/1vaSM1igdnIZHMDfvNT6n1p22Z2MwXKAP/view)
2. 開啟OBS及`Stream Timer.exe`
3. 調成你想倒數的時間
4. 在OBS裡新增`文字(GDI+)` 並勾選`"從檔案讀取"`
![](https://i.imgur.com/YIaWPeX.png)
5. 選取檔案裡的`timer.txt`就完成了

