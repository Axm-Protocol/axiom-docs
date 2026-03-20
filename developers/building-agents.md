# Building AI Agents

Create custom AI agents that run on the AXIOM Protocol and earn revenue from the marketplace.

## Agent Architecture

AXIOM AI agents are autonomous programs that:
- Monitor on-chain and off-chain data sources
- Execute trading, rebalancing, and risk management strategies
- Operate within authority bounds set by the Agent Registry
- Report performance metrics on-chain

## Agent Template

```typescript
import { AXMAgent, AgentConfig } from '@axm-protocol/agent-sdk';

const config: AgentConfig = {
  name: 'My Custom Agent',
  strategy: 'yield-optimizer',
  riskLevel: 'medium',
  rebalanceInterval: 3600, // seconds
  maxSlippage: 0.5, // percent
  assets: ['SOL', 'USDC', 'mSOL'],
};

const agent = new AXMAgent(config);

agent.onTick(async (state) => {
  // Your strategy logic here
  const positions = await state.getPositions();
  const prices = await state.getPrices();
  
  // Rebalance if needed
  if (shouldRebalance(positions, prices)) {
    await state.rebalance(newAllocations);
  }
});

agent.start();
```

## Registration

1. Build and test your agent locally
2. Submit to the Agent Registry with required $AXM deposit (10,000 AXM)
3. Pass automated security review
4. Agent goes live on the marketplace

## Revenue Model

- Agents earn a share of management fees from users who deploy them
- Performance fees are split between the agent creator and the protocol
- Top-performing agents receive additional $AXM rewards from the ecosystem fund
