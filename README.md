## 我的數位筆記本 (My Digital Notes)

這是一個以「極簡主義（Minimalism）」為設計核心的個人靜態筆記網站，用來記錄日常技術整理、學習心得與讀書摘要。

### 核心特色：透過 `AGENTS.md` 進行規格驅動開發
與傳統一次性的網頁生成不同，本專案在根目錄建立了 **`AGENTS.md` 專案開發規範書**，將網站的視覺風格、檔案命名規則、HTML 結構與更新流程標準化：
- **極簡閱讀體驗**：採用柔和米白背景（`#FAFAFA`）搭配深炭灰文字，並將閱讀寬度限制在 `720px` 以內，減少視覺干擾。
- **純靜態架構**：僅使用原生 HTML 與共用的 `style.css`，無需複雜建置工具，可直接透過 GitHub Pages 託管。
- **高擴充性與一致性**：日後只要將零散的筆記草稿交給 AI，AI 就能依據 `AGENTS.md` 自動生成風格完全一致的獨立筆記頁面，並同步更新首頁的時間倒序列表。

### 專案結構
```text
digital-notes/
├── AGENTS.md           # AI 協作與開發規範書
├── README.md           # 專案說明文件
├── index.html          # 網站首頁（筆記列表與分類索引）
├── style.css           # 全站共用的極簡風格樣式表
└── notes/              # 存放所有獨立筆記文章
    ├── template.html                       # 筆記頁面標準模板
    ├── 2026-11-16-hello-notes.html         # 範例筆記
    └── 2022-02-24-java-installation.html   # Java 安裝紀錄
```
## 日後新增筆記的 Prompt
我要為我的網站新增一篇筆記。請你嚴格依照下面提供的 `AGENTS.md` 規範來產出程式碼。

1. 專案規範 (AGENTS.md)：
https://github.com/ShengMuu/digital-notes/blob/main/AGENTS.md

2. 目前的首頁 (index.html)：
https://github.com/ShengMuu/digital-notes/blob/main/index.html

3. 我要新增的筆記資料：
- 日期：YYYY-MM-DD（例如：2026-11-20）
- 分類：[輸入分類標籤，例如：讀書筆記 / 技術整理 / 遊戲心得]
- 筆記內容：
[在此貼上你的筆記草稿、重點或 HackMD 純文字內容]

請輸出兩樣東西給我：
1. 新筆記的完整 HTML 程式碼（並告訴我這支檔案應該命名為什麼，以及要放在哪個資料夾）。
2. 更新後的完整 `index.html` 程式碼（請確保新文章依時間倒序放在正確位置）。

## DEMO 方式
1. 使用 GitHub Pages 線上網站 : https://shengmuu.github.io/digital-notes/
2. 下載整個壓縮檔並解壓

如果不用上述方法， `index.html` 會讀不到 `style.css` 與 `note/` 下的所有日記檔案
