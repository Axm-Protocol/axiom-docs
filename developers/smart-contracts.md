# Smart Contracts

All AXIOM Protocol smart contracts are built with the Anchor framework on Solana and audited by OtterSec.

## Contract Overview

| Contract | File | Status | Description |
|----------|------|--------|-------------|
| AXM Token | `axm_token.rs` | Audited | SPL token with mint authority, metadata, and transfer hooks |
| Presale Vault | `presale_vault.rs` | Audited | Time-locked presale with hard/soft cap, whitelist, and auto-refund |
| Staking Vault | `staking_vault.rs` | Audited | Flexible staking with lock multipliers and revenue sharing |
| Agent Registry | `agent_registry.rs` | Audited | On-chain registry for autonomous AI agents with performance tracking |
| Governance | `governance.rs` | In Review | Token-weighted voting with AI proposal analysis and delegation |
| Treasury | `treasury.rs` | In Review | Protocol treasury with timelock, multi-sig, and spending limits |

## Presale Contract

```
contribute(amount: u64)
```
Contribute SOL to the presale. Amount must be between 0.1 and 10 SOL. Wallet must not exceed the per-wallet contribution limit.

```
claim_tokens()
```
Claim your AXM tokens after a successful presale (soft cap reached and Meteora pool created).

```
claim_refund()
```
Claim a full SOL refund if the presale fails to reach the soft cap.

```
finalize_presale()  // Admin
```
Finalize the presale and trigger migration to Meteora DAMM v1 pool.

```
emergency_refund_enable()  // Admin
```
Enable emergency refund mode. All contributors can claim full SOL refunds.

## Staking Vault

```
stake(amount: u64, lock_period: u64)
```
Stake AXM tokens in the staking vault. Rewards begin accruing immediately.

```
unstake()
```
Initiate unstaking. Begins the 7-day cooldown period.

```
claim_rewards()
```
Claim accumulated staking rewards.

## Source Code

Smart contract source code is available in the private [axiom-contracts](https://github.com/Axm-Protocol/axiom-contracts) repository. Access is granted to auditors and approved contributors.
