# PropFi

**Decentralized Real Estate Finance on Stellar · Built with Soroban**

Tokenize property. Fractionalize ownership. Stream rent. Borrow against equity. Go cross-border. Stay compliant — without putting PII on-chain.

PropFi is a full-stack, production-grade decentralized real estate protocol on the Stellar blockchain. Anyone, anywhere, can tokenize a property, split it into tradeable fractions, stream rental income to investors, and take out on-chain mortgages against equity — all gated by zero-knowledge KYC attestations and governed on-chain by fraction holders.

**No banks. No brokers. No paper. Just code.**

---

## What's here

PropFi is a single monorepo (`PropFi`), organized as:

- **`contracts/`** — 8 Soroban smart contracts: PropertyRegistry, FractionVault, RentDistributor, MortgagePool, PaymentBridge, OracleAdapter, ComplianceRegistry, Governance
- **`sdk/`** — TypeScript client SDK for interacting with the protocol
- **`indexer/`** — Horizon event indexer
- **`frontend/`** — Next.js dApp
- **`scripts/`** — deployment and setup scripts

## Quick links

- [Documentation](#)
- [Protocol overview](#)
- [Contributing guide](#)

## Security

PropFi contracts have not yet undergone a formal security audit. Do not use on mainnet with real funds until an audit is complete. To report a vulnerability, email `security@propfi.xyz` — please don't open a public issue.

---

Built on [Stellar](https://stellar.org) · Powered by [Soroban](https://soroban.stellar.org)
