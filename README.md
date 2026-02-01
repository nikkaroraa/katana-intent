# Katana Intent ⚔️

> Natural language interface to DeFi on Katana. Make DeFi as easy as talking to a friend.

<p align="center">
  <img src="https://img.shields.io/badge/Next.js-14-black" />
  <img src="https://img.shields.io/badge/TypeScript-5.4-blue" />
  <img src="https://img.shields.io/badge/Tailwind-3.4-38bdf8" />
  <img src="https://img.shields.io/badge/Powered%20by-Claude-orange" />
</p>

## Features

- 🧠 **Natural Language DeFi** - Just type what you want, like "deposit 100 USDC into best yield"
- 💰 **Balance Queries** - "Show my balances" → instant wallet overview
- 📈 **Yield Finder** - "Best yield for USDC?" → ranked opportunities
- 🔄 **Swaps** - "Swap half my ETH to USDC" → preview and execute
- ⚠️ **Risk Monitoring** - "Am I safe?" → health factor checks

## Quick Start

```bash
# Install dependencies
npm install

# Set up environment
cp apps/web/.env.example apps/web/.env.local
# Add your ANTHROPIC_API_KEY and NEXT_PUBLIC_WALLETCONNECT_PROJECT_ID

# Run development server
npm run web
```

## Project Structure

```
katana-intent/
├── apps/
│   ├── web/                 # Next.js frontend
│   │   ├── app/             # App router pages
│   │   ├── components/      # React components
│   │   └── lib/             # Utilities and stores
│   └── bot/                 # Telegram bot (Week 3)
├── packages/
│   ├── intent-engine/       # NL → Intent parsing
│   ├── protocol-adapters/   # DeFi protocol integrations
│   └── shared/              # Types and utilities
└── turbo.json               # Turborepo config
```

## Commands

```bash
npm run dev      # Run all apps in development
npm run web      # Run just the web app
npm run bot      # Run just the Telegram bot
npm run build    # Build all packages
npm run lint     # Lint all packages
```

## Tech Stack

- **Frontend**: Next.js 14, React 18, Tailwind CSS, Framer Motion
- **Wallet**: RainbowKit, wagmi, viem
- **AI**: Claude API for intent parsing
- **State**: Zustand with persistence
- **Monorepo**: Turborepo with npm workspaces

## Intent Types

| Type | Example | Description |
|------|---------|-------------|
| `query` | "Show my balances" | Information requests |
| `deposit` | "Deposit 100 USDC" | Add to yield protocols |
| `withdraw` | "Withdraw all from Yearn" | Remove from protocols |
| `swap` | "Swap 0.5 ETH to USDC" | Token exchanges |
| `stake` | "Stake my ETH" | Staking operations |
| `borrow` | "Borrow USDC against ETH" | Lending operations |

## Roadmap

- [x] **Week 1**: Monorepo, intent parsing, chat UI, wallet connect, balance query
- [ ] **Week 2**: Yield finder, deposit/withdraw flows, swap integration
- [ ] **Week 3**: Telegram bot, risk analyzer, polish
- [ ] **Week 4**: User accounts, alerts, premium features

## Environment Variables

```env
# apps/web/.env.local
ANTHROPIC_API_KEY=sk-ant-...
NEXT_PUBLIC_WALLETCONNECT_PROJECT_ID=...
KATANA_RPC_URL=https://rpc.katana.network
```

## Contributing

This is a build-in-public project. Follow along on Twitter [@nikkaroraa](https://twitter.com/nikkaroraa).

## License

MIT
