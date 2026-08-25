# Freysa Security 🔒

**On-chain security intelligence layer for autonomous AI agents.**

27 x402 pay-per-call endpoints on Base mainnet. No API keys, no signup, no subscription — pay per request in USDC.

```
Agent → HTTP 402 → sign EIP-3009 → verify → execute → settle → result
```

## 🚀 Quick Start

```bash
# Any agent can call us in 3 steps:
# 1. Make a request → get 402 Payment Required
curl -X POST https://economic-agent-369.freysa.dev/api/honeypot-check \
  -H "Content-Type: application/json" \
  -d '{"token_address":"0x..."}'

# 2. Sign the payment with your wallet (EIP-3009 TransferWithAuthorization)
# 3. Retry with PAYMENT-SIGNATURE header
curl -X POST https://economic-agent-369.freysa.dev/api/honeypot-check \
  -H "Content-Type: application/json" \
  -H "PAYMENT-SIGNATURE: <base64-payload>" \
  -d '{"token_address":"0x..."}'
```

## 🛡️ Capabilities

### Security Analysis ($0.25)
| Endpoint | Description |
|----------|-------------|
| `/api/honeypot-check` | Token honeypot & rug-pull detection via bytecode analysis |
| `/api/address-risk` | Wallet address risk scoring (0-100) |
| `/api/approval-risk` | Scan wallet for dangerous token approvals |
| `/api/wallet-forensics` | Deep wallet forensic analysis |
| `/api/token-analyze` | Token contract analysis (bytecode, ownership, liquidity) |
| `/api/code-review` | Solidity smart contract security review |

### Pre-Trade Safety ($1.00-$2.50)
| Endpoint | Description |
|----------|-------------|
| `/api/pre-trade-check` | Full pre-trade: token + contract + wallet in one call |
| `/api/agent-preflight` | **Flagship**: PROCEED/CAUTION/ABORT verdict |

### CAPTCHA Solving ($0.01)
| Endpoint | Description |
|----------|-------------|
| `/api/captcha-solve` | Solve CAPTCHAs via CapSolver AI backend (99% accuracy) |

### Data Feeds (Free - $0.001)
| Endpoint | Price | Description |
|----------|-------|-------------|
| `/api/eth-gas` | **FREE** | Current gas prices on Base |
| `/api/trending` | $0.001 | Trending tokens from DexScreener |
| `/api/base-stats` | $0.001 | Base L2 network statistics |
| `/api/market-overview` | $0.001 | Aggregated crypto market data |
| `/api/crypto-price` | $0.001 | Real-time price for any ticker |
| `/api/fetch` | $0.001 | Web scraping: fetch any URL as markdown |

### AI Intelligence ($0.25-$1.00)
| Endpoint | Price | Description |
|----------|-------|-------------|
| `/api/reason` | $1.00 | Deep reasoning & decision analysis |
| `/api/research` | $1.00 | Full research report with citations |
| `/api/synthesize` | $0.001 | AI data synthesis |

## 💰 Pricing

| Tier | Price | Examples |
|------|-------|----------|
| Free | $0.00 | Gas prices |
| Data | $0.001 | Trending, prices, stats, web scraping |
| Utility | $0.01 | CAPTCHA solving |
| Security | $0.25 | Honeypot, address risk, forensics, code review |
| Premium | $1.00-$2.50 | Pre-trade check, agent preflight |

## ⛓️ Network & Settlement

- **Chain:** Base (eip155:8453)
- **Asset:** USDC (`0x833589fCD6eDb6E08f4c7C32D4f71b54bdA02913`)
- **Protocol:** x402 v2
- **Facilitator:** Coinbase CDP
- **PayTo:** `0x6D8abB282C35D45E3C773aD8a67b288Ac35fd1e9`

## 🔍 Discovery

- **x402 Manifest:** `https://economic-agent-369.freysa.dev/.well-known/x402`
- **Agent Card:** `https://economic-agent-369.freysa.dev/.well-known/agent-card.json`
- **OpenAPI:** `https://economic-agent-369.freysa.dev/openapi.json`
- **API Base:** `https://economic-agent-369.freysa.dev`

## 📦 OpenClaw Skill

```bash
clawhub install freysa-security
```

## 🏪 Listings

- [x402scan](https://www.x402scan.com) — 26/26 endpoints registered
- [agent-tools.cloud](https://agent-tools.cloud/api/v1/services/economic-agent-369-freysa-dev-sub342)
- [claw402](https://github.com/NoFxAiOS/claw402-open/pull/10) — PR #10 (pending merge)
- [awesome-x402](https://github.com/xpaysh/awesome-x402/pull/1321) — PR #1321 (pending merge)

## 🧪 Example Workflow

### Trading Agent Pre-Flight

```
1. Agent finds new token on DexScreener
2. → Calls honeypot-check ($0.25) → "SAFE"
3. → Calls address-risk on deployer ($0.25) → "LOW RISK"
4. → Calls pre-trade-check ($1.00) → "GO"
5. → Executes trade
Total: $1.50 for $500+ risk protection
```

## 📬 Contact

- Email: admin@economic-agent-369.freysa.dev

## 🔐 Security

This API is a security tool. Report vulnerabilities to admin@economic-agent-369.freysa.dev.