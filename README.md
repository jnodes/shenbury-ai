# Shenbury: AI-Verified Art & Asset Tokenization 神堡：AI鑑定的藝術品與資產代幣化

## Project Overview 項目概述

Shenbury Ltd. is a Hong Kong-based asset tokenization company. We are unlocking the $60B+ illiquid art market by combining two unique assets:

1.  **The Assets:** Our $257M+ portfolio of museum-grade Chinese imperial ceramics.
2.  **The Technology:** Our proprietary "Dynasty X" AI-Powered Provenance Protocol, a local-first AI swarm built to verify high-value artifacts.

We are not a theoretical platform; we are an asset-backed company. Our first initiative is the tokenization of our own legal-and-physical-custody collection, giving public investors access to this asset class for the first time.

**[English Version](README.md) | [中文版](README-zh.md)**

For detailed technical documentation, our business model, and tokenomics, please refer to our [Whitepaper](public/whitepaper.html).

## Key Technical Features 核心技術特性

Our "Dynasty X" AI Protocol is our core technology, a decentralized, self-contained intelligent infrastructure.

### AI Agent Swarm AI代理群
- **Local Execution**: All AI processing runs locally without cloud dependencies.
- **Self-Contained Agents**: Independent operation with embedded knowledge bases.
- **Specialized Roles**: Dedicated agents for imaging, spectroscopy, and documentation analysis.
- **Closed-Loop Learning**: Continuous improvement through reinforcement feedback, trained by our in-house art experts.

### Technical Architecture 技術架構
- **AgentDB**: Local vector database with HNSW indexing and 4-32x compression.
- **ReasoningBank**: Closed-loop learning system inspired by DeepMind's framework.
- **Local Embeddings**: transformers.js with Xenova/all-MiniLM-L6-v2 model (384-dimensional vectors).
- **No External Dependencies**: Fully autonomous operation without cloud services.

## The Collection (Initial Assets)

Our launch is built on six foundational, world-class artifacts from our collection, with a combined valuation over **$257,000,000 USD**. These pieces are held in legal custody by Shenbury Ltd. and form the underlying assets for the SHBY token.

View the full collection here: [Shenbury Collection](public/index.html#auctions)

## Project Leadership

Shenbury is led by a public team to ensure trust and accountability.
- **Technology & Finance:** [Jesse Brown](https://linkedin.com/in/digitalassets) (Project Lead)
- **Provenance & Art:** *Our Head of Provenance & Chief Art Historian will be announced prior to launch.*

## Quick Start (For Developers) 快速開始

### Prerequisites 前提條件
- Node.js (v14 or higher)
- npm (v6 or higher)

### Installation 安裝
```bash
# Clone the repository
git clone https://github.com/jnodes/shenbury-ai.git
cd shenbury-ai

# Install dependencies
npm install
```

### Running the Application 運行應用程序
```bash
# Start the local development server
npm run dev
```

Visit http://localhost:3000 to view the application.

## Documentation 文檔
- **[Whitepaper](public/whitepaper.html)** - Business model, tokenomics, and asset overview.
- **[AI Protocol Technical Paper](public/ai-protocol.html)** - In-depth technical architecture of the "Dynasty X" AI Protocol.
- **[Operating Agreement](OPERATING-AGREEMENT.md)** - Legal framework and governance for Shenbury Ltd. (Hong Kong).

## Terms & Conditions 條款和條件

By accessing or using Shenbury, you agree to be bound by the terms and conditions set forth in this repository and in the Operating Agreement.

### Disclaimer 免責聲明

Shenbury is an asset-backed tokenization project. The value of digital assets is volatile. This is not investment advice. The legal framework governing the tokens is detailed in the Operating Agreement.

### License 許可證

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

**© 2025 Shenbury Ltd. 神堡. All rights reserved.**