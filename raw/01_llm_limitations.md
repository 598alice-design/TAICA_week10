# 原始資料 01：大型語言模型（LLM）的限制與外部知識需求

- **資料來源**：AWS — *What is RAG? - Retrieval-Augmented Generation AI Explained*
- **參考網址**：https://aws.amazon.com/what-is/retrieval-augmented-generation/

## 原始重點摘錄
大型語言模型（LLM）在海量公開資料上進行訓練，能夠流暢回答一般性問題，但在實際導入企業或個人應用時，面臨以下結構性限制：
1. **知識過期（Outdated Information）**：LLM 的知識停留在訓練資料的截止時間，無法得知訓練之後發生的最新事件、政策或產品規格。
2. **缺乏領域與私有資料（Lack of Domain-Specific Data）**：模型未曾接觸過組織內部的機密文件、個人筆記或特定領域的專有資料庫。
3. **幻覺問題（Hallucination）**：當系統被問及未知資訊時，模型不會拒絕回答，而是傾向生成看似合理、語氣自信但事實錯誤的虛假內容。
4. **來源不可信或不可追溯**：一般 LLM 難以提供明確的引用出處，導致使用者無法驗證回答的真實性。

因此，實務上需要一種機制，讓模型在生成回答前先讀取權威且最新的外部知識庫，而非僅依賴參數內的靜態記憶。
