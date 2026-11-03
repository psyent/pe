# PropEdge — The Open-Source Player Prop Research Platform

> **Smarter bets. Better tools. No gatekeepers.**

A modern, web-first alternative to props.cash — built for serious bettors who want transparency, extensibility, and power-user features without subscription lock-in.

## 🎯 Why PropEdge?

| Feature | props.cash | PropEdge |
|---------|-----------|----------|
| **Platform** | iOS only | Web + PWA + API |
| **Free Tier** | ❌ 7-day trial only | ✅ Generous forever-free |
| **Pricing** | $19.99/mo flat | Usage-based, transparent |
| **Sportsbooks** | ~10 | 25+ (extensible) |
| **EV/Kelly Calculator** | Basic | Advanced + Portfolio |
| **Arbitrage Detection** | ❌ | ✅ Built-in |
| **API Access** | ❌ | ✅ First-class |
| **Open Source** | ❌ | ✅ MIT License |
| **Community** | Closed | Discord + GitHub |
| **Data Export** | ❌ | ✅ CSV/JSON/Parquet |

## ✨ Features

### 🔍 Prop Research Engine
- **1,500+ props** across NBA, NFL, NHL, MLB, WNBA, CFB, CBB, MMA, Soccer
- **Real-time odds** from 25+ sportsbooks (DraftKings, FanDuel, BetMGM, Caesars, PrizePicks, Underdog, etc.)
- **Advanced filters**: stat type, line range, EV threshold, correlation, matchup grade
- **Player correlations** & **matchup grades** with opponent defensive ratings
- **Shot charts**, H2H logs, injury reports, weather (NFL/MLB), rest days

### 📊 Analytics Suite
- **Expected Value (EV) Calculator** with customizable win probability models
- **Kelly Criterion** bet sizing (full, half, quarter Kelly)
- **Portfolio Tracker** — track ROI, CLV, win rate by sport/prop type/book
- **Arbitrage & Middle Detector** — cross-book opportunities in real-time
- **Steam Move Alerts** — line movement > 5% in 5 min
- **Historical Backtesting** — test strategies against 3+ seasons of data

### 🎨 Modern UX
- **Lightning-fast** React 19 + TanStack Query + WebSocket streams
- **Dark/light mode**, fully responsive (mobile → 4K)
- **Keyboard-first** navigation (Vim-style bindings)
- **Customizable dashboards** — drag/drop widgets, save layouts
- **PWA** — installable, offline-capable, push notifications

### 🔌 Extensibility
- **Plugin System** — custom data sources, alert rules, viz widgets
- **REST + GraphQL API** — build your own tools
- **Webhooks** — push alerts to Discord, Slack, Telegram, email
- **Python/JS SDKs** — `pip install propedge-sdk`

## 🚀 Quick Start

```bash
# Clone & install
git clone https://github.com/yourusername/propedge.git
cd properedge
pnpm install

# Start dev server (Vite + HMR)
pnpm dev

# Build for production
pnpm build
```

## 🏗️ Architecture

```
propedge/
├── apps/
│   ├── web/          # React 19 + Vite + TanStack Router
│   ├── api/          # Hono + Cloudflare Workers (edge)
│   └── worker/       # BullMQ queues for odds ingestion
├── packages/
│   ├── ui/           # Shared component library (Radix + Tailwind)
│   ├── core/         # Types, utilities, EV/Kelly math
│   ├── sdk/          # TypeScript/Python SDKs
│   └── plugins/      # Plugin runtime & official plugins
├── turbo.json        # Turborepo config
└── pnpm-workspace.yaml
```

## 📈 Data Sources (Pluggable)

| Source | Type | Latency | Cost |
|--------|------|---------|------|
| The Odds API | REST | ~500ms | Free tier: 500 req/day |
| OddsJam | WebSocket | ~50ms | $149/mo |
| Pinnacle | REST | ~200ms | Free (affiliate) |
| SportRadar | WebSocket | ~30ms | Enterprise |
| **Custom Plugin** | Any | You decide | You decide |

## 💰 Pricing Philosophy

> **Pay for what you use. Own your data. No surprises.**

| Plan | Props/Day | API Calls | Webhooks | History | Support |
|------|-----------|-----------|----------|---------|---------|
| **Free** | 500 | 1,000 | 5 | 30 days | Community |
| **Pro** | 10,000 | 100,000 | 50 | 2 years | Email |
| **Team** | 100,000 | 1M | 500 | Unlimited | Priority + Slack |
| **Enterprise** | ∞ | ∞ | ∞ | ∞ | Dedicated |

*Self-hosted? **100% free forever.** Pay only for managed hosting if you want it.*

## 🤝 Contributing

We welcome PRs! See [CONTRIBUTING.md](./CONTRIBUTING.md) for:
- Code style (Biome, TypeScript strict)
- Testing (Vitest + Playwright)
- Plugin development guide
- Data provider integration checklist

## 📄 License

MIT — use it, fork it, build on it. See [LICENSE](./LICENSE).

---

**Built with ❤️ by bettors, for bettors.**  
*Not financial advice. Bet responsibly. 18+/21+ depending on jurisdiction.*