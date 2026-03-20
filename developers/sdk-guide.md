# SDK & Quick Start

Integrate AXIOM staking, governance, or RWA data into your dApp via the TypeScript SDK.

## Installation

```bash
npm install @axm-protocol/sdk @solana/web3.js
```

## Quick Start

```typescript
import { AXMClient } from '@axm-protocol/sdk';
import { Connection, PublicKey } from '@solana/web3.js';

const connection = new Connection('https://api.mainnet-beta.solana.com');
const client = new AXMClient(connection);

// Get staking info
const stakingInfo = await client.getStakingVault();
console.log('Total Staked:', stakingInfo.totalStaked);
console.log('APY:', stakingInfo.currentAPY);

// Get token info
const tokenInfo = await client.getTokenInfo();
console.log('Supply:', tokenInfo.totalSupply);
```

## Available Methods

| Method | Description |
|--------|-------------|
| `getTokenInfo()` | Get AXM token metadata and supply info |
| `getStakingVault()` | Get staking vault state and statistics |
| `getUserStake(wallet)` | Get a user's staking position and rewards |
| `getPresaleState()` | Get presale progress and parameters |
| `getGovernanceProposals()` | List active governance proposals |
| `getAgentRegistry()` | Browse registered AI agents |

## Authentication

No API key required for read operations. Write operations (staking, voting, etc.) require a connected Solana wallet.
