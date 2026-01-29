# QORA 

## Executive Summary

**QORA is the world's fastest Layer-1 blockchain with mandatory privacy and native social infrastructure.**

- **400ms finality** (10-50x faster than any EVM chain)
- **Mandatory ZK-SNARK privacy** for all tokens
- **Native encrypted Chat (video, voice), Auth (user, company), KYC (user, company), ID (@qor), Oracle (crypto , commodities, forx with signals) and AI with decentralized agent**
- **Full EVM compatibility** with 34 custom modules

---

## 1. What is Qora going to make?

### The Product

QORA is a complete financial and social operating system built on a revolutionary DAG-based blockchain. We've solved the blockchain trilemma by building consensus from scratch instead of forking existing solutions.

### Three Groundbreaking Innovations

#### Innovation #1: Sub-400ms Finality (Fastest in Industry)

| Chain | Block Time | Finality | Our Advantage |
|-------|------------|----------|---------------|
| Ethereum | 12 sec | 12-15 min | **120x faster** |
| Solana | 400ms | 400ms | **4-8x faster** |
| Polygon | 2 sec | 30 min | **360x faster** |
| Avalanche | 2 sec | 2 sec | **20x faster** |
| **QORA** | **50-100ms** | **Instant** | - |

**How Qora will achieve this:**
- **DAG Consensus**: Parallel block creation instead of sequential
- **VRF/VDF Lottery**: Cryptographic proposer selection (no round timeouts)
- **Proposal-First Model**: Voting happens during block creation, not after
- **GHOST Fork Choice**: Deterministic ordering without BFT rounds

#### Innovation #2: Mandatory Privacy Layer

Every token on QORA has built-in privacy using PLONK+KZG zero-knowledge proofs:

| Feature | Description |
|---------|-------------|
| **Shield** | Convert public tokens to private |
| **Unshield** | Convert private tokens back to public |
| **Private Transfer** | Send privately without revealing amounts |
| **Stealth Addresses** | Recipients can't be linked to transactions |
| **View Tags** | 99.6% faster scanning for recipients |

**Why mandatory?** Optional privacy fails because:
- Chainalysis can track "clean" vs "mixed" coins
- Exchanges reject coins that touched privacy pools
- Users who need privacy are automatically suspicious

**Our approach**: ALL tokens are private by default. No taint analysis possible.

#### Innovation #3: Native Social + AI Infrastructure

Unlike chains where chat/video are dApps, QORA has native:

| Feature | Technology | Capability |
|---------|------------|------------|
| **Encrypted Chat** | X3DH + Kafka | End-to-end encrypted DMs and groups |
| **Video Calls** | LiveKit WebRTC | P2P and group video with recording |
| **Voice Calls** | LiveKit | Audio calls with presence detection |
| **AI Assistants** | vLLM/LocalAI | On-chain billing, auto-reply bots |
| **Chat Bots** | Webhook API | Telegram-style bots for groups |
| **Message Backup** | IPFS | Encrypted cloud backup |

#### Innovation #4: Enterprise Authentication (QoraAuth)

Passwordless blockchain auth for companies - like Magic Link but 5x cheaper:

| Feature | Description |
|---------|-------------|
| **Passwordless Login** | Email → 6-digit code → blockchain session |
| **Multi-Wallet 2FA** | Main wallet + Auth wallet (on-chain 2FA) |
| **Company Integration** | Simple API key, no complex setup |
| **Session Management** | Configurable expiry, instant revocation |
| **Zero Secrets** | Pure cryptographic verification |

**Pricing**: $0.01/MAU vs Magic Link's $0.05/MAU = **80% cheaper**

**B2B Revenue**: High-margin, sticky, recurring revenue from enterprises.

---

## 2. How far along are you?

### Development Status: Production-Ready Codebase

