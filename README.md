# 𓃥 白六航空訊息傳遞 (White 6 Aero Explorer)

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![Three.js](https://img.shields.io/badge/Three.js-000000?style=flat-square&logo=three.js&logoColor=white)
![WebGL](https://img.shields.io/badge/WebGL-990000?style=flat-square&logo=webgl&logoColor=white)
![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-222222?style=flat-square&logo=github&logoColor=white)

一個基於 WebGL 與 Three.js 開發的 3D 互動飛機拉布條訊息傳遞應用程式。使用者可以自訂飛行布條的中文字樣、色彩與氣流波浪動態，並支援一鍵生成 WebM 高畫質動畫影片下載與 URL 客製化訊息分享。

👉 **[馬上體驗線上 App](https://kuochili-ops.github.io/Airplane-message/)**

---

## 🌟 核心特色 (Key Features)

- **3D 機械雙翼機與動態運鏡**：精緻的 GLB 雙翼機模型，具備平滑高速自轉的木質螺旋槳與自然氣流搖晃效果。
- **即時客製化 Canvas 布條貼圖**：
  - 支援自訂中文訊息、文字顏色與布條背景色。
  - 雙面貼圖邏輯，確保視角旋轉至正面或背面時文字均方向正確且清晰可讀。
  - 布條前端精準銜接於飛機尾端繩架，搭配幾何頂點算術（Vertex Wave Effect），實現自然流暢的風浪飄動效果。
- **動態雲朵背景視差**：3D 程式化白雲群向右飄移，營造飛機持續向前高空飛行的擬真視覺視差。
- **一鍵自動動畫錄影 (WebM Download)**：
  - 提供「🎬 錄影並下載 WebM」功能。
  - 觸發時飛機自動從畫面右側特寫入場，拖曳客製化布條橫越天空，並於布條尾端停留在畫面中央 1 秒後自動結束錄製並下載影片。
- **URL 參數編碼與分享 (Shareable URLs)**：
  - 提供「🔗 複製分享連結」功能，可將目前設定的文字、顏色與氣流參數編碼至網址。
  - 支援網頁初始化讀取 URL 參數，開啟即可完美還原專屬訊息布條。

---

## 🛠️ 技術架構 (Tech Stack)

- **前端渲染 Engine**：[Three.js (v0.160.0)](https://threejs.org/)
- **模型格式**：GLTF / GLB (`sketchfab_5_million_members.glb`)
- **動態貼圖繪製**：HTML5 Canvas 2D API
- **畫面錄製**：HTMLCanvasElement `captureStream()` + `MediaRecorder API`
- **部署平台**：GitHub Pages

---

## 📁 專案結構 (Directory Structure)

```text
Airplane-message/
├── index.html                           # 應用程式主程式碼 (3D 場景、UI 控制與動畫迴圈)
├── sketchfab_5_million_members.glb      # 飛機與繩架 3D 模型檔
└── README.md                            # 專案說明文件
