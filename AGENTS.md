## 專案目標

- 使用 HTML 建立數據儀表板模板。
- 可將前端結構整理成單一 HTML 版本，以放入 n8n HTML 節點中使用。

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

- `index.html`：儀表板主要頁面，負責 HTML 結構與內容區塊。
- `css/style.css`：儀表板視覺呈現，負責版面、顏色、字體等設定。
- `js/main.js`：儀表板互動，負責讀取資料、寫入數據、製作圖表。
- `data/`：儀表板的資料來源，為 JSON 格式。


## 注意事項

- 專案根目錄可包含多個儀表板資料夾。
- 儀表板資料夾須以 `<儀表板名稱>_html` 規則命名。
- 每個儀表板資料夾視為獨立網站根目錄，需包含自己的 HTML、CSS、JavaScript 與資料來源。
- 優先使用 Tailwind CSS 設計版面，以 CDN 引入。
- 優先使用 Chart.js 繪製圖表，以 CDN 引入。
- 以 JavaScript 讀取 JSON 資料，並將數據寫入儀表板呈現的對應位置。


## 程式輸出規則

- 除了特別提示程式要使用在 n8n HTML 節點，其餘狀況皆以前端結構的情境考量回應。


## n8n HTML 節點相容性

- 若要在 n8n 使用儀表板，需將前端結構整理成單一 HTML 版本，以放入 n8n HTML 節點中使用。
- 單一 HTML 版本不得使用外部相對路徑，例如 `./js/main.js`、`./css/style.css`。
- 資料會以 JSON 格式由 n8n 上游節點傳入，注意：
    - 不要使用 `fetch('./data/xxx.json')` 讀取本地 JSON。
    - 不要把資料寫在 HTML 的 `<script>` 中。


