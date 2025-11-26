# TruthMesh 

Prototype Demo: https://truthweave-mind.lovable.app

  TruthMesh envisions a world where intelligence is trustworthy by default — where every claim, insight, and computation produced by AI agents comes with transparent provenance, cryptographic verification, and community-driven accountability. Today’s AI models generate answers that are powerful but opaque. Sources disappear, citations are 

# TruthMesh — Verifiable Multi-Agent Intelligence

**Tagline:** A decentralized AI system for verification, truth synthesis, and consensus intelligence.

## Summary
TruthMesh is a multi-agent platform that verifies claims by retrieving evidence, computing cross-model consensus, scoring sources, building a Knowledge Graph (JSON-LD/RDF), and publishing verifiable Knowledge Assets to the OriginTrail DKG (or mock DKG for local demo). It includes token-staked community notes, reputation, and optional x402 micropayment gating patterns.

## Repo Contents
- /docs — docs, anchoring, integration notes
- /assets — logo (SVG), diagrams (Mermaid)
- /dkg-schemas — JSON-LD schemas + examples
- /agents — Node.js and Python agent implementations (mock & adapters)
- /appcanvas — Node graph JSON and UI page configs (for App Canvas import)
- /demo — mock DKG server, sample pages
- /tokenomics — token spec and simulation
- /video — ≤5 min demo script + storyboard
- /pitch-deck — slide content