| Component | Status | Details |
|-----------|--------|---------|
| **Consensus Engine** | ✅ Complete | DAG with VRF/VDF, proposal-first model |
| **Privacy Module** | ✅ Complete | PLONK+KZG circuits compiled, production SRS |
| **34 SDK Modules** | ✅ Complete | DEX, CLOB, perpetuals, oracle, etc. |
| **EVM Integration** | ✅ Complete | Full compatibility with pointer contracts |
| **Chat Service** | ✅ Complete | Kafka integration, E2E encryption |
| **Video/Voice** | ✅ Complete | LiveKit integration |
| **AI System** | ✅ Complete | Validator coordination, billing |
| **QoraAuth** | ✅ Complete | Passwordless login, multi-wallet 2FA |
| **QoraID** | ✅ Complete | @qor or companies can create @.. |
| **QoraKYC** | ✅ Complete | Onchain KYC infrastructure|
| **Security Audit** | ✅ Complete | 27 issues identified and fixed |
| **Docker Deploy** | ✅ Complete | Multi-node cluster ready |
| **Public Testnet** | 🔄 In Progress | Launching Q2 2026 |
| **Mainnet** | 📅 Planned | Q4 2026 |

### Codebase Statistics

```
Total Go Files:        1,200+
Total Lines of Code:   300,000+
Custom Modules:        34
Proto Definitions:     50+
Test Coverage:         75%+
```

---

## 3. Tech Stack

### Core Blockchain

| Layer | Technology | Purpose |
|-------|------------|---------|
| **Language** | Go 1.24 | Performance + safety |
| **Framework** | Cosmos SDK (forked) | Module architecture |
| **Consensus** | Custom DAG (qora-neuron) | Replaces Tendermint |
| **Privacy** | PLONK+KZG (gnark) | ZK-SNARK proofs |
| **Randomness** | Curve25519 VRF | Lottery fairness |
| **Time-Lock** | Quadratic Residue VDF | Anti-grinding |
| **EVM** | go-ethereum | Smart contracts |
| **State** | IAVL Tree | Merkle proofs |

### Communication Infrastructure

| Layer | Technology | Purpose |
|-------|------------|---------|
| **Messaging** | Apache Kafka | Real-time message streaming |
| **Video/Voice** | LiveKit | WebRTC infrastructure |
| **Encryption** | X3DH + Double Ratchet | Forward secrecy |
| **Key Exchange** | X25519 | ECDH key agreement |
| **Signing** | Ed25519 | Message authentication |
| **Storage** | IPFS | Decentralized backup |

### AI Infrastructure

| Layer | Technology | Purpose |
|-------|------------|---------|
| **Inference** | vLLM / LocalAI | GPU-accelerated LLMs |
| **Billing** | On-chain module | Token-based payments |
| **Verification** | Multi-validator | Consensus on outputs |
| **Hardware** | RTX 4090 / A100 | Validator requirements |

### AI Tools Used in Development

| Tool | Usage |
|------|-------|
| **Claude Code** | Security audit, vulnerability fixes |
| **GitHub Copilot** | Code completion |

---

## 4. The 34 QORA Modules

### Trading & DeFi (6 modules)

| Module | Purpose | Key Features |
|--------|---------|--------------|
| **DEX** | Batch order matching | CosmWasm integration, in-memory matching |
| **CLOB** | Central limit orderbook | Price-time matching, MEV protection |
| **PERPETUALS** | Leveraged trading | Funding rates, liquidation engine |
| **LEVERAGE** | Lending protocol | Cross-collateral, interest rates |
| **PRICES** | Price tracking | Historical snapshots, oracle integration |
| **ORACLE** | Asset pricing | Validator voting, weighted median |

### Privacy & Security (3 modules)

| Module | Purpose | Key Features |
|--------|---------|--------------|
| **PRIVACY** | ZK-SNARK transfers | Shield/unshield, stealth addresses |
| **QRC20** | Privacy tokens | Mandatory privacy, auto EVM pointer |
| **RATELIMIT** | DoS protection | Per-address limits, configurable |

### Account & Auth (4 modules)

