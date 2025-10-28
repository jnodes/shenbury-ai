# 神堡：藝術鑑定的AI代理群

## 項目概述

神堡引入了一個去中心化的自包含智能基礎設施，用於驗證和代幣化美術品和歷史文物。其核心是**AI代理群**，結合了本地向量推理、閉環學習和鏈上來源。每個代理都使用完全本地的堆棧獨立運行——數據庫、嵌入和學習層——不依賴外部API或雲系統。

**[English Version](README.md) | [中文版](README-zh.md)**

## 核心功能

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

### 代幣經濟學
- **代幣**：SHBY（神堡來源代幣）
- **總供應量**：1,000,000,000 SHBY
- **無預售**：代幣由MetaDAO鑄造和管理
- **效用**：治理、驗證折扣和生態系統訪問

## 商業模式

神堡的可持續商業模式旨在從600億美元以上的全球藝術市場中獲取價值，同時建立全面的驗證生態系統。收入模式多元化，以確保長期可行性和增長。

### 收入來源
1. **按次驗證**：對單個文物進行AI驗證，費用根據複雜性和價值範圍從5,000美元到100,000美元以上不等。
2. **訂閱服務**：為畫廊、拍賣行和收藏家提供的月度/年度驗證套餐，價格從每月500美元到100,000美元不等。
3. **企業授權**：為大型機構提供的API訪問和白標解決方案，年度授權費從100,000美元到500萬美元以上不等。
4. **數據貨幣化**：將匿名聚合數據出售給研究機構和市場分析公司，每份報告5,000美元到500,000美元不等。
5. **代幣門控服務**：為SHBY代幣持有者提供折扣和早期訪問權限。

### 市場機會
全球藝術市場規模超過600億美元，數字化和驗證服務滲透率低於5%。神堡定位於高端市場，專注於價值超過100萬美元的文物。

### 競爭優勢
- **技術領先**：本地AI代理群提供無與倫比的性能和隱私
- **成本效益**：自主運行將驗證成本降低90%以上
- **可擴展性**：無雲依賴實現無限擴展
- **信任**：鏈上來源提供不可篡改的驗證記錄

### 收入預測
- **第1年**：1000萬美元
- **第2年**：3000萬美元
- **第3年**：1億美元
- **第5年**：5億美元以上

## DAO治理

神堡作為一個由智能合約和社區共識治理的去中心化自治組織(DAO)運營。DAO不擁有任何實物資產，包括藝術品。所有藝術收藏和實物資產仍為其各自所有者擁有。

### DAO治理協議
購買者同意管轄項目的神堡DAO LLC營運協議。完整的營運協議可在[SHENBURY-DAO-OPERATING-AGREEMENT-ZH.md](SHENBURY-DAO-OPERATING-AGREEMENT-ZH.md)文件中找到。

[English Version](SHENBURY-DAO-OPERATING-AGREEMENT.md)

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