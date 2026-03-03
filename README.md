# Edufrem Escrow Protocol

> **A blockchain-based escrow and payment infrastructure designed for education financing in emerging markets.**

---

## Overview

The **Edufrem Escrow Protocol** is the technical backbone of Edufrem's mission to enable transparent, secure, and accessible education financing across francophone Africa and beyond. This protocol addresses two critical challenges:

1. **Capital flight** — preventing educational funds from being diverted or misappropriated.
2. **Financial exclusion** — enabling learners and institutions without traditional banking access to participate in digital finance.

---

## Architecture

### Layer 2 Scaling

The protocol is built on a **Layer 2 (L2) network** on top of Ethereum (EVM-compatible), chosen for:

- **Low transaction fees** — critical for micro-payments in low-income markets.
- **High throughput** — enabling thousands of payment events per day.
- **EVM compatibility** — leveraging the existing Solidity smart contract ecosystem.

Candidate L2 networks under evaluation: **Polygon zkEVM**, **Optimism**, **Base**.

---

### Smart Contracts

| Contract | Role |
|---|---|
| `EscrowVault.sol` | Holds tuition funds until predefined release conditions are met |
| `MilestoneOracle.sol` | Verifies academic milestones via trusted oracles |
| `FundReleaseController.sol` | Triggers fund release to verified institutions |
| `GovernanceModule.sol` | Stakeholder voting on protocol parameters |

**Key principles:** Non-custodial · Transparent · Upgradable (OpenZeppelin Proxy).

---

### Stablecoins

- **USDC (Circle)** — primary settlement currency.
- **EURC** — for EUR-denominated grants.
- **cUSD (Celo)** — for mobile-first markets in West Africa.

Circle CCTP integration planned for cross-chain transfers.

---

### Anti-Capital-Flight Mechanisms

- **Destination whitelisting**: funds only reach KYC-verified institutions.
- **Time-locked disbursements**: tranches aligned with academic milestones.
- **On-chain audit trail**: immutable reporting for donors, regulators, UNICEF.
- **Refund logic**: unvalidated milestones trigger automatic fund repatriation.

---

## Target Use Cases

- Tuition escrow for scholarship recipients in Côte d'Ivoire, Senegal, Cameroon, Mali.
- Employer-sponsored learning with proof-of-completion triggers.
- NGO and donor fund management with real-time compliance reporting.
- Micro-grants for vocational training in underserved communities.

---

## Roadmap

| Phase | Status | Description |
|---|---|---|
| Phase 1 | ✅ Completed | Protocol architecture & whitepaper |
| Phase 2 | 🔄 In Progress | Smart contract development (Solidity, Hardhat) |
| Phase 3 | 🔜 Planned | Testnet deployment & security audit |
| Phase 4 | 🔜 Planned | Mainnet launch with pilot institution in Abidjan |
| Phase 5 | 🔜 Planned | Multi-country expansion & CBDC integration |

---

## Tech Stack

- **Smart Contracts**: Solidity ^0.8.20 + OpenZeppelin
- **Framework**: Hardhat
- **Frontend**: React + Wagmi + RainbowKit
- **Oracles**: Chainlink
- **Storage**: IPFS (academic credentials)
- **Treasury**: Safe (Gnosis) multisig

---

## Security

- Third-party audit before mainnet.
- Emergency pause (OpenZeppelin Pausable).
- Multi-sig governance via Safe.

---

## About Edufrem

Edufrem is an edtech/fintech startup building transparent, inclusive education financing infrastructure for francophone Africa.

🌍 [edufrem.com](https://edufrem.com) · 📧 [contact@edufrem.com](mailto:contact@edufrem.com)

---

## License

MIT License — see [LICENSE](LICENSE) for details.

---

*This repository represents the architectural foundation. Code implementation is actively in development.*