| Module | Purpose | Key Features |
|--------|---------|--------------|
| **ACCOUNTPLUS** | Smart accounts | Custom authentication, plugins |
| **SUBACCOUNTS** | Account hierarchy | Sub-account permissions |
| **QORAAUTH** | Multi-wallet auth | 2-wallet security, company login |
| **TOKENFACTORY** | Token creation | Permissionless, admin controls |

### Communication (3 modules)

| Module | Purpose | Key Features |
|--------|---------|--------------|
| **CHAT** | On-chain messaging | E2E encryption, groups, bots |
| **AI** | AI integration | Inference billing, model registry |
| **SENDING** | Coin transfers | Multi-recipient, conditional |

### Infrastructure (10 modules)

| Module | Purpose |
|--------|---------|
| **EVM** | Ethereum compatibility |
| **EPOCH** | Time-based events |
| **MINT** | Token inflation |
| **REWARDS** | Reward distribution |
| **REVSHARE** | Revenue sharing |
| **AFFILIATES** | Referral system |
| **VAULT** | Token lockup |
| **VEST** | Vesting schedules |
| **FEETIERS** | Dynamic fees |
| **BRIDGE** | Cross-chain transfers |

### Utilities (8 modules)

| Module | Purpose |
|--------|---------|
| **ASSETS** | Asset metadata |
| **LISTING** | Asset whitelisting |
| **GOVPLUS** | Enhanced governance |
| **INDEXER** | TX indexing |
| **STATS** | Analytics |
| **DELAYMSG** | Scheduled execution |
| **BLOCKTIME** | Block timing |
| **STORE** | KV utilities |

---

## 5. Consensus Deep Dive

### Why Tendermint is the Bottleneck

Traditional Cosmos chains use Tendermint BFT:

```
Round 0: Propose (wait for timeout)
       ↓
       Prevote (wait for 2/3 votes)
       ↓
       Precommit (wait for 2/3 votes)
       ↓
       Commit

Each round: 250-500ms minimum
Total: 1-3 seconds per block
```

### QORA's DAG Consensus

```
Parallel Block Creation:
  Validator A creates block ──┐
  Validator B creates block ──┼── All in parallel
  Validator C creates block ──┘
         ↓
  VRF Lottery (instant winner selection)
         ↓
  Async Vote Collection (during next block creation)
         ↓
  Instant Finality (on 2/3+ votes)

Total: 50-100ms per level
```

### Key Innovations

#### 1. VRF Lottery (Verifiable Random Function)

```go
// Instead of round-robin proposer selection:
winner = validator with lowest VRF_output
where VRF_output = VRF_prove(private_key, slot_number)

// Stake-weighted: more stake = more lottery tickets
threshold = base_threshold / voting_power
eligible = VRF_output < threshold
```

**Benefits:**
- No waiting for "your turn"
- Unpredictable winner (MEV protection)
- Verifiable by all validators

#### 2. VDF Time-Lock (Verifiable Delay Function)

```go
// Prevents grinding attacks
VDF_output = compute_VDF(VRF_output, difficulty)
// Takes ~14 seconds to compute
// Takes ~350ms to verify

// Next block's VRF input includes VDF output
// Attacker can't try multiple VRF inputs quickly
```

#### 3. Proposal-First Consensus

```go
// Traditional: Block → Vote → Finalize
// QORA: Proposal → Async Vote → Finalized Block

type Proposal struct {
    BlockData      []byte
    ExecutionResult StateRoot  // Pre-computed!
    VRFProof       []byte
    VDFProof       []byte
}

// Voting happens while next proposal is created
// No wasted time waiting for consensus
```

#### 4. GHOST Fork Choice

```go
// Heaviest sub-DAG wins (not longest chain)
func weight(block) uint64 {
    return 1 + sum(weight(child) for child in block.children)
}

// Deterministic: all validators agree on same fork
// Fast: no BFT rounds needed
```

### Performance Comparison

