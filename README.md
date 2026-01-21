# OFC Trading Platform

A professional-grade cryptocurrency trading analytics platform providing real-time market insights, AI-powered analysis, and automated trading tools for futures markets.

**Live Demo:** [https://ofc-trading.xyz](https://ofc-trading.xyz)

---

## Tech Stack

### Frontend
- **Next.js 14** - React framework with SSR/SSG
- **TypeScript** - Type-safe development
- **Tailwind CSS** - Utility-first styling
- **Framer Motion** - Smooth animations
- **Recharts & Chart.js** - Data visualization
- **Lightweight Charts** - TradingView-style charts

### Backend
- **Next.js API Routes** - Serverless functions
- **PostgreSQL** - Primary database
- **Prisma ORM** - Database management
- **Redis** - Real-time caching & pub/sub
- **BullMQ** - Background job processing

### Infrastructure
- **AWS S3** - Chart image storage
- **Vercel** - Deployment & hosting
- **NextAuth.js** - Authentication
- **Stripe** - Subscription management

### Data & Analysis
- **Python/Flask** - Market data processing
- **WebSocket** - Real-time data streams
- **Bybit API** - Exchange integration

---

## Features

### Real-Time Trading Dashboard
- Live portfolio tracking with P&L visualization
- Active positions monitoring across multiple accounts
- Trade execution history with detailed metrics
- Equity curve analysis and performance statistics

### Market Analysis Tools
- **OFC Indicators** - Proprietary order flow correlation indicators
- **Market Scanner** - Cross-asset screening with customizable filters
- **Regime Detection** - Automated market condition classification
- **Consolidation & Breakout Alerts** - Real-time pattern recognition

### AI-Powered Features
- **AI Strategy Selector** - Machine learning-based strategy recommendations
- **Market Reports** - Automated daily/weekly analysis
- **Trading Signals** - Data-driven entry/exit suggestions
- **AI Agent Terminal** - Interactive market analysis assistant

### Copy Trading
- Follow professional trader accounts
- Automated position mirroring
- Risk-adjusted position sizing
- Performance tracking and analytics

### Portfolio Management
- Multi-account support (Bybit integration)
- Historical performance analytics
- Calendar view with daily P&L breakdown
- Symbol-level performance analysis

### Account & Subscription
- Tiered subscription plans
- Two-factor authentication (2FA)
- Email alert preferences
- Admin dashboard for user management

---

## Screenshots

### Trading Dashboard
![Trading Dashboard](screenshots/dashboard.png)
*Real-time portfolio overview with P&L charts and active positions*

### Market Scanner
![Market Scanner](screenshots/scanner.png)
*Cross-asset screening with OFC indicators*

### AI Strategy Selector
![AI Strategy](screenshots/ai-strategy.png)
*Machine learning-powered strategy recommendations*

### Charts & Indicators
![Charts](screenshots/charts.png)
*Interactive charts with proprietary order flow indicators*

### Copy Trading
![Copy Trading](screenshots/copy-trading.png)
*Automated position mirroring interface*

---

## Architecture Overview

```
                    +------------------+
                    |    Vercel CDN    |
                    +--------+---------+
                             |
                    +--------v---------+
                    |   Next.js App    |
                    |  (SSR + API)     |
                    +--------+---------+
                             |
          +------------------+------------------+
          |                  |                  |
+---------v------+  +--------v-------+  +------v--------+
|   PostgreSQL   |  |     Redis      |  |    AWS S3     |
|  (Trade Data)  |  |  (Cache/PubSub)|  | (Chart Images)|
+----------------+  +----------------+  +---------------+
          |                  |
          |         +--------v--------+
          |         |     BullMQ      |
          |         | (Job Processing)|
          |         +--------+--------+
          |                  |
+---------v------------------v---------+
|       Data Processing Pipeline       |
|   (Python/Flask WebSocket Workers)   |
+--------------------------------------+
                    |
          +---------v---------+
          |  Exchange APIs    |
          |  (Bybit, Binance) |
          +-------------------+
```

### Key Components

- **Web Application** - Next.js-based frontend with server-side rendering for optimal performance
- **API Layer** - RESTful endpoints handling authentication, data queries, and real-time updates
- **Data Pipeline** - Python workers processing market data, computing indicators, and generating alerts
- **Caching Layer** - Redis for real-time data caching, session management, and pub/sub messaging
- **Job Queue** - BullMQ handling background tasks like report generation and alert processing
- **Storage** - PostgreSQL for persistent data, S3 for chart images and static assets

---

## Contact

Interested in learning more about the platform or exploring partnership opportunities?

**Email:** contact@ofc-trading.xyz

---

*Source code is private. Contact for more info.*
