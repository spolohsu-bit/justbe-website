# JustBe Landing Page

這是 JustBe 應用程式的宣傳網頁。

## 檔案結構

```
website/
├── index.html      # 主要網頁
├── images/         # 圖片目錄
│   ├── screenshot-1.png   # 首頁儀表板截圖
│   ├── screenshot-2.png   # 專注模式截圖
│   ├── screenshot-3.png   # 預設選擇截圖
│   └── screenshot-4.png   # 分類瀏覽截圖
└── README.md       # 本說明檔案
```

## 添加截圖

### 建議的截圖內容

1. **screenshot-1.png** - 首頁儀表板
   - 顯示四大類別卡片
   - 展示整體 UI 設計風格

2. **screenshot-2.png** - 專注模式 (Focus Mode)
   - 顯示呼吸動畫或專注畫面
   - 展示音樂控制按鈕

3. **screenshot-3.png** - 預設選擇
   - 顯示不同的 Preset 選項
   - 如 Daily Core Presence、PERMA 等

4. **screenshot-4.png** - 分類瀏覽
   - 顯示某個類別的項目列表
   - 展示項目選擇功能

### 截圖規格

- **尺寸**: iPhone 截圖原始尺寸 (建議 1170 x 2532 px for iPhone 14)
- **格式**: PNG 或 WebP
- **命名**: screenshot-1.png, screenshot-2.png, etc.

### 如何截圖

#### 使用模擬器截圖
```bash
# 在 Xcode 模擬器中按 Cmd + S 儲存截圖
# 或使用 simctl 命令：
xcrun simctl io booted screenshot screenshot.png
```

#### 使用真機截圖
1. 同時按下「側邊按鈕」+「音量增加」
2. 截圖會儲存到照片 App
3. AirDrop 傳到電腦後放入 images/ 目錄

### 更新網頁使用截圖

截圖放入 `images/` 目錄後，修改 `index.html` 中的截圖區塊：

```html
<!-- 將 placeholder 替換為實際圖片 -->
<div class="screenshot">
    <img src="images/screenshot-1.png" alt="首頁儀表板">
</div>
```

## 部署網頁

### GitHub Pages

1. 建立 GitHub repository（如 `justbe-app`）
2. 上傳 website/ 目錄的內容
3. Settings > Pages > Source 選擇 main branch
4. 網址：`https://yourusername.github.io/justbe-app`

### Netlify

1. 拖放 website/ 目錄到 Netlify
2. 自動獲得 `https://xxx.netlify.app` 網址

### Vercel

```bash
cd website
npx vercel
```

## 本地預覽

```bash
cd website
python3 -m http.server 8000
# 然後開啟 http://localhost:8000
```

或使用 VS Code 的 Live Server 擴充功能。

## 網頁特色

- **響應式設計**: 支援桌面、平板、手機
- **漸層動畫**: Hero 區塊有柔和的背景漸層動畫
- **中文字體**: 使用 Noto Sans TC 確保中文顯示優美
- **品牌色彩**: 與 App 一致的溫暖色調

## 內容重點

網頁傳達的核心訊息：

1. **這不是生產力應用** - 不追蹤任務、不測量效率
2. **活在當下** - 專注於此刻的狀態，而非待辦事項
3. **四大支柱** - 智慧、呼吸、情緒、身體
4. **品質 vs 數量** - 關注「你是誰」而非「做了多少」