| Metric | Tendermint | QORA DAG | Improvement |
|--------|------------|----------|-------------|
| Block Time | 1-3 sec | 50-100ms | **10-60x** |
| Finality | 2 rounds | Instant | **Eliminated** |
| Proposers/block | 1 | Many | **Parallel** |
| TX Latency | 3-6 sec | 100-200ms | **15-60x** |
| Throughput | 10k TPS | 100k+ TPS | **10x+** |

---

## 6. Privacy Architecture

### The Problem with Optional Privacy

```
User A: Has 100 ETH
User A: Sends 50 ETH to Tornado Cash
User A: Withdraws 50 ETH from Tornado Cash
Chain analysis: "These 50 ETH touched a mixer = suspicious"
Exchange: "We won't accept these coins"
```

**Result**: Optional privacy creates a two-tier system where private coins are worth less.

### QORA's Solution: Mandatory Privacy

```
All QRC20 tokens are private by default
Public ←→ Private conversion via Shield/Unshield
No way to identify "mixed" vs "clean" coins
All coins are equal
```

### ZK-SNARK Implementation

#### Circuit Types

| Circuit | Constraints | Purpose |
|---------|-------------|---------|
| ShieldCircuit | 885 | Public → Private |
| UnshieldCircuit | 19,552 | Private → Public |
| PrivateTransferCircuit | 19,553 | Private → Private |

#### Cryptographic Primitives

| Primitive | Implementation | Purpose |
|-----------|----------------|---------|
| Curve | BN254 (BabyJubJub) | ZK-friendly elliptic curve |
| Hash | MiMC | ZK-friendly hash function |
| Commitment | Pedersen | Binding + hiding |
| Proof System | PLONK+KZG | Succinct proofs |
| SRS | Aztec Powers of Tau | Trusted setup |

#### Transaction Flow

```
Shield (Public → Private):
1. User has 100 QORA publicly
2. Creates commitment = MiMC(secret, amount, blinding)
3. Proves knowledge of preimage (ZK proof)
4. Public balance decreases, commitment added to Merkle tree

Private Transfer:
1. Prove ownership of input commitment
2. Create nullifier = hash(secret, commitment)
3. Create new commitment for recipient
4. ZK proof: input_amount = output_amount (no inflation)

Unshield (Private → Public):
1. Prove ownership of commitment
2. Reveal nullifier (prevents double-spend)
3. Public balance increases
```

#### Stealth Addresses

```
Recipient Setup:
- Generate scan_key (for finding payments)
- Generate spend_key (for spending)
- Publish stealth_address = (scan_pubkey, spend_pubkey)

Sender:
1. Generate ephemeral_key
2. Compute shared_secret = ECDH(ephemeral_key, scan_pubkey)
3. Derive one-time address from shared_secret
4. Include view_tag = hash(shared_secret)[0] (1 byte)

Recipient Scanning:
1. For each TX, check view_tag (filters 99.6%)
2. If match, compute shared_secret
3. Derive address, check if spendable
```

---

## 7. Social Infrastructure

### Why Native vs dApp?

| Aspect | dApp Approach | Native Approach |
|--------|---------------|-----------------|
| **Key Management** | Separate from wallet | Derived from wallet |
| **Encryption** | App-specific | Protocol-level |
| **Interop** | None | All apps share keys |
| **Privacy** | App decides | Mandatory |
| **Payments** | Bridge needed | Seamless |

### Chat Architecture

```
┌─────────────────────────────────────────────────────────┐
│                    QORA CHAT SERVICE                     │
├─────────────────────────────────────────────────────────┤
│                                                          │
│  ┌──────────┐    ┌──────────┐    ┌──────────────────┐  │
│  │  Client  │───▶│   API    │───▶│  Kafka Topics    │  │
│  │ (WebSocket)   │  Server  │    │                  │  │
│  └──────────┘    └──────────┘    │ dm.{user1}_{user2}│  │
│                                   │ group.{groupId}   │  │
│                                   │ presence          │  │
│  ┌──────────┐    ┌──────────┐    │ typing            │  │
│  │ Blockchain│◀──│  Event   │◀───│ calls             │  │
│  │  Module  │    │ Handler  │    └──────────────────┘  │
│  └──────────┘    └──────────┘                          │
│                                                          │
└─────────────────────────────────────────────────────────┘
```

