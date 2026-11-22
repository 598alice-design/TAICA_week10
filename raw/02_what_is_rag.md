# 原始資料 02：RAG 架構定義與與微調（Fine-tuning）的比較

- **資料來源**：Patrick Lewis et al. (Meta AI / NeurIPS 2020) — *Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks*
- **參考網址**：https://arxiv.org/abs/2005.11401

## 原始重點摘錄
RAG（Retrieval-Augmented Generation，檢索增強生成）由 Patrick Lewis 等人於 2020 年提出，核心概念是將「參數化記憶（預訓練語言模型）」與「非參數化記憶（外部文件索引庫）」結合：
1. **運作原理**：面對知識密集型問題時，系統先透過檢索器（Retriever）從外部知識庫撈出相關段落，再將問題與檢索結果一併輸入生成器（Generator）產出最終答案。
2. **「開書考」優勢**：相較於純參數模型（閉書考），RAG 能生成更具體、多樣且符合事實的回答，並顯著降低幻覺率。
3. **與微調（Fine-tuning）的關鍵差異**：
   - **微調**：需要重新訓練模型權重，算力與時間成本高，且當外部事實更新時必須重新微調；適合調整模型語氣或特定任務格式。
   - **RAG**：無需更動模型參數，只需直接更新外部文件庫即可讓 AI 獲得最新知識，成本低且具備高度可解釋性（可標註來源）。
