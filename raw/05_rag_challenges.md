# 原始資料 05：RAG 系統工程實務的常見失敗點與限制

- **資料來源**：Scott Barnett et al. (2024) — *Seven Failure Points When Engineering a Retrieval Augmented Generation System*
- **參考網址**：https://arxiv.org/abs/2401.05856

## 原始重點摘錄
Barnett 等人於 2024 年針對實務 RAG 系統進行研究，指出 RAG 並非萬靈丹，常見的關鍵失敗點包括：
1. **切塊與前處理失衡（Chunking / Format Issues）**：切太碎會導致上下文斷裂（看到數據卻不知對應條件）；切太大或未清理格式雜訊，則會稀釋語意重點並干擾模型。
2. **檢索失敗（Missed Top Ranked Documents）**：俗稱「垃圾進、垃圾出（Garbage In, Garbage Out）」。若正確段落沒有排進 Top-K，無論後端 LLM 多強大，都無法給出正確答案。
3. **內容未正確抽取或仍產生幻覺（Not Extracted / Hallucination）**：即使正確段落已被放進 Prompt，模型仍可能因雜訊過多而漏看重點、誤解內容，或偷渡自身舊記憶。因此實務上常需在系統提示詞明確約束：「若參考資料中沒有答案，請直接回答不知道」。
