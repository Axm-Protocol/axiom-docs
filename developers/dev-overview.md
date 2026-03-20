# Developer Overview

AXIOM Protocol is built on Solana using the Anchor framework. This section covers the tools, SDKs, and smart contracts available for building on AXIOM.

## Technology Stack

| Layer | Technology | Usage |
|-------|-----------|-------|
| **Blockchain** | Solana | Runtime, consensus, transaction processing |
| **Token** | SPL Token-2022 | AXM token with metadata extension |
| **Contracts** | Anchor (Rust) | Presale, vesting, staking, agent registry |
| **SDK** | TypeScript | Client library for dApp integration |
| **Liquidity** | Meteora DAMM v1 | Permanent LP with fee claims |

## Repositories

| Repository | Visibility | Description |
|-----------|------------|-------------|
| `axiom-docs` | Public | Documentation (this repo) |
| `axiom-whitepaper` | Public | Whitepaper PDF |
| `axiom-token-metadata` | Public | On-chain token metadata |
| `axiom-contracts` | Private | Smart contract source code |

## Getting Started

1. Install [Solana CLI](https://docs.solana.com/cli/install-solana-cli-tools) and [Anchor](https://www.anchor-lang.com/)
2. Install the AXIOM SDK: `npm install @axm-protocol/sdk`
3. Check the [SDK Guide](sdk-guide.md) for setup instructions
4. Browse the [Smart Contracts](smart-contracts.md) reference
