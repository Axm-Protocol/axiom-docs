# Governance

AXIOM Protocol is governed by $AXM token holders through on-chain voting. Governance power is weighted by both token holdings and staking multiplier.

## Governance Power

Your governance voting weight is calculated as:

```
Voting Power = Staked AXM × Lock Multiplier
```

For example, 10,000 AXM staked for 1 year (3.0x multiplier) gives 30,000 governance votes.

## Proposal Types

| Type | Description | Threshold |
|------|-------------|-----------|
| **Protocol Upgrade** | Smart contract upgrades and new feature deployment | 10% quorum |
| **Treasury Spend** | Allocate treasury funds to grants, development, or partnerships | 15% quorum |
| **Agent Whitelist** | Approve new AI agents for the marketplace | 5% quorum |
| **Parameter Change** | Adjust fees, staking rates, risk parameters | 10% quorum |
| **Emergency** | Critical security responses and emergency actions | 5% quorum, expedited |

## Proposal Lifecycle

1. **Draft** — Community discussion on Discord/forum
2. **Formal Proposal** — Submitted on-chain with required AXM stake
3. **Voting Period** — 7-day voting window
4. **Timelock** — 48-hour timelock before execution
5. **Execution** — Automatic on-chain execution if passed

## AI-Assisted Governance

AXIOM's AI agents can analyze governance proposals and provide impact assessments, including:
- Economic simulation of proposed parameter changes
- Risk analysis of treasury spending proposals
- Historical comparison with similar protocol decisions
