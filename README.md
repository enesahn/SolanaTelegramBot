# Solana Trading Telegram Bot

A highly advanced Telegram bot built for the Solana blockchain that focuses on automated trading and launch sniping. The bot supports trading on **Raydium** and **Pumpfun** liquidity platforms exclusively, and it features powerful scraper integrations for **Twitter** and **Telegram**. In addition, the bot includes a new launch snipe module built on Pumpfun.

---

## Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Environment Variables](#environment-variables)
- [Usage](#usage)
- [File Structure](#file-structure)
- [Contributing](#contributing)
- [Troubleshooting](#troubleshooting)
- [License](#license)
- [Acknowledgements](#acknowledgements)

---

## Features

- **Trading Support Platforms (Raydium & Pumpfun Only)**  
  - **Raydium & Pumpfun Swap Integration:**  
    The bot exclusively supports trading on Raydium and Pumpfun liquidity pools. It uses the Jupiter API for live token quotes and performs swaps through a unified SwapSystem utilizing these two platforms.
  - **Auto Trading & Limit Orders:**  
    Automated buy and sell operations using configurable limit orders (take profit / stop loss). (All auto trading operations are supported on Raydium and Pumpfun.)

- **Wallet Management**  
  - Create new wallets, import existing ones, export private keys securely.
  - View wallet balances in SOL and USD with live price feeds.

- **Market Data Integration**  
  - Live SOL price updates and robust token data retrieval via the Jupiter API.
  - Redis caching is used to optimize repeated data requests and reduce API load.

- **PNL Reporting**  
  - Generate high-quality, modern PNL report images using Puppeteer and Tailwind CSS.
  - New design features a dark mode theme with large, clear fonts and responsive layout.
  - Detailed metrics include Cost, Current Value, Profit, ROI, Price, Market Cap, and Liquidity.
  - Interactive exchange links to Solscan, BirdEye, Pump.fun, etc.

- **Scraper Platforms (Twitter & Telegram)**  
  - **Twitter Scraper:**  
    The bot monitors Twitter channels using a Tweet Catcher Auth Token to filter and identify new token-related messages.
  - **Telegram Scraper:**  
    The bot also scrapes messages from Telegram channels/groups for token announcements.
  - Both scraper integrations support blacklist filtering and social links verification to avoid scams or misleading tokens.

- **New Launch Snipe Platform (Pumpfun)**  
  - **Pumpfun Launch Sniping:**  
    The bot includes a dedicated launch snipe module built on Pumpfun. It monitors new mints on Pumpfun in real time and automatically initiates a buy when a new token is detected, based on user-configurable parameters.
  
- **Performance & Monitoring**  
  - Uses MongoDB for persisting user and session data, and Redis for caching critical runtime data.
  - Cron jobs and periodic warmup routines ensure efficient performance and timely data updates.
  - Detailed logging, error handling, and event-based monitoring provide resilient operation in live markets.

- **Administration & Utilities**  
  - Comprehensive command and callback handler suite for trading, wallet management, settings, sniper operations, and more.
  - PM2 process management integration for production deployments.
  - Built-in error and performance reporting via custom middleware and logging.

---

## Installation

### Prerequisites

- **Node.js** (v16+) with npm or bun  
- **MongoDB** instance (local or cloud)  
- **Redis** instance  
- Linux systems: Install required libraries for Puppeteer (e.g., `libatk-1.0-0`, `libgtk-3-0`, etc.). See [Puppeteer Troubleshooting](https://pptr.dev/troubleshooting) for more info.

### Clone & Install

```bash
git clone https://github.com/yourusername/solana-trading-telegram-bot.git
cd solana-trading-telegram-bot
npm install
# or if using bun:
bun install
