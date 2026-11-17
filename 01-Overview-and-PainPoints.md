# 01. 核心概念與痛點 (Overview & Pain Points)

- **白話一句話（TL;DR）**：MCP 是一套開放標準，讓各種 AI 模型都能用同一套規則去讀取外部資料與操作工具，不用再為每個工具重寫客製化程式。
- **生活化比喻（Analogy）**：**AI 界的 USB-C 接口**。以前每家手機充電線都不同（Micro-USB、Lightning），現在統一成 USB-C，一條線就能接螢幕、硬碟跟充電器；MCP 就是統一 AI 與外部軟體之間的「通用插頭」。
- **核心技術重點（Key Facts）**：
  - 解決 $M \times N$ 整合難題：過去若有 $M$ 個 AI 應用要連接 $N$ 個資料來源，需要開發 $M \times N$ 個客製化連接器（Connectors）。導入 MCP 後，只需各自實作標準，複雜度降為 $M + N$。
  - 打破資料孤島：讓大型語言模型（LLM）不再受限於訓練時的靜態知識，能安全存取本地檔案、企業資料庫與即時網路服務。
  - 開源開放標準：由 Anthropic 提出並開源，任何開發者都能自由實作支援 MCP 的模型或工具。
- **資料來源（Source）**：Doc 1 (*Introducing the Model Context Protocol*, Anthropic 官方部落格)
