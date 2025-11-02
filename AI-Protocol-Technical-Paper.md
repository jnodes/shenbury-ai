### **AI Protocol Technical Paper**

### **The Shenbury AI-Powered Provenance Protocol**

Date: October 27, 2025 Author: Shenbury Core Development Team  
Status: DRAFT v1.0

### **Abstract**

The Shenbury AI-Powered Provenance Protocol introduces a decentralized, multi-agent AI system for the cryptographic-grade object verification of high-value cultural artifacts. The primary challenge in the multi-billion dollar art market is information asymmetry and the opacity of provenance, which constrains liquidity and trust. Our protocol solves this by fusing a resilient, self-contained AI stack with an immutable on-chain ledger.

This system is built on a "zero-cost" framework that runs locally with no external dependencies, eliminating API fees and ensuring data privacy. It leverages a stack of proprietary NPX libraries—including AgentDB for high-speed vector storage, ReasoningBank for autonomous closed-loop learning, and claude-flow for swarm coordination—to create self-contained, learning agents. These agents autonomously analyze, verify, and reach a consensus on an artifact's authenticity, with the final verification hash logged immutably on the Ethereum blockchain.

### **1\. Introduction**

The tokenization of Real World Assets (RWAs) has been hampered by a single point of failure: the "oracle problem." An on-chain token is only as reliable as the off-chain data it represents. In the high-value art market, this problem is amplified. Verification is a manual, centralized, and often subjective process, making it impossible to guarantee authenticity in a trustless manner.

The Shenbury AI Protocol is designed to solve this problem at its root. Instead of relying on human oracles, we have built an autonomous AI swarm that functions as an unbiased, data-driven verification engine. This paper details its architecture, from its core philosophy to its specific technical implementation.

### **2\. The Agentic Manifesto (Core Philosophy)**

Our architecture is guided by the "Agentic Manifesto," which prioritizes resilience, autonomy, and security:

* **Failure is Assumed, Recovery is Automated:** The system is designed for fault tolerance. Agents operate in a resilient mesh topology, ensuring that the failure of a single agent does not halt the verification process.  
* **Agents as Stateless, Purpose-Bound Services:** Each AI agent is a small, specialized microservice with a single, dedicated function (e.g., "Chemical Analysis Agent," "Auction History Agent," "Visual Stylometry Agent").  
* **Zero-Trust Security & Immutable Ledgers:** Security is zero-trust. All inter-agent communication is authenticated. The final verification "attestation" is cryptographically hashed and logged to the Ethereum blockchain, creating a permanent, immutable record of provenance.  
* **Humans as Stewards, Not Operators:** Human experts (academics, historians) are used to *train* the AI swarm and provide initial ground-truth data. However, they are removed from the critical path of active operations, ensuring unbiased, data-driven verification.

### **3\. System Architecture: The Shenbury Stack**

The key innovation of the Shenbury stack is its combination of speed, autonomy, and zero recurring cost. The entire system—database, learning model, and embeddings—runs locally, allowing agents to become self-contained learning entities that retain institutional memory without external dependencies.

#### **3.1 Orchestration Layer: agentic-flow**

agentic-flow is the core orchestration platform. It manages the lifecycle of verification tasks, tasking specialized agents and coordinating the flow of data between them. For example, when a new artifact is submitted, agentic-flow initiates a "Verification" task, which in turn activates the necessary "worker" agents (e.g., coder, researcher).

#### **3.2 Swarm Coordination & Memory: claude-flow**

claude-flow provides the memory and coordination backbone for the agent swarm. It allows agents to store and retrieve knowledge using a local-first memory architecture. Its swarm initialization (swarm init topology mesh) creates a resilient, decentralized communication network between agents, enabling complex, collaborative reasoning.

#### **3.3 Foundational Database: AgentDB**

AgentDB is the foundational vector database that acts as the "long-term memory" for the entire swarm. It is optimized for the extreme performance required by real-time agentic systems.

* **Performance:** Achieves 150x faster performance than traditional vector databases through HNSW (Hierarchical Navigable Small World) indexing.  
* **Efficiency:** Utilizes vector quantization to compress memory by 4x to 32x while preserving accuracy, enabling sub-millisecond queries on massive datasets without specialized infrastructure.

#### **3.4 Autonomous Learning: ReasoningBank**

ReasoningBank is our closed-loop learning system, inspired by DeepMind’s autonomous improvement framework. This is what allows the swarm to learn and improve over time.

1. **Evaluates Outcomes:** When a verification is complete (and later confirmed by real-world auction results), ReasoningBank evaluates the accuracy of the agents' contributions.  
2. **Extracts Knowledge:** It extracts reusable knowledge, patterns, and heuristics from the outcome.  
3. **Updates Confidence:** It updates the "confidence score" of the reasoning pathways used, reinforcing successful strategies.  
4. **Weighted Retrieval:** Its memory retrieval algorithm balances semantic similarity, recency, reliability, and diversity, ensuring agents learn from both new and proven information.

#### **3.5 Local Embeddings: transformers.js**

All data (images, chemical analysis reports, provenance documents) is vectorized locally. This is a critical component for both cost and privacy.

* **Engine:** transformers.js using the Xenova/all-MiniLM-L6-v2 model.  
* **Output:** Generates 384-dimensional vectors for all ingested data.  
* **Cost:** After an initial 23MB model download, all embedding operations run offline at **zero marginal cost**, eliminating reliance on external, fee-based embedding APIs.

### **4\. The Verification Workflow: An Example**

1. **Data Ingestion:** A new artifact (e.g., a Ming Dynasty vase) is submitted. All known data is ingested: high-resolution 3D scans, pigment chemical analysis, and known provenance documents.  
2. **Local Embedding:** transformers.js converts all this unstructured data into 384-dimensional vectors.  
3. **Task Orchestration:** agentic-flow initiates a verification task.  
4. **Agent Swarm Query:**  
   * A **Visual Agent** queries AgentDB for visually similar items (shape, glaze, markings).  
   * A **Chemical Agent** queries AgentDB for matches in chemical composition from its database of known-good artifacts.  
   * A **Provenance Agent** queries AgentDB to cross-reference auction records and museum catalogs.  
5. **Reasoning & Consensus:** claude-flow facilitates communication as the agents share their findings. ReasoningBank synthesizes their outputs, weights them based on historical reliability, and generates a final, consolidated "Provenance Confidence Score."  
6. **Attestation:** The full verification report, along with its confidence score and the data used, is cryptographically hashed. This hash is published to the Ethereum blockchain via a smart contract, creating an immutable, trustless, and publicly verifiable "proof of authenticity."

### **5\. Conclusion**

The Shenbury AI-Powered Provenance Protocol solves the RWA oracle problem for high-value art by *becoming* the oracle. By building a fully integrated, self-contained AI stack, we have created an autonomous verification engine that operates without bias, learns from its outcomes, and functions at zero marginal cost. This protocol is the foundation for a new standard of trust, enabling the creation of a secure, transparent, and liquid marketplace for the world's most valuable cultural assets.