# 04. 運作流程與安全性 (Communication & Security)

- **白話一句話（TL;DR）**：MCP 底層使用通用的 JSON 格式傳遞訊息，支援本機與遠端連線，並強制要求「人類同意」才能執行危險操作。
- **生活化比喻（Analogy）**：**銀行保險箱的雙鑰匙機制**。AI 雖然知道保險箱裡有什麼，但每次要拿東西（呼叫 Tool）都必須經過你（使用者）按確認鍵同意。
- **核心技術重點（Key Facts）**：
  - **JSON-RPC 2.0 通訊格式**：所有請求（Request）、回應（Response）與通知（Notification）都遵循輕量級的 JSON-RPC 2.0 標準。
  - **兩種傳輸方式（Transports）**：
    - **Stdio（本機連線）**：適合在「同一台電腦」上執行，Host 直接啟動本地的 Server 程式，速度極快且無網路外洩風險。
    - **Streamable HTTP / SSE（雲端連線）**：適合連接「遠端雲端」的 MCP Server，透過 HTTP 進行雙向通訊。
  - **安全性與人機協作（Human-in-the-Loop）**：Host 必須提供明確的 UI 介面，在執行敏感 Tool 之前取得使用者授權（Consent），並限制 Server 只能存取被允許的目錄（Roots）。
- **資料來源（Source）**：Doc 4 (*MCP Specification: Transports & Security*, `spec.modelcontextprotocol.io`)
