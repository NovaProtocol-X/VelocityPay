# VelocityPay

> High-speed merchant POS interface with instant USDC settlements on Stellar

---

## Overview

VelocityPay is a **high-speed merchant point-of-sale (POS) interface** built on Stellar. It generates dynamic QR codes using the **SEP-7** standard for instant USDC settlements with **5-second finality**.

Thanks to Stellar's native path payment functionality, customers can pay in any asset they hold — while merchants always settle in stablecoins. No manual conversions, no custodial risk, no delays.

---

## Features

- **SEP-7 QR Codes** — Dynamic, per-transaction QR codes for seamless checkout
- **5-Second Finality** — Near-instant settlement on Stellar's network
- **Any-Asset Payments** — Customers pay in any Stellar asset; merchants receive stablecoins
- **Path Payment Integration** — Automatic on-chain conversion at point of sale
- **USDC Settlement** — Merchant funds land directly in stablecoins

---

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/)

### Installation

**1. Set up the mobile/web UI:**
```bash
cd web && npm install
```

**2. Test the QR code generation logic:**
```bash
npm test packages/qr-gen
```

**3. Run the local development server:**
```bash
npm run dev
```

The interface will be available at `http://localhost:3000`.

---

## Project Structure

```
velocitypay/
├── web/                # Merchant POS web interface
├── packages/
│   └── qr-gen/         # SEP-7 QR code generation package
├── tests/              # Test suite
└── CONTRIBUTING.md     # Contribution guidelines
```

---

## How It Works

1. The merchant opens VelocityPay and enters the transaction amount
2. A **SEP-7 QR code** is dynamically generated for that payment request
3. The customer scans the QR code with any SEP-7 compatible Stellar wallet
4. Stellar's **path payment** engine converts the customer's asset to USDC on-chain
5. The merchant receives **USDC in ~5 seconds** — settlement complete

---

## Contributing

We're actively looking for contributors to help build **POS hardware integrations** — connecting VelocityPay to physical merchant terminals and hardware wallets. If you're interested, see [CONTRIBUTING.md](./CONTRIBUTING.md) for how to get involved.

---

## License

This project is licensed under the [MIT License](./LICENSE).
