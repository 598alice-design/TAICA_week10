# RAG 入門知識庫（LLM Wiki Index）

本知識庫採用「先討論規格、後生成內容」的方式建立，共收錄 5 篇原始資料（`/raw`），並整理為 5 篇標準化概念頁（`/wiki`），作為教學 HTML 簡報（`index.html`）的唯一知識來源。

## 概念導覽（依教學順序）
1. [[wiki/llm-limitations.md|LLM 的三大限制]] — 為什麼 AI 會過時、看不懂私人文件且愛瞎掰？
2. [[wiki/rag-overview.md|RAG 核心概念]] — 什麼是「開書考」架構？它和微調（Fine-tuning）差在哪？
3. [[wiki/chunking-and-embedding.md|切塊與向量化]] — 如何把長文件變成 AI 找得到的語意座標？
4. [[wiki/vector-search.md|向量資料庫與語意搜尋]] — 系統怎麼用「意思」找資料並組裝給 AI？
5. [[wiki/rag-limitations.md|RAG 的常見地雷]] — 為什麼開書考還是有可能寫錯？

## 知識庫約束規則
- 所有簡報內容必須嚴格對應上述 5 篇 Wiki 頁面，禁止引入未定義的進階術語。
- 每頁簡報皆須標註來源檔案（`Source: wiki/xxx.md`）。
