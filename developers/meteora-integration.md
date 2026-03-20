# Meteora Integration

AXIOM uses Meteora DAMM v1 as the primary liquidity protocol. This page explains the integration and why Meteora was chosen over alternatives.

## Why Meteora over Raydium?

| Feature | Meteora DAMM v1 | Raydium |
|---------|-----------------|---------|
| LP Lock | Lock LP + earn fees | Burn LP = lose fees forever |
| Fee Structure | 5% protocol fee | Higher protocol fees |
| Liquidity | Dynamic concentrated | Standard AMM |
| Solana Native | Yes | Yes |
| LP Token Control | Lockable with fee claims | Must burn to prove commitment |

## Key Benefits

- **Locked LP earns fees forever** — unlike Raydium where burning LP loses all fee revenue
- **Concentrated liquidity** — better capital efficiency and tighter spreads for traders
- **5% protocol fee** — only 5% goes to Meteora, 95% to the AXIOM LP position
- **Native Solana** — fast, cheap swaps with no bridging required

## Integration Details

After presale finalization, the `finalize_presale()` function:

1. Creates an AXM/SOL pool on Meteora DAMM v1
2. Deposits collected SOL and allocated AXM tokens
3. Locks LP tokens permanently (preserving fee claim rights)
4. Enables trading on the AXM/SOL pair

## Fee Collection

Locked LP positions on Meteora continue to earn trading fees. These fees are collected by the protocol treasury and distributed according to the revenue distribution model:

- 60% to stakers
- 25% to protocol treasury
- 15% to developer fund