## Quick start (local)
1. Install Node 18+, Python 3.10+, npm
2. `git clone <repo>`
3. Start mock DKG:
   ```bash
   node demo/mock-dkg/server.js

cd agents/node
npm install
node orchestrator.js "Climate change"

n
TruthMesh transforms AI from a “black box answer generator” into a verifiable knowledge fabric, where:
1. Every AI output is anchored across a decentralized knowledge graph.
Agents automatically collect evidence, align perspectives, detect contradictions, and publish structured findings as DKG-backed truth-assets.
2. Multi-agent ecosystems collaborate instead of hallucinating.
Retriever agents, verifier agents, ontology agents, and reputation-scoring agents work together, forming a self-correcting mesh of intelligence that continually improves through usage and contribution.
3. Knowledge becomes a public resource, not a corporate silo.
Anyone — developers, researchers, enterprises — can plug into the TruthMesh graph and immediately access auditable, machine-readable, bias-aware knowledge.
4. AI applications become trust-native.
Instead of embedding a single brittle model, TruthMesh-powered apps build on top of a verifiable truth layer, enabling:
Transparent research
Verified analytics
Credible decision support
Source-aware copilots
Multi-model consensus engines
5. Truth creation becomes collaborative, modular, and decentralized.
Every agent can contribute. Every user can validate. Every dataset becomes interoperable.
TruthMesh turns the internet into a living, evolving mesh of verified knowledge, not static pages.

🌟 The Ultimate Goal
To establish the global standard for verifiable AI — a composable ecosystem where:
Models are accountable
Insights are reproducible
Knowledge is interoperable
Truth is cryptographically anchored
And intelligence can be trusted, scaled, and audited
TruthMesh isn’t just a platform — it’s the future infrastructure for credible AI ecosystems, built for the next generation of decentralized applications, scientific discovery, and knowledge automation.

TruthMesh: Verifiable Multi-Agent Truth Alignment System
Trusted AI built on the OriginTrail Decentralized Knowledge Graph (DKG), NeuroWeb (Polkadot), MCP, and x402.
<p align="center"> <img src="assets/logo/truthmesh-logo.png" width="180"/> </p>
TruthMesh is a decentralized, multi-agent truth-verification system that aligns AI-generated knowledge with human-curated sources, detects divergences, computes reputation, and publishes verifiable Knowledge Assets to the OriginTrail Decentralized Knowledge Graph (DKG).
It turns AI from a “black box” into a transparent, cryptographically-verifiable knowledge fabric.
🚀 Key Features
🔎 Truth Alignment Engine
Compares Grokipedia vs. Wikipedia topics. Detects:
Missing facts
Bias
Contradictions
Hallucinations
Divergence graphs
🤖 Multi-Agent Architecture (MCP)
Agents include:
Retriever Agent
Alignment Agent
Verifier Agent
Reputation Agent
Publisher Agent
Orchestrator Agent
All agents communicate through the Model Context Protocol.
🧠 Verifiable Knowledge Layer (DKG)
Agents publish structured JSON-LD Knowledge Assets with:
Provenance
Claim-level confidence
Source URLs
Timestamps
Hash-anchored integrity (NeuroWeb)
💰 Trust Layer + x402 Micropayments
Optional economic layer for:
Rewarding high-quality notes
Slashing malicious contributions
Gating premium truth-reports via x402 microtransactions
📊 Reputation System
Computes Sybil-resistant scores using PageRank + stake weighting from Umanitek’s social graph dataset.
🖥️ App Canvas UI (Low-Code)
A visual interface to run the full pipeline:
Input → Agents → DKG Publish → Anchoring → Visual Diff

Repository Structure
truthmesh/
 ├─ agents/
 │   ├─ retriever/
 │   ├─ aligner/
 │   ├─ verifier/
 │   ├─ reputation/
 │   └─ publisher/
 ├─ orchestrator/
 ├─ dkg/
 │   ├─ schemas/
 │   ├─ examples/
 │   └─ client.js
 ├─ app-canvas/
 │   ├─ nodes/
 │   ├─ pages/
 ├─ mock-dkg/
 ├─ tokenomics/
 ├─ scripts/
 ├─ docs/
 │   ├─ architecture.md
 │   ├─ runbook.md
 │   └─ video-script.md
 └─ assets/
     └─ truthmesh-logo.png
🧬 Architecture Overview
User Input (topic)
     │
     ▼
🧵 Orchestrator Agent (MCP)
     │
 ┌───────────────┬────────────────┬─────────────────────┬─────────────────────┐
 ▼               ▼                ▼                     ▼
Retriever     Alignment        Verifier            Reputation
Agent         Agent            Agent               Agent
 │             │                 │                     │
 ▼             ▼                 ▼                     ▼
Fetched     Parallel         Cross-source         Reputation
Sources     Comparisons      validation           scores
 │             │                 │                     │
 └─────────────┴─────────────────┴─────────────────────┘
                       ▼
                Publisher Agent
                       ▼
       Publishes Knowledge Asset (JSON-LD)
                       ▼
              OriginTrail DKG Edge Node
                       ▼
           Anchoring on NeuroWeb (Polkadot)
                       ▼
        TruthMesh Viewer / API / App Canvas UI
🛠️ Installation & Setup
1. Clone the repo
git clone https://github.com/<your-org>/truthmesh.git
cd truthmesh
2. Install dependencies
Node.js agents:
cd agents/node
npm install
Python agents:
pip install -r requirements.txt
DKG Client:
cd dkg
npm install
🌐 Running the Mock DKG (local testing)
cd mock-dkg
node server.js
This mimics:
POST /createAsset
GET /kassets/:id
GET /query
UI:
http://localhost:4001/kassets
🤖 Running the Multi-Agent Pipeline
Run a full truth-alignment flow:
cd orchestrator
node orchestrator.js "Climate change"
Output includes:
Grokipedia → extracted knowledge
Wikipedia → extracted knowledge
Divergence report
Claim-level verification
Reputation-weighted trust score
Final Knowledge Asset file
DKG publish confirmation
📦 DKG Knowledge Assets (Schemas)
The repo includes full JSON-LD schemas:
TruthAlignmentAsset.jsonld
Metadata + evidence + side-by-side diff.
ProvenanceAsset.jsonld
Source URLs, timestamps, agent IDs.
ReputationAsset.jsonld
Graph-based credibility.
CommunityNoteAsset.jsonld
Crowd-based fact-checks + moderation.
DeepfakeNoteAsset.jsonld (optional)
Verifiable notes for suspected AI-faked media.
Example output:
{
  "@context": "https://schema.origintrail.io/context.json",
  "@type": "TruthAlignmentAsset",
  "topic": "Climate change",
  "divergences": [...],
  "provenance": [...],
  "confidence": 0.92,
  "anchors": {
    "neuroWebHash": "0xabc123..."
  }
}
🧠 Agent Roles (Detailed)
1. Retriever Agent
Fetches Grokipedia and Wikipedia content
Normalizes data
Outputs JSON-LD stubs
2. Alignment Agent
Runs LLM-based comparisons
Detects:
Factual differences
Missing claims
POV bias
Hallucinations
3. Verifier Agent
Cross-checks claims across:
DKG
External sources
Semantic similarity
Flags contradictions
4. Reputation Agent
Computes PageRank-based trust
Adds stake-weighted credibility
Publishes ReputationAsset
5. Publisher Agent
Converts all evidence to Knowledge Assets
Publishes to the DKG
Optionally gates with x402
Anchors on NeuroWeb

Tokenomics (Optional)
Stake–Reward–Slash Mechanism
Stake TRAC/x402 to become a contributor
Earn micropayments for verified notes
Slash low-quality or malicious contributors
Premium x402-Gated Features
High-confidence composite reports
Reputation-enriched bundles
Verified media analysis
🖥️ App Canvas UI
This repo includes all App Canvas configs:
Page components
Flow nodes
Agent invocation blocks
DKG publishing nodes
Visual difference graphs
Import into App Canvas to get a ready-to-run UI.
🎬 Demo Run (For the Hackathon)
The repo includes:
/docs/video-script.md
/docs/architecture.md
/docs/slides.md
The demo shows:
Entering topic
Agents running
Divergence visual map
DKG publish
Anchoring
Loading the TruthMesh result
Viewing reputation + provenance
Judges see the entire Agent–Knowledge–Trust flow working end to end.

Contributing
Pull requests welcome.
Please open an issue for bugs, enhancements, or ideas.
