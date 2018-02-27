# PWA(Progressive Web App)
> * [Introduction](#introduction)
> * [Used Technics](#technics)
>   - [Web App Manifest](#web-app-manifest)
---
## Introduction
PWA 是一個讓 Web App 可以類似於 Native App 的使用者體驗的技術，它可以透過 *Service Worker* 來在離線仍可以使用，也可以透過 *W3C manifests meta data* 和 *Service Worker* 的登記，讓搜索引擎能夠找到 Web App，還可以像 Native App 一般掛在主螢幕上…，詳細可帶來的效益可以參考[你的首個 Progressive Web App][]。 

[微軟也在 2018/02 宣佈 Windows 10 及 Edge 支援 PWA][Welcoming Progressive Web Apps to Microsoft Edge and Windows 10]，所以 PWA 應該會是未來 Web App 發展的主軸之一。

---
## Technologies
> * [Web App Manifest](#web-app-manifest)
> * [Service Work](#service-work)
> * [Push Notification](#push-notification)

- ### Web App Manifest
> 是一個 JSON 格式的文件，它提供了應用程式相關的資訊（像是名稱、作者、圖示，和描述）。 
> manifest 的功用是將 Web 應用程式安裝到設備的主畫面，為用戶提供更快速的訪問和更豐富的體驗。
> \~~ From [Mozilla: Web App Manifest][]
* [W3C Spec](https://www.w3.org/TR/appmanifest/)
* How to use: [Mozilla: Web App Manifest][]
  1. manifest.json
  ```json
  {
    "name": "HackerWeb",
    "short_name": "HackerWeb",
    "start_url": ".",
    "display": "standalone",
    "background_color": "#fff",
    "description": "A simply readable Hacker News app.",
    "icons": [{
      "src": "images/touch/homescreen48.png",
      "sizes": "48x48",
      "type": "image/png"
    }, {
      "src": "images/touch/homescreen72.png",
      "sizes": "72x72",
      "type": "image/png"
    }, {
      "src": "images/touch/homescreen96.png",
      "sizes": "96x96",
      "type": "image/png"
    }, {
      "src": "images/touch/homescreen144.png",
      "sizes": "144x144",
      "type": "image/png"
    }, {
      "src": "images/touch/homescreen168.png",
      "sizes": "168x168",
      "type": "image/png"
    }, {
      "src": "images/touch/homescreen192.png",
      "sizes": "192x192",
      "type": "image/png"
    }],
    "related_applications": [{
      "platform": "web"
    }, {
      "platform": "play",
      "url": "https://play.google.com/store/apps/details?id=cheeaun.hackerweb"
    }]
  }
  ```
  2. html
  ```html
  <link rel="manifest" href="manifest.json">
  ```

- ### Service Work
- ### Push Notification
---
## References
1. [你的首個 Progressive Web App][]
2. [下一代 Web 应用模型 —— Progressive Web App](https://huangxuan.me/2017/02/09/nextgen-web-pwa/)
3. [Welcoming Progressive Web Apps to Microsoft Edge and Windows 10][]


[你的首個 Progressive Web App]: https://developers.google.com/web/fundamentals/codelabs/your-first-pwapp/?hl=zh-tw
[Welcoming Progressive Web Apps to Microsoft Edge and Windows 10]: https://blogs.windows.com/msedgedev/2018/02/06/welcoming-progressive-web-apps-edge-windows-10/#Zt6AeeVsUMl1mVEf.97
[Mozilla: Web App Manifest]: https://developer.mozilla.org/zh-TW/docs/Web/Manifest
