# 原始資料 03：資料前處理——切塊策略（Chunking）與向量化（Embedding）

- **資料來源**：Pinecone — *Chunking Strategies for LLM Applications*
- **參考網址**：https://www.pinecone.io/learn/chunking-strategies/

## 原始重點摘錄
在將長文件匯入 RAG 系統前，必須先進行切塊與向量化處理，這直接影響後續檢索的精準度：
1. **為什麼需要切塊（Chunking）**：
   - LLM 具有上下文視窗（Context Window）長度限制，無法一次塞入整本數百頁的文件。
   - 將長文切成語意集中的小段落（例如每 300–500 字一塊），能讓向量表達更精準，減少無關雜訊干擾。
2. **重疊區間（Chunk Overlap）**：
   - 在相鄰兩個切塊之間保留一小段重複文字（例如 10%–20%），避免關鍵句子或前後因果剛好在邊界被截斷。
3. **向量化（Embedding）**：
   - 透過 Embedding 模型將每個文字區塊轉換為高維度的數字陣列（向量）。語意越相近的文字，在向量空間中的距離越近，使電腦能夠以數學方式衡量「意思是否相近」。
