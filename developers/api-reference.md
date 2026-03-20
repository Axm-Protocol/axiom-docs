# API Reference

Technical reference for AXIOM Protocol on-chain programs and SDK methods.

## On-Chain Program IDs

> Program IDs will be published at mainnet launch.

## RPC Endpoints

```
Mainnet: https://api.mainnet-beta.solana.com
Devnet:  https://api.devnet.solana.com
```

## SDK Methods

### Token

| Method | Returns | Description |
|--------|---------|-------------|
| `getTokenInfo()` | `TokenInfo` | Token metadata, supply, and mint info |
| `getTokenBalance(wallet)` | `number` | AXM balance for a wallet |
| `getTokenHolders()` | `HolderInfo[]` | Top token holders |

### Staking

| Method | Returns | Description |
|--------|---------|-------------|
| `getStakingVault()` | `VaultState` | Total staked, APY, reward pool balance |
| `getUserStake(wallet)` | `StakePosition` | User's stake amount, lock period, rewards |
| `stake(amount, lockPeriod)` | `Transaction` | Create a staking transaction |
| `unstake()` | `Transaction` | Initiate unstaking (7-day cooldown) |
| `claimRewards()` | `Transaction` | Claim accumulated rewards |

### Governance

| Method | Returns | Description |
|--------|---------|-------------|
| `getProposals(status?)` | `Proposal[]` | List governance proposals |
| `getProposal(id)` | `Proposal` | Get proposal details and vote counts |
| `vote(proposalId, support)` | `Transaction` | Cast a governance vote |

### Agents

| Method | Returns | Description |
|--------|---------|-------------|
| `getAgentRegistry()` | `Agent[]` | List all registered AI agents |
| `getAgentPerformance(id)` | `Performance` | Agent performance history and metrics |
| `deployAgent(config)` | `Transaction` | Deploy a new agent (requires 10,000 AXM) |
