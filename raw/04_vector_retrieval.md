# 原始資料 04：向量資料庫與語意檢索流程（Vector Search）

- **資料來源**：IBM Documentation — *Retrieval-Augmented Generation (RAG)*
- **參考網址**：https://www.ibm.com/docs/en/quarkus/3.33.x?topic=data-rag-overview-how-rag-works-in-quarkus

## 原始重點摘錄
完整的 RAG 系統分為「離線資料匯入（Ingestion）」與「線上檢索生成（Retrieval & Generation）」兩大階段：
1. **向量資料庫（Vector Store / Database）**：專門用來儲存文件切塊後的向量與對應原文，並支援高效的相似度搜尋。
2. **語意搜尋（Semantic Search）vs. 傳統關鍵字搜尋**：
   - 傳統關鍵字搜尋只比對字面是否完全符合，換個說法（如「筆電無法開機」vs.「電腦沒反應」）就可能漏找。
   - 語意搜尋會將使用者的提問同樣轉成向量，計算與資料庫中各段落的餘弦相似度（Cosine Similarity），找出語意最接近的前 K 筆段落（Top-K）。
3. **提示詞增強與生成（Augmentation & Generation）**：系統將「使用者問題」與「Top-K 檢索段落」組合成完整的 Prompt 傳給 LLM，由模型依據這些上下文整理出最終回答。
