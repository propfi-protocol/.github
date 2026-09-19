<div align="center">

# PropFi

**Decentralized Real Estate Finance on Stellar · Built with Soroban**

Tokenize property. Fractionalize ownership. Stream rent. Borrow against equity.
Go cross-border. Stay compliant — without putting PII on-chain.

[Documentation](#) · [Protocol Overview](#) · [Contributing Guide](#)

</div>

---

## What is PropFi?

PropFi is a full-stack, production-grade decentralized real estate protocol on the Stellar blockchain. Anyone, anywhere, can:

- **Tokenize** a property
- **Fractionalize** it into tradeable ownership shares
- **Stream** rental income to fraction holders
- **Borrow** on-chain against property equity
- **Transact cross-border**, gated by zero-knowledge KYC attestations — no PII on-chain
- **Govern** the protocol on-chain, by fraction holders

No banks. No brokers. No paper. Just code.

## Repositories

PropFi is organized as a set of focused repos under this org:

| Repo | Description |
|---|---|
| [`contracts`](https://github.com/propfi-protocol/contracts) | 8 Soroban smart contracts — see below |
| [`sdk`](https://github.com/propfi-protocol/sdk) | TypeScript client SDK for interacting with the protocol |
| [`indexer`](https://github.com/propfi-protocol/indexer) | Horizon event indexer for fast queries over on-chain activity |
| [`frontend`](https://github.com/propfi-protocol/frontend) | Next.js dApp |
| [`scripts`](https://github.com/propfi-protocol/scripts) | Deployment and environment setup scripts |

### Contracts

| Contract | Responsibility |
|---|---|
| `PropertyRegistry` | Registers properties and their metadata on-chain |
| `FractionVault` | Mints and manages fractional ownership tokens per property |
| `RentDistributor` | Streams rental income to fraction holders |
| `MortgagePool` | On-chain borrowing against property equity |
| `PaymentBridge` | Handles cross-border payment settlement |
| `OracleAdapter` | Interface to external price/valuation data feeds |
| `ComplianceRegistry` | Tracks zero-knowledge KYC attestations, gates protocol access |
| `Governance` | On-chain voting and protocol parameter changes by fraction holders |

## Architecture at a Glance

```
Property Owner ──► PropertyRegistry ──► FractionVault ──► Fraction Holders
                                              │                   │
                                              ▼                   ▼
                                      MortgagePool          RentDistributor
                                              │                   │
                                              ▼                   ▼
                                      PaymentBridge ◄──── OracleAdapter
                                              │
                                              ▼
                                   ComplianceRegistry (gates all of the above)
                                              │
                                              ▼
                                         Governance
```

All contract interaction is indexed by `indexer` and surfaced to users through `frontend`, or accessed programmatically via `sdk`.

## Security

Found a vulnerability? Please **do not open a public issue** — email `security@propfi.xyz` instead.

## Compliance by Design

PropFi gates protocol access through the `ComplianceRegistry` contract, which checks zero-knowledge KYC attestations rather than storing personally identifiable information on-chain. This lets the protocol meet compliance requirements without compromising user privacy or creating an on-chain data liability.

---

<div align="center">

Built on [Stellar](https://stellar.org/) · Powered by [Soroban](https://soroban.stellar.org/)

</div>
