import { FuelAgent } from 'fuel-agent-kit';

const agent = new FuelAgent();

// Call different functions
await agent.transfer({
  to: '0x8F8afB12402C9a4bD9678Bec363E51360142f8443FB171655eEd55dB298828D1',
  amount: 0.1,
  symbol: 'USDC',
});

// or, execute commands in natural language
await agent.execute(
  'Send 0.1 USDC to 0x8F8afB12402C9a4bD9678Bec363E51360142f8443FB171655eEd55dB298828D1',
);

// Swap Assets
await agent.execute('Swap 5 USDC for ETH');

// Add Liqudity
await agent.execute(
  'Add liquidity into USDC/USDT pool for 0.1 USDC with 5% slippage',
);

// Lend Assets
await agent.execute('Supply 10 USDT as Collateral');

// Borrow Assets
await agent.execute('Borrow 11 USDC');
