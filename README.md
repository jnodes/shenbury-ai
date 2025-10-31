# Shenbury: AI Agent Swarm for Art Authentication 神堡：藝術鑑定的AI代理群

## Project Overview 項目概述

Shenbury introduces a decentralized, self-contained intelligent infrastructure for authenticating and tokenizing fine art and historical artifacts. At its core is the **AI Agent Swarm**, combining local vector reasoning, closed-loop learning, and on-chain provenance. Each agent operates independently with a fully local stack—database, embeddings, and learning layer—without reliance on external APIs or cloud systems.

神堡引入了一個去中心化的自包含智能基礎設施，用於驗證和代幣化美術品和歷史文物。其核心是**AI代理群**，結合了本地向量推理、閉環學習和鏈上來源。每個代理都使用完全本地的堆棧獨立運行——數據庫、嵌入和學習層——不依賴外部API或雲系統。

**[English Version](README.md) | [中文版](README-zh.md)**

For detailed technical documentation, business model, and tokenomics, please refer to our [Whitepaper](public/whitepaper.html). 如需詳細的技術文檔、商業模式和代幣經濟學，請參閱我們的[白皮書](public/whitepaper-zh.html)。

## Key Technical Features 核心技術特性

### AI Agent Swarm AI代理群
- **Local Execution**: All AI processing runs locally without cloud dependencies 本地執行：所有AI處理都在本地運行，無需雲依賴
- **Self-Contained Agents**: Independent operation with embedded knowledge bases 自包含代理：具有嵌入式知識庫的獨立操作
- **Specialized Roles**: Dedicated agents for imaging, spectroscopy, and documentation analysis 專業角色：專門處理成像、光譜學和文檔分析的代理
- **Closed-Loop Learning**: Continuous improvement through reinforcement feedback 閉環學習：通過強化反饋持續改進

### Technical Architecture 技術架構
- **AgentDB**: Local vector database with HNSW indexing and 4-32x compression AgentDB：具有HNSW索引和4-32倍壓縮的本地向量數據庫
- **ReasoningBank**: Closed-loop learning system inspired by DeepMind's framework ReasoningBank：受DeepMind框架啟發的閉環學習系統
- **Local Embeddings**: transformers.js with Xenova/all-MiniLM-L6-v2 model (384-dimensional vectors) 本地嵌入：使用Xenova/all-MiniLM-L6-v2模型的transformers.js（384維向量）
- **No External Dependencies**: Fully autonomous operation without cloud services 無外部依賴：無雲服務的完全自主操作

## Quick Start 快速開始

### Prerequisites 前提條件
- Node.js (v14 or higher) Node.js (v14或更高版本)
- npm (v6 or higher) npm (v6或更高版本)

### Installation 安裝
```bash
# Clone the repository 克隆倉庫
git clone https://github.com/jnodes/shenbury-ai.git
cd shenbury-ai

# Install dependencies 安裝依賴
npm install
```

### Running the Application 運行應用程序
```bash
# Start the local development server 啟動本地開發服務器
npm run dev
```

Visit `http://localhost:3000` to view the application. 訪問`http://localhost:3000`查看應用程序。

## Project Structure 項目結構
```
shenbury-main/
├── public/                 # Static assets 靜態資源
│   ├── assets/            # Images and media 圖像和媒體
│   ├── js/                # JavaScript files JavaScript文件
│   ├── index.html         # Main HTML file 主HTML文件
│   ├── index-zh.html      # Chinese version of main HTML file 主HTML文件中文版
│   ├── whitepaper.html    # Whitepaper HTML file 白皮書HTML文件
│   ├── whitepaper-zh.html # Chinese version of whitepaper HTML file 白皮書HTML文件中文版
│   └── favicon.svg        # Favicon 圖標
├── README.md              # Project documentation 項目文檔
├── README-zh.md           # Chinese version of project documentation 項目文檔中文版
├── SHENBURY-DAO-OPERATING-AGREEMENT.md # DAO operating agreement DAO營運協議
└── SHENBURY-DAO-OPERATING-AGREEMENT-ZH.md # Chinese version of DAO operating agreement DAO營運協議中文版
```

## Documentation 文檔

- **[Whitepaper](public/whitepaper.html)** - Technical documentation and system architecture 白皮書 - 技術文檔和系統架構
- **[Whitepaper (Chinese)](public/whitepaper-zh.html)** - Technical documentation and system architecture (Chinese) 白皮書 - 技術文檔和系統架構（中文）
- **[DAO Operating Agreement](SHENBURY-DAO-OPERATING-AGREEMENT.md)** - Governance and operational framework DAO營運協議 - 治理和運營框架
- **[DAO Operating Agreement (Chinese)](SHENBURY-DAO-OPERATING-AGREEMENT-ZH.md)** - Governance and operational framework (Chinese) DAO營運協議 - 治理和運營框架（中文）

## Terms & Conditions 條款和條件

By accessing or using Shenbury, you agree to be bound by the terms and conditions set forth in this repository. The project is provided "as is" without warranty of any kind. 通過訪問或使用神堡，您同意受本倉庫中規定的條款和條件約束。該項目"按原樣"提供，不提供任何形式的保證。

### Disclaimer 免責聲明
Shenbury is an experimental project and should not be considered investment advice. The value of digital assets is highly volatile and may result in significant financial losses. 神堡是一個實驗性項目，不應被視為投資建議。數字資產的價值高度波動，可能導致重大財務損失。

### DAO Governance Agreement DAO治理協議
Purchasers agree to the Shenbury DAO LLC's operating agreement governing the project. The complete operating agreement is available in the [SHENBURY-DAO-OPERATING-AGREEMENT.md](SHENBURY-DAO-OPERATING-AGREEMENT.md) file. 購買者同意管轄項目的神堡DAO LLC營運協議。完整的營運協議可在[SHENBURY-DAO-OPERATING-AGREEMENT.md](SHENBURY-DAO-OPERATING-AGREEMENT.md)文件中找到。

## License 許可證

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details. 該項目根據MIT許可證授權 - 請參閱[LICENSE](LICENSE)文件了解詳細信息。

---

**© 2025 Shenbury 神堡. All rights reserved.** 版權所有.