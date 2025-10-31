# 神堡：藝術鑑定的AI代理群

## 項目概述

神堡引入了一個去中心化的自包含智能基礎設施，用於驗證和代幣化美術品和歷史文物。其核心是**AI代理群**，結合了本地向量推理、閉環學習和鏈上來源。每個代理都使用完全本地的堆棧獨立運行——數據庫、嵌入和學習層——不依賴外部API或雲系統。

**[English Version](README.md) | [中文版](README-zh.md)**

如需詳細的技術文檔、商業模式和代幣經濟學，請參閱我們的[白皮書](public/whitepaper-zh.html)。

## 核心技術特性

### AI代理群
- **本地執行**：所有AI處理都在本地運行，無需雲依賴
- **自包含代理**：具有嵌入式知識庫的獨立操作
- **專業角色**：專門處理成像、光譜學和文檔分析的代理
- **閉環學習**：通過強化反饋持續改進

### 技術架構
- **AgentDB**：具有HNSW索引和4-32倍壓縮的本地向量數據庫
- **ReasoningBank**：受DeepMind框架啟發的閉環學習系統
- **本地嵌入**：使用Xenova/all-MiniLM-L6-v2模型的transformers.js（384維向量）
- **無外部依賴**：無雲服務的完全自主操作

## 快速開始

### 前提條件
- Node.js (v14或更高版本)
- npm (v6或更高版本)

### 安裝
```bash
# 克隆倉庫
git clone https://github.com/jnodes/shenbury-ai.git
cd shenbury-ai

# 安裝依賴
npm install
```

### 運行應用程序
```bash
# 啟動本地開發服務器
npm run dev
```

訪問`http://localhost:3000`查看應用程序。

## 項目結構
```
shenbury-main/
├── public/                 # 靜態資源
│   ├── assets/            # 圖像和媒體
│   ├── js/                # JavaScript文件
│   ├── index.html         # 主HTML文件
│   ├── index-zh.html      # 主HTML文件中文版
│   ├── whitepaper.html    # 白皮書HTML文件
│   ├── whitepaper-zh.html # 白皮書HTML文件中文版
│   └── favicon.svg        # 圖標
├── README.md              # 項目文檔
├── README-zh.md           # 項目文檔中文版
├── SHENBURY-DAO-OPERATING-AGREEMENT.md # DAO營運協議
└── SHENBURY-DAO-OPERATING-AGREEMENT-ZH.md # DAO營運協議中文版
```

## 文檔

- **[白皮書](public/whitepaper-zh.html)** - 技術文檔和系統架構
- **[Whitepaper (English)](public/whitepaper.html)** - Technical documentation and system architecture
- **[DAO營運協議](SHENBURY-DAO-OPERATING-AGREEMENT-ZH.md)** - 治理和運營框架
- **[DAO Operating Agreement (English)](SHENBURY-DAO-OPERATING-AGREEMENT.md)** - Governance and operational framework

## 條款和條件

通過訪問或使用神堡，您同意受本倉庫中規定的條款和條件約束。該項目"按原樣"提供，不提供任何形式的保證。

### 免責聲明
神堡是一個實驗性項目，不應被視為投資建議。數字資產的價值高度波動，可能導致重大財務損失。

### DAO治理協議
購買者同意管轄項目的神堡DAO LLC營運協議。完整的營運協議可在[SHENBURY-DAO-OPERATING-AGREEMENT-ZH.md](SHENBURY-DAO-OPERATING-AGREEMENT-ZH.md)文件中找到。

## 許可證

該項目根據MIT許可證授權 - 請參閱[LICENSE](LICENSE)文件了解詳細信息。

---

**© 2025 神堡. 版權所有.**