### Encryption Protocol

```
X3DH Key Agreement:
1. Alice fetches Bob's prekey bundle
   - Identity key (long-term)
   - Signed prekey (rotates monthly)
   - One-time prekey (single use)

2. Alice computes shared secrets:
   DH1 = ECDH(Alice_identity, Bob_signed_prekey)
   DH2 = ECDH(Alice_ephemeral, Bob_identity)
   DH3 = ECDH(Alice_ephemeral, Bob_signed_prekey)
   DH4 = ECDH(Alice_ephemeral, Bob_one_time_prekey)

3. Master secret = KDF(DH1 || DH2 || DH3 || DH4)

4. Double Ratchet for forward secrecy
   - New keys derived for each message
   - Compromise of current key doesn't reveal past messages
```

### Video/Voice Architecture

```
┌──────────────────────────────────────────────────────────┐
│                    LIVEKIT INTEGRATION                    │
├──────────────────────────────────────────────────────────┤
│                                                           │
│  ┌─────────┐         ┌─────────────┐         ┌─────────┐│
│  │  User A │◀───────▶│  LiveKit    │◀───────▶│  User B ││
│  │ (WebRTC)│         │   Server    │         │ (WebRTC)││
│  └─────────┘         └─────────────┘         └─────────┘│
│       │                     │                     │      │
│       ▼                     ▼                     ▼      │
│  ┌─────────────────────────────────────────────────────┐│
│  │                  QORA BLOCKCHAIN                    ││
│  │  - Call billing (per minute)                       ││
│  │  - Recording storage (IPFS CID)                    ││
│  │  - Participant tracking                            ││
│  └─────────────────────────────────────────────────────┘│
│                                                           │
└──────────────────────────────────────────────────────────┘
```

### AI Assistant System

```
┌──────────────────────────────────────────────────────────┐
│                    AI ASSISTANT FLOW                      │
├──────────────────────────────────────────────────────────┤
│                                                           │
│  1. User configures assistant profile:                    │
│     - Business name & description                         │
│     - Products/services list                              │
│     - FAQ with Q&A pairs                                  │
│     - Response guidelines                                 │
│     - Working hours                                       │
│                                                           │
│  2. Message arrives in chat                               │
│     ↓                                                     │
│  3. Assistant manager checks:                             │
│     - Is auto-reply enabled?                              │
│     - Within working hours?                               │
│     - Matches keyword filters?                            │
│     ↓                                                     │
│  4. Generate response via qora-ai:                        │
│     - Context: user profile + message history             │
│     - Model: QoraFast-1.0 (or configured)                │
│     - Billing: tokens charged on-chain                    │
│     ↓                                                     │
│  5. Send reply with delay (configurable)                  │
│                                                           │
└──────────────────────────────────────────────────────────┘
```

---

## 8. Market Opportunity

### Total Addressable Market

| Segment | Market Size | QORA's Position |
|---------|-------------|-----------------|
| **DeFi TVL** | $50B+ | Privacy-first DeFi |
| **Private Transactions** | $10B+ (pre-Tornado shutdown) | Only mandatory privacy L1 |
| **Encrypted Messaging** | 2B+ users | Crypto-native alternative |
| **AI Inference** | $100B+ by 2030 | Decentralized, verifiable |
| **L1 Market Cap** | $500B+ | Faster + more private |

### Why Now?

1. **Regulatory clarity emerging** - Privacy is legal, mixers aren't
2. **Tornado Cash proved demand** - $8B+ TVL before shutdown
3. **Solana proved speed matters** - $70B market cap
4. **Telegram proved social demand** - 900M users
5. **AI explosion** - Need for verifiable, decentralized inference

---

## 9. Competitive Analysis

### Speed Comparison

```
                    Block Time        Finality
                    ──────────        ────────
Ethereum            12 seconds        12-15 minutes
Polygon             2 seconds         30 minutes
Avalanche           2 seconds         2 seconds
Solana              400ms             400ms
QORA                50-100ms          INSTANT
                    ▲                 ▲
                    │                 │
                    └── 4-8x faster ──┘
```

### Privacy Comparison

| Chain | Privacy Type | Mandatory? | Smart Contracts? |
|-------|--------------|------------|------------------|
| Monero | Ring signatures | Yes | No |
| Zcash | zk-SNARKs | No (optional) | Limited |
| Secret Network | TEE (hardware) | Yes | Yes |
| Tornado Cash | Mixer | N/A (shut down) | Ethereum only |
| **QORA** | **PLONK+KZG** | **Yes** | **Full EVM** |

### Feature Comparison

| Feature | ETH | SOL | ATOM | SECRET | QORA |
|---------|-----|-----|------|--------|------|
| Fast Finality | ❌ | ✅ | ❌ | ❌ | ✅ |
| Privacy | ❌ | ❌ | ❌ | ✅ | ✅ |
| EVM | ✅ | ❌ | ❌ | ❌ | ✅ |
| Native Chat | ❌ | ❌ | ❌ | ❌ | ✅ |
| Native Video | ❌ | ❌ | ❌ | ❌ | ✅ |
| Native AI | ❌ | ❌ | ❌ | ❌ | ✅ |
| **Enterprise Auth** | ❌ | ❌ | ❌ | ❌ | ✅ |
| DEX/Orderbook | dApp | dApp | dApp | dApp | ✅ Native |

---

## 10. Revenue Model

### Transaction Fees

| Fee Type | Rate | Comparable |
|----------|------|------------|
| Base TX fee | 0.001 QORA | Ethereum gas |
| Privacy operations | 0.01 QORA | ZK proof verification |
| Smart contract calls | Variable | Based on computation |
| Auth operations | 0.001 QORA | Per login/session |

### Protocol Revenue Streams

| Stream | Model | Year 1 | Year 3 |
|--------|-------|--------|--------|
| TX Fees | 0.1% of volume | $1M | $50M |
| Privacy Fees | Per shield/unshield | $500K | $20M |
| AI Inference | Per token | $500K | $100M |
| Chat Backup | Per MB/month | $100K | $10M |
| DEX Trading | Maker/taker fees | $1M | $200M |
| Perpetuals | Funding + fees | $500K | $100M |
| **QoraAuth (B2B)** | **Per MAU + API calls** | **$2M** | **$150M** |
| **Total** | | **$5.6M** | **$630M** |

### QoraAuth: Enterprise Authentication (HIGH MARGIN B2B)

**What it is:** Passwordless blockchain authentication for companies - like Magic Link but native to QORA.

**How it works:**
```
1. Company registers → Gets API key
2. User clicks "Login with QORA" on company website
3. User receives email/push with 6-digit code
4. User confirms → Blockchain creates session
5. Company verifies session via API
```

**Key Features:**
| Feature | Description |
|---------|-------------|
| **Passwordless Login** | Email → blockchain wallet binding |
| **Multi-Wallet Security** | Main wallet + Auth wallet (2FA on-chain) |
| **Session Management** | Configurable expiry, revocation |
| **Zero Secrets Stored** | Pure cryptographic verification |
| **API Key Billing** | Pay-per-use or monthly plans |

**Competitive Landscape:**

| Competitor | Pricing | Weakness | QORA Advantage |
|------------|---------|----------|----------------|
| **Magic Link** | $0.05/MAU | Centralized, no crypto-native | Native blockchain identity |
| **Web3Auth** | $0.02/MAU | Complex setup, middleware | Single-chain, simple |
| **Privy** | $0.03/MAU | VC-dependent, can change terms | Decentralized, immutable |
| **Dynamic** | Custom | Enterprise only | Self-service + enterprise |
| **QORA Auth** | **$0.01/MAU** | - | **Cheapest + most features** |

**Revenue Projection:**

