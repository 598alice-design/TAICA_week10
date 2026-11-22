# RAG 入門知識庫（LLM Wiki Index）

本知識庫採用「先討論規格、後生成內容」的方式建立，共收錄 5 篇實際權威技術文件與學術論文摘要（`/raw`），並整理為 5 篇標準化概念頁（`/wiki`），作為教學 HTML 簡報（`index.html`）的唯一知識來源。

## 概念導覽（依教學順序）
1. [[wiki/llm-limitations.md|LLM 的三大限制]] — 為什麼 AI 會過時、看不懂私人文件且愛瞎掰？
2. [[wiki/rag-overview.md|RAG 核心概念]] — 什麼是「開書考」架構？它和微調（Fine-tuning）差在哪？
3. [[wiki/chunking-and-embedding.md|切塊與向量化]] — 如何把長文件變成 AI 找得到的語意座標？
4. [[wiki/vector-search.md|向量資料庫與語意搜尋]] — 系統怎麼用「意思」找資料並組裝給 AI？
5. [[wiki/rag-limitations.md|RAG 的常見地雷]] — 為什麼開書考還是有可能寫錯？

## 外部權威資料來源（Sources）
| 對應原始檔案 | 權威來源 | 網址 |
| :--- | :--- | :--- |
| `raw/01_llm_limitations.md` | **AWS**：What is RAG? - Retrieval-Augmented Generation AI Explained | https://aws.amazon.com/what-is/retrieval-augmented-generation/ |
| `raw/02_what_is_rag.md` | **Patrick Lewis et al. (NeurIPS 2020)**：Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks | https://arxiv.org/abs/2005.11401 |
| `raw/03_chunking_embedding.md` | **Pinecone**：Chunking Strategies for LLM Applications | https://www.pinecone.io/learn/chunking-strategies/ |
| `raw/04_vector_retrieval.md` | **IBM Documentation**：Retrieval-Augmented Generation (RAG) | https://www.ibm.com/docs/en/quarkus/3.33.x?topic=data-rag-overview-how-rag-works-in-quarkus |
| `raw/05_rag_challenges.md` | **Scott Barnett et al. (2024)**：Seven Failure Points When Engineering a Retrieval Augmented Generation System | https://arxiv.org/abs/2401.05856 |

## 知識庫約束規則
- 所有簡報內容必須嚴格對應上述 5 篇 Wiki 頁面，禁止引入未定義的進階術語。
- 每頁簡報皆須標註來源檔案（`Source: wiki/xxx.md`）。
