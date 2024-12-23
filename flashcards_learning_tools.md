(1) 程式的功能 Features
   
    1.*Interactive Input*: Input answers using the keyboard.
  
    2.*Real-Time Visualization*: Questions are printed on a flashcard.
  
    3.*Recording Answers*: Records the number of correct and wrong answers.
  
    4.*Learning Efficiency*: Presents learning efficiency based on correctly answered questions.
  
    5.*Constructive Feedback*: Provides constructive feedbacks and suggestions based on performance.
  
    6.*Learning Graphs*: Outputs learning graphs for a single subject 
  
(2) 使用方式 Usage

  0. 前置作業:
      在終端機Terminal 執行 pip install -r requirements.txt
      (可選):
      python -m venv venv 
      source venv/bin/activate  # 在 Windows 上使用 `venv\Scripts\activate`
  1. 啟動伺服器：
      ```bash
      打開python app.py
      打開並執行python flashcard.py
      ```
  2. 訪問應用：
      在瀏覽器中打開 `http://127.0.0.1:5000`。

  3. 添加 Flashcard：
      - 訪問 `http://127.0.0.1:5000/add_flashcard` 來添加新的 Flashcard。

  4. 管理 Flashcards：
      - 訪問 `http://127.0.0.1:5000/manage_flashcards` 來查看、編輯和刪除 Flashcards。

  5. 編輯 Flashcard：
      - 訪問 `http://127.0.0.1:5000/edit_flashcard/<id>` 來編輯特定的 Flashcard，其中 `<id>` 是 Flashcard 的 ID。
      譬如:http://127.0.0.1:5000/edit_flashcard/1 就是編號一的題目


(3) 架構 Architecture

    my_final_project.py/ 
    ├── instance/ 
    │ ├── flashcards.db # SQLite 資料庫文件，存儲所有 Flashcard 的數據。 
    ├── myflashcardproject/ 
    │ ├── app.py # 主應用檔案，包含 Flask 應用的主要邏輯和路由。 
    │ ├── models.py # 定義資料庫模型，描述資料庫表格的結構和關係。 
    │ ├── flashcard.py # 包含 Flashcard 相關的路由和功能。 
    ├── templates/ 
    │ ├── index.html # 主頁面模板。 
    │ ├── flashcard.html # Flashcard 題目頁面模板。 
    │ ├── manage_flashcards.html # 管理 Flashcards 的頁面模板。 
    │ ├── edit_flashcard.html # 編輯 Flashcard 的頁面模板。 
    │ ├── add_flashcard.html # 新增 Flashcard 的頁面模板。 
    │ ├── learning_curve.html # 顯示學習曲線圖表的頁面模板。 
    │ ├── quiz.html # 顯示 Flashcard 問題和答案對錯的頁面模板。 
    ├── static/
    │ ├── learning_curve.png # 存放學習曲線圖表。 
    ├── requirements.txt # required dependencies 
(4) 開發過程 Development Process

1. 設計和規劃：確定應用的基本功能和進階功能。
2. 設置環境：安裝 Flask 和其他必要的庫。
3. 實現基本功能：實現交互式輸入、實時可視化、記錄答案和學習效率展示。
4. 實現進階功能：提供建設性的反饋和建議，輸出學習圖表。
5. 測試和調試：測試應用的各個功能，修復錯誤。
6. 部署：將應用部署到伺服器上。

(5) 參考資料 References
1. [Flask Documentation](https://flask.palletsprojects.com/)
2. [Matplotlib Documentation](https://matplotlib.org/stable/contents.html)
Chatgpt 提供程式架構與內容輔助

(6) 程式修正或增強功能 Enhancements
ChatGpt 提供了實現flashcard的架構
而我參考其中的架構，在這個專案中貢獻以下部分：

1. **設計和實現基本功能**：
    - 設計並實現了 Flashcard 的交互式輸入和實時可視化功能。
    - 記錄用戶的正確和錯誤答案，並展示學習效率。

2. **實現進階功能**：
    - 提供建設性的反饋和建議，根據用戶的表現生成學習圖表。(利用matplotlib利用matplotlib)

3. **資料庫模型設計**：
    - 聽從Chat Gpt的觀點，使用 SQLAlchemy 定義資料庫模型，描述資料庫表格的結構和關係。

4. **前端模板設計**：
    -藉由Chat Gpt 的建議與指教，我設計並實現了多個 HTML 模板，包括 `index.html`、`flashcard.html`、`manage_flashcards.html`、`edit_flashcard.html`、`add_flashcard.html`、`learning_curve.html` 和 `quiz.html`。

5. **測試和調試**：
    - 測試應用的各個功能，修復錯誤，確保應用穩定運行。

感謝 ChatGPT 在程式架構與內容上的輔助，幫助我更好地完成這個專案。