| Metric | Year 1 | Year 2 | Year 3 |
|--------|--------|--------|--------|
| Companies | 100 | 1,000 | 10,000 |
| Avg MAU/Company | 10,000 | 25,000 | 50,000 |
| Total MAUs | 1M | 25M | 500M |
| Revenue/MAU | $0.01 | $0.01 | $0.01 |
| API Call Revenue | $1M | $10M | $100M |
| **Total Auth Revenue** | **$2M** | **$35M** | **$150M** |

**Why This is a Big Opportunity:**
1. **Low Competition**: No blockchain-native auth at scale
2. **High Margins**: Pure software, minimal infrastructure
3. **Sticky Revenue**: Companies don't switch auth providers
4. **Network Effects**: More companies = more users = more value
5. **Upsell Path**: Auth → Chat → Payments → Full stack

### Token Economics

```
Total Supply: 1,000,000,000 QORA

Distribution:
- Team & Advisors: 15% (4-year vest, 1-year cliff)
- Investors: 20% (2-year vest)
- Ecosystem Fund: 25% (grants, partnerships)
- Community: 30% (airdrops, rewards)
- Treasury: 10% (protocol development)

Inflation: 5% year 1, decreasing 1% annually to 2% floor
```

---

## 11. Roadmap

### 2026 Q2: Public Testnet
- [ ] Launch incentivized testnet
- [ ] Bug bounty program
- [ ] Developer documentation
- [ ] SDK release

### 2026 Q4: Mainnet Launch
- [ ] Genesis block
- [ ] Initial validator set
- [ ] Bridge to Ethereum
- [ ] DEX launch

### 2021 Q1: Ecosystem Growth
- [ ] Grant program
- [ ] Hackathons
- [ ] Mobile wallet
- [ ] Chat app release

### 2027 Q2: Enterprise Features
- [ ] Company authentication
- [ ] Compliance tools
- [ ] Institutional custody
- [ ] Advanced AI models

---

## 12. Team

*[To be filled with team information]*

---

## 13. Contact

- **Website**: [Coming Soon]
- **GitHub**: github.com/qora-protocol
- **Twitter**: [Coming Soon]
- **Discord**: [Coming Soon]

---

## Appendix A: Security Audit Summary

### Issues Found and Fixed

| Severity | Count | Status |
|----------|-------|--------|
| CRITICAL | 8 | ✅ All Fixed |
| HIGH | 7 | ✅ All Fixed |
| MEDIUM | 12 | ✅ All Fixed |
| **Total** | **27** | **✅ Complete** |

### Key Fixes

1. **Goroutine Deadlock** - Fixed lock management in voting
2. **Race Conditions** - Added proper synchronization
3. **Overflow Protection** - Safe math for voting power
4. **Memory Limits** - Bounded queues and maps
5. **Timestamp Validation** - Future block rejection
6. **Privacy Leaks** - Removed debug statements

---

## Appendix B: Technical Specifications

### Consensus Parameters

| Parameter | Value |
|-----------|-------|
| Block Time Target | 50-100ms |
| Finality Threshold | 2/3 voting power |
| VDF Difficulty | 1024-bit quadratic residue |
| VDF Compute Time | ~14 seconds |
| VDF Verify Time | ~350ms |
| Checkpoint Interval | 500 levels |
| Max Ahead Gap | 500 levels |

### Privacy Parameters

| Parameter | Value |
|-----------|-------|
| Curve | BN254 (BabyJubJub) |
| Proof System | PLONK+KZG |
| SRS | Aztec Powers of Tau (2^20) |
| Merkle Depth | 32 levels |
| Nullifier Size | 32 bytes |
| View Tag Size | 1 byte |

### Network Parameters

| Parameter | Value |
|-----------|-------|
| Max Block Size | 4 MB |
| Max TX Size | 1 MB |
| P2P Protocol | Custom (libp2p-based) |
| RPC | Tendermint-compatible |
| gRPC | Cosmos SDK standard |

---

*Last updated: January 2026*
