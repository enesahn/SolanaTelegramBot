# 🚀 Solana Trading Telegram Bot
Your personal trading companion for the Solana blockchain! This powerful Telegram bot helps you trade like a pro with automated features, real-time monitoring, and smart wallet management.

## ✨ What Can This Bot Do?

### 🎯 Core Features

- **Smart Trading**
  - Buy and sell tokens automatically
  - Set up limit orders (take profit & stop loss)
  - Execute trades through multiple platforms
  - Snipe new tokens as soon as they launch 🎯

- **Wallet Management**
  - Create new wallets or import existing ones
  - Track your balances in real-time
  - Switch between wallets with ease

- **First build-in Scraper Feature**
  - Twitter Scraper
     - Advanced CA Detection
     - <250ms tweet detection
     - Blacklist Word Filtering
     
  - Telegram Channel/Group Scraper
     - Bot/User/Admin Filter
     - Advanced CA Detection
     - ReBuy Protection
     - Blacklist Word Filtering

  - Discord Scraper
     - Custom User Message Filter
     - Blacklist Word Filtering
     - Advanced CA Detection

## 🛠️ Tech Stack
- TypeScript (runs on Node.js or Bun)
- MongoDB for data storage
- Redis for lightning-fast caching
- Multiple APIs (Helius, Quicknode, GRPC)

## 📦 Getting Started

### Prerequisites
- Node.js or Bun
- MongoDB
- Redis
- Telegram Bot Token (get it from [@BotFather](https://t.me/botfather))

### Quick Setup

1. **Clone & Install**
   ```bash
   git clone https://github.com/enesahn/SolanaTelegramBot.git
   cd SolanaTelegramBot
   npm install   # or 'bun install' if you're using Bun
   ```

2. **Set Up Your Environment**
   Create a `.env` file with your secrets 🔐

3. **Launch! 🚀**
   ```bash
   npm run dev    # for development
   npm run start  # for production
   ```

## 🔑 Environment Variables

### Core Settings
```env
BOT_TOKEN=your-telegram-bot-token
MONGODB_URI=your-mongodb-connection-string
REDIS_URL=your-redis-url
```

### Blockchain Connections
```env
# Helius Endpoints
HELIUS_RPC_HTTP=https://api.mainnet-beta.solana.com
HELIUS_RPC_WS=wss://api.mainnet-beta.solana.com
HELIUS_RPC_STAKED_HTTP=https://solana-mainnet.rpcpool.com

# GRPC Settings
GRPC_ENDPOINT=https://grpc.ams.shyft.to
GRPC_TOKEN=your-grpc-auth-token

# Quicknode Access
QUICKNODE_HTTP=https://solana-mainnet.quicknode.pro/your-api-key
QUICKNODE_WS=wss://solana-mainnet.quicknode.pro/your-api-key
```

## 📁 Project Structure
```
src/
├── config/      # Bot configuration files
├── cron/        # Scheduled tasks
├── handlers/    # Command & event handlers
├── messages/    # User communication templates
├── models/      # Database schemas
├── services/    # Core business logic
├── swaps/       # Trading execution code
└── utils/       # Helper functions
```

## 🚀 Features In Detail

### 🎯 Social Scrapers

#### 📱 Twitter Scraper
- **Ultra-Fast Detection**
  - Sub-250ms tweet detection capability
  - Real-time stream processing
  - Minimal latency for faster trading execution
- **Smart Contract Address (CA) Detection**
  - Advanced CA identification
  - Multi-format support (raw address, embedded links)
  - Automatic verification and validation
- **Blacklist Word Filtering**
  - Avoids rug token messages etc.
  - Ensures trading security

#### 💬 Telegram Scraper
- **Advanced Filtering System**
  - Bot detection and filtering
  - Admin message prioritization
- **Smart Features**
  - Automatic CA detection and validation
  - ReBuy Protection to prevent duplicate purchases
  - Custom filter configurations
- **Blacklist Word Filtering**
  - Avoids rug token messages etc.
- **Performance Optimization**
  - Parallel message processing
  - Rate limit handling
  - Resource-efficient monitoring

#### 🎮 Discord Scraper
- **Custom User Message Filtering**
  - Filters messages based on user-defined criteria
- **Blacklist Word Filtering**
  - Avoids rug token messages etc.
- **Smart Contract Address (CA) Detection**
  - Identifies contract addresses in Discord messages
  - Multi-format support

### 🔎 **Advanced Smart Contract Address (CA) Detection**
- **Handles Special Characters**: Detects CA even with special characters or unusual formats
- **Partial CA Detection**: Identifies split or incomplete contract addresses
- **Multi-Format Support**: Recognizes raw addresses, embedded links, and hidden CA formats
- **Automated Verification**: Ensures validity before execution
- **Cross-Platform Scraping**: Works across different sources like Twitter, Telegram, and Discord

### 💼 Wallet Management
- Secure wallet creation and import
- Multi-wallet support
- Real-time balance tracking

### 📊 Monitoring & Reports
- Real-time portfolio tracking
- PnL calculations and visualization

## 🤝 Contributing
Got ideas? We'd love to hear them! Feel free to:
- Open issues
- Submit pull requests
- Suggest new features

## 📝 License
This project its still building. If u have a question TELEGRAM: @nidtowest

---
Happy Trading! 🚀✨
