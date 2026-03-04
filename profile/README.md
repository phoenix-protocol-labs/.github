# 🔥 PHOENIX — On-Chain Structured Products, Fully Automated 🏛️

> **Institutional-Grade. Trustless. Automated. Welcome to the future of structured products on [Arbitrum](https://arbitrum.io), powered by [Chainlink CRE](https://chain.link).**

[➡️ Live Demo](https://phoenix-protocol.xyz/) · [📄 Documentation](https://phoenix-protocol.xyz/docs)

---

## ✨ What is Phoenix?

**Phoenix** is an on-chain protocol that brings **autocall structured products** — a multi-trillion dollar TradFi market — to DeFi. Deposit USDC, pick your barriers, and let **Chainlink CRE** handle the rest: price observation, barrier evaluation, and settlement, all **fully automated** with zero manual intervention.

The secret weapon? The **Phoenix Memory Coupon** — missed coupons aren't lost, they're *remembered* and paid retroactively.

---

## 💥 Start Earning Structured Yield

<p align="center">
  <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&size=20&duration=3000&pause=1000&color=FF6B35&center=true&vCenter=true&width=700&lines=🏛️+TradFi+structured+products+on-chain;🔗+Automated+by+Chainlink+CRE;🔥+Missed+coupons+remembered+%26+paid+back;💰+Idle+capital+earns+yield+on+Aave" alt="Typing SVG" />
</p>

[➡️ Explore Vaults](https://phoenix-protocol.xyz/app)

---

## 🚀 Core Advantages

| 🏛️ Institutional Mechanics | 🔗 Fully Automated | 🔥 Phoenix Memory |
|---------------------------|--------------------|--------------------|
| Real autocall products with configurable **barriers**, **coupon rates**, and **observation schedules** — the same products banks sell to institutions. | **Chainlink CRE** handles everything: cron-triggered observations, DON-consensus pricing from **5 data sources**, and on-chain settlement. Zero keepers. | Missed coupons are **never lost** — they accumulate and get paid retroactively on the next favorable observation. |

| 💰 Aave Yield on Deposits | 📊 5 Data Sources | 🏭 Factory Pattern |
|--------------------------|-------------------|--------------------|
| All USDC deposits are auto-supplied to **Aave V3**. Your capital earns yield while locked, on top of structured product coupons. | Pendle, Hyperliquid, xStocks, Aave rates, DeFi Llama — **13 vaults** across crypto and **real-world stocks**. | Create custom vaults with your own barriers, coupon rates, and maturity via the **AutocallFactory**. |

---

## 🧠 How It Works

```
📅 CRE Cron fires
        │
   Fetch price (DON consensus median)
        │
        ▼
  price ≥ 100% (autocall barrier)?
   ┌────┴────┐
   │ YES     │ NO
   ▼         ▼
 AUTOCALL   price ≥ 70% (coupon barrier)?
 Capital +   ┌────┴────┐
 all coupons │ YES     │ NO
 returned    ▼         ▼
         PAY_COUPON  price ≥ 60% (knock-in)?
         + memory     ┌────┴────┐
         coupons     │ YES     │ NO
                     ▼         ▼
                  CONTINUE   KNOCK_IN
                  (missed,   (capital loss,
                   remembered) memory forfeited)
```

---

## 🔥 Phoenix Memory Coupon — The Innovation

> *"What if missed coupons could come back?"*

When a coupon is missed because the price dips between the knock-in and coupon barriers, Phoenix **remembers** it. On the next favorable observation, all accumulated missed coupons are **paid retroactively**.

| Period | Price | Action | Memory | Payout |
|:------:|:-----:|--------|:------:|--------|
| 1 | $0.85 | ✅ PAY_COUPON | 0 | **$0.05** |
| 2 | $0.65 | ⏸️ CONTINUE | 1 | $0.00 *(remembered)* |
| 3 | $0.68 | ⏸️ CONTINUE | 2 | $0.00 *(remembered)* |
| 4 | $0.90 | ✅ PAY_COUPON | 0 | **$0.15** *(current + 2 memory)* |

---

## 📦 Vault Catalog — 13 Live Vaults

| Vault | Underlying | Source | Strike |
|-------|-----------|--------|--------|
| 🟢 Conservative YT | ETH | Pendle | $1.00 |
| 🔴 Aggressive YT | ETH | Pendle | $1.00 |
| 📊 6-Period Demo | ETH | Pendle | $1.00 |
| 📈 ETH Perp | ETH | Hyperliquid | $3,800 |
| 🍎 AAPL | AAPL | xStocks | $275 |
| ⚡ TSLA | TSLA | xStocks | $415 |
| 🟩 NVDA | NVDA | xStocks | $195 |
| 📦 AMZN | AMZN | xStocks | $230 |
| 🔍 GOOG | GOOG | xStocks | $185 |
| 💧 WETH Rate | WETH | Aave | 2.5% APY |
| 💵 USDC Rate | USDC | Aave | 4.0% APY |
| 🔷 stETH | stETH | Lido / DeFi Llama | $3,800 |
| 🔶 wstETH | wstETH | Lido / DeFi Llama | $4,500 |

---

## ❓ Frequently Asked Questions

<details>
  <summary>🤔 What are structured products?</summary>
  <p>Structured products are derivatives with conditional payoffs based on an underlying asset's performance. They are a <strong>multi-trillion dollar market</strong> in TradFi — think autocalls, reverse convertibles, and capital-protected notes.</p>
</details>

<details>
  <summary>🔥 What is the Phoenix Memory Coupon?</summary>
  <p>When a coupon is missed (price between knock-in and coupon barriers), it's <strong>remembered, not lost</strong>. On the next favorable observation, all missed coupons are paid retroactively. A knock-in event forfeits them.</p>
</details>

<details>
  <summary>💰 How do deposits earn yield?</summary>
  <p>All USDC deposits are automatically supplied to <strong>Aave V3</strong>. Your capital earns the Aave supply rate while locked in the vault — on top of any structured product coupons.</p>
</details>

<details>
  <summary>🔗 How does Chainlink CRE automate settlement?</summary>
  <p>CRE runs a cron-triggered workflow across the Chainlink DON: it fetches prices from 5 external APIs, reaches <strong>consensus via median aggregation</strong>, evaluates barriers, and writes the settlement action on-chain via <code>IReceiver.onReport()</code>. Zero keepers, fully trustless.</p>
</details>

<details>
  <summary>🚀 How do I get started?</summary>
  <p>Connect your wallet on Arbitrum Sepolia, mint test USDC, pick a vault, deposit, and watch the automated observation lifecycle unfold.</p>
</details>

---

## 🏗️ Architecture

```
                     Frontend
                (React + Vite + wagmi)
                        │
                        ▼
        ┌───────────────────────────────┐
        │        Smart Contracts        │
        │  Factory + Vault + Settlement │
        └───────────────────────────────┘
             │                    │
             ▼                    ▼
       Chainlink CRE          Aave V3
    (Cron + HTTP + EVM)    (yield on deposits)
             │
   ┌─────────┼─────────┬─────────┬─────────┐
   │         │         │         │         │
 Pendle  Hyperliquid  xStocks   Aave   DeFi Llama
(YT price) (perp mid) (stocks) (rates) (prices)
```

---

## 🏗️ Tech Stack

| Layer | Technology |
|-------|-----------|
| 🔐 **Smart Contracts** | Solidity 0.8.24 · Foundry · OpenZeppelin v5 |
| 🔗 **Oracle & Automation** | Chainlink CRE v1.0.9 · TypeScript → WASM |
| ⚛️ **Frontend** | React 19 · Vite · Tailwind CSS 4 · wagmi v3 · viem v2 |
| 💰 **Yield** | Aave V3 (automated supply/withdraw) |
| ⛓️ **Network** | Arbitrum Sepolia (chainId 421614) |
| 📊 **Data Sources** | Pendle · Hyperliquid · xStocks · DeFi Llama |
| 🧪 **Testing** | Forge — **47 passing tests** |

---

## 🤝 Built With & Powered By

<p align="center">
  <img src="https://raw.githubusercontent.com/phoenix-protocol-labs/.github/main/profile/assets/Phoenix.svg" alt="Phoenix Protocol" height="100" />
</p>

<p align="center">
  <a href="https://phoenix-protocol.xyz"><strong>Phoenix Protocol</strong></a> is proudly built on <a href="https://arbitrum.io"><strong>Arbitrum</strong></a>, powered by <a href="https://chain.link"><strong>Chainlink CRE</strong></a>.
</p>

<p align="center">
  <img src="https://raw.githubusercontent.com/phoenix-protocol-labs/.github/main/profile/assets/Chainlink_Logo_White.svg" alt="Chainlink" height="30" />
  &nbsp;&nbsp;&nbsp;&nbsp;
  <img src="https://raw.githubusercontent.com/phoenix-protocol-labs/.github/main/profile/assets/xstocks.svg" alt="xStocks" height="30" />
</p>

---

> _"Phoenix doesn't just bring structured products on-chain — it makes them **automated**, **transparent**, and **accessible** to everyone."_ 🔥

<p align="center">
  <img src="https://img.shields.io/badge/structured_products-on--chain-orange?style=for-the-badge" />
  <img src="https://raw.githubusercontent.com/phoenix-protocol-labs/.github/main/profile/assets/chainlink_build_blue.png" alt="Built with Chainlink" height="45" />
  <img src="https://img.shields.io/badge/47_tests-passing-brightgreen?style=for-the-badge" />
  <img src="https://img.shields.io/badge/13_vaults-live-blue?style=for-the-badge" />
</p>
