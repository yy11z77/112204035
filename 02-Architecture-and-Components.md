# 02. 系統架構與三大角色 (Architecture & Components)

- **白話一句話（TL;DR）**：MCP 採用主從式（Client-Server）架構，由三個角色分工合作，把「AI 大腦」跟「外部工具」安全地串接起來。
- **生活化比喻（Analogy）**：**餐廳點餐系統**。顧客（Host）想吃牛排，透過服務生（Client）把標準菜單需求傳給廚房（Server），廚房做好菜再透過服務生端回給顧客。
- **核心技術重點（Key Facts）**：
  - **MCP Host（主機）**：使用者直接互動的 AI 應用程式，負責管理整體對話與安全權限（例如：Claude Desktop 應用程式、Cursor 編輯器）。
  - **MCP Client（客戶端）**：內建在 Host 裡的通訊模組，負責與 Server 建立「一對一」的專屬連線，處理協定交握（Handshake）。
  - **MCP Server（伺服器）**：輕量級的獨立程式，專門負責對接某個特定資料源或工具（例如：Google Drive Server、SQLite Server），並把能力暴露給 Client。
- **資料來源（Source）**：Doc 2 (*MCP Architecture Overview*, `modelcontextprotocol.io`)
