# 實驗班網頁 JSON 編輯器

這是一個圖形化的 JSON 編輯工具，專為實驗班網站所設計。透過直覺的使用者介面，管理者可以輕鬆編輯網站內容的 JSON 結構，包含新增、修改、刪除項目，圖片與檔案上傳，並自動套用翻譯顯示。

## 🧩 功能特色

- 支援多層目錄的結構編輯
- 每層以下拉選單選擇，中文翻譯自動對應
- JSON 結構中若為 list，會顯示成項目清單供編輯
- 支援圖片與檔案上傳、刪除
- 表單化管理項目的標題、內文、日期、標籤
- 拖曳調整項目順序
- 所有資料皆儲存在原始資料夾，不另存副本
- 支援翻譯快取 translation_cache.json，避免重複翻譯

## 📁 專案結構

```
├── try.py                      # 主程式，圖形化 JSON 編輯器
├── set.bat                     # 一鍵設定程式執行環境
├── export_output/              # 其他資料
    └── data.json               # 網站主資料（需自行準備）
    └── translation_cache.json  # 翻譯快取（自動產生）
    └── files/                  # 圖片與檔案會儲存在此資料夾中
```

## 🚀 使用方式

1. 安裝必要套件：
    ```bash
    pip install pillow deep-translator
    ```

2. 執行主程式：
    ```bash
    python try.py
    ```

3. 選擇包含 `data.json` 的資料夾即可開始使用。

> 💡 請確認資料夾內有正確格式的 `data.json`，結構需為巢狀 dict + list 組合。

## 💬 翻譯系統說明

- 程式會將每一層 key 對應的完整路徑送至 Google 翻譯。
- 翻譯結果會儲存到 `translation_cache.json`。
- 每個下拉選單項目會顯示為：`英文key (中文翻譯)`。

## 👨‍💻 作者

- 鄭宸翔
- 萬芳高中數位學習實驗班

## 🛡️ 版權宣告

```
© 2025 萬芳高級中學數位學習實驗班．鄭宸翔 保留所有變更權利
```
