## 專案目標

- 使用 HTML 建立數據觀測儀表板。
- 專案根目錄可包含多個儀表板資料夾，儀表板資料夾須以 `<儀表板名稱>_html` 規則命名。
- 每個儀表板資料夾視為獨立網站根目錄，需包含自己的 HTML、CSS、JavaScript 與資料來源。
- 優先使用 Chart.js 繪製前端圖表。
- 前端讀取 JSON 資料，不把資料寫死在 HTML 中。

## 前端結構

```text
<儀表板名稱>_html/
├── index.html
├── css/
│   └── style.css
├── js/
│   └── main.js
└── data/
```

### 目錄與檔案說明

- `index.html`：儀表板主要頁面，負責 HTML 結構與內容區塊。
- `css/style.css`：儀表板樣式，負責版面、顏色、字體等視覺設定。
- `js/main.js`：儀表板互動，負責讀取資料、製作圖表。
- `data/`：儀表板的資料來源，為 JSON 格式。
