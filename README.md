# Flashcard Learning Tool

這個項目是一個簡單的 flashcard 應用程序，允許用戶創建、管理和學習 flashcards。它旨在幫助用戶有效地學習和記憶信息。

1.程式功能

- 創建和管理帶有問題和答案的 flashcards。
- 顯示 flashcards 進行學習。
- 驗證用戶答案。
- 添加和刪除 flashcards。
- 藉由回答正確率提供學習圖表。(以作答正確率為縱軸，測驗次數為橫軸作圖)

2.使用方式
- 安裝requirements.txt內的模組
- 開啟main.pyy並執行。接著點選add flashcards ，可增加題目與答案(兩個都要填)
- 點選show flashcards 可打開題目庫 (edit 可以編輯題目 delete可以刪除題目)。
- 點選start quiz 可以測試自己
- 點選show efficiency plot 可以畫出習圖表

3.程式架構
```
flashcard-project
├── src
│   ├── __init__.py
│   ├── main.py
│   ├── flashcards
│   │   ├── __init__.py
│   │   ├── flashcard.py
│   │   └── flashcard_manager.py
│   └── utils
│       ├── __init__.py
│       └── helper.py
├── tests
│   ├── __init__.py
│   ├── test_flashcard.py
│   └── test_flashcard_manager.py
├── requirements.txt
└── README.md
```

4.開發過程

在開發這個 flashcard 應用程序的過程中，我按照了以下步驟：

   (1) **需求分析**：
      - 確定應用程序的基本功能，如創建、管理和測試 flashcards。
      - 確定需要的外部庫，如 `tkinter` 用於 GUI，`json` 用於數據存儲，      `matplotlib` 用於繪製學習成效圖表。

   (2) **項目結構設計**：
      - 設計項目目錄結構，將不同功能模塊分開管理。
      - 創建 `src` 目錄來存放主要的應用程序代碼，`tests` 目錄來存放測試代碼。

   (3) **核心功能開發**：
      - 開發 `flashcard.py` 來表示單個 flashcard，包含問題和答案，以及檢查答案的方法。
      - 開發 `flashcard_manager.py` 來管理 flashcards 的集合，包含添加、刪除、保存和加載 flashcards 的方法。

   (4) **用戶界面開發**：   
      - 使用 `tkinter` 開發 GUI，提供用戶創建、查看和測試 flashcards 的界面。
      - 添加按鈕和輸入框來實現用戶交互功能。

   (5) **數據存儲和加載**：
      - 使用 `json` 庫將 flashcards 保存到文件中，並在應用程序啟動時加載。
      - 確保數據的持久性，允許用戶在多次運行應用程序之間保留 flashcards。

   (6) **測試和調試**：
      - 使用 `unittest` 編寫測試用例，確保 `Flashcard` 和 `FlashcardManager` 類的功能正確。
      - 測試 GUI 的各種功能，確保用戶交互順暢無誤。

   (7) **學習成效圖表**：
      - 使用 `matplotlib` 繪製用戶的學習成效圖表，顯示每次測驗的正確率。
      - 提供視覺化反饋，幫助用戶了解自己的學習進度。

   (8) **文檔和說明**：
      - 編寫 `README.md` 文件，提供應用程序的使用說明和開發過程。
      - 確保用戶能夠輕鬆上手並理解應用程序的功能。
      
5.參考資料 References

   Tkinter Documentation
   Matplotlib Documentation
   JSON Documentation
   使用 ChatGPT 協助撰寫部分文檔內容，像是提供專案的框架以及自己撰寫程式的優化

6.程式修改或增強的內容
    在開發過程中，我們對以下部分進行了修改和增強：

   (1)設計並實現了 Flashcard 和 FlashcardManager 類，確保核心功能的正確性和穩定性。
   (2)開發了完整的 GUI 界面，提供用戶友好的交互體驗。
   (3)編寫了詳細的測試用例，確保代碼質量。
   (4)撰寫了完整的文檔，幫助用戶理解和使用應用程序。




