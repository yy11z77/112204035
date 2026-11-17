# 03. 三大核心能力 (Core Capabilities)

- **白話一句話（TL;DR）**：一個 MCP Server 可以提供給 AI 三種不同層級的幫助：「給資料看（Resources）」、「幫你做事（Tools）」、「教你怎麼問（Prompts）」。
- **生活化比喻（Analogy）**：**實習生的工作包**。Resources 是「公司參考手冊」（只能讀）、Tools 是「影印機與發信權限」（能執行動作）、Prompts 是「標準作業 SOP 範本」（引導工作流程）。
- **核心技術重點（Key Facts）**：
  - **Resources（資源 — 唯讀資料）**：由應用程式或使用者控制，類似檔案系統的 URI（如 `file:///logs/error.log`），提供上下文背景知識給 AI 閱讀，不會改變外部狀態。
  - **Tools（工具 — 執行動作）**：由 AI 模型自主決定何時呼叫的函式（Functions），可以執行計算、寫入資料庫或呼叫外部 API（具備副作用，通常需使用者核准）。
  - **Prompts（提示詞模板 — 互動引導）**：由使用者主動觸發（例如斜線指令 `/review-code`），預先設計好的結構化提示詞，幫助使用者快速執行特定任務。
- **資料來源（Source）**：Doc 3 (*MCP Concepts: Resources, Prompts, and Tools*, `modelcontextprotocol.io`)
