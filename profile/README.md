# PHOENIX — On-Chain Structured Products, Fully Automated 🏛️

> **Institutional-Grade. Trustless. Automated. Welcome to the future of structured products on-chain, powered by [Chainlink CRE](https://chain.link).**

🏆 **Built for the [Chainlink Convergence Hackathon](https://chain.link/hackathon)** — DeFi & Tokenization Track

[➡️ Live Demo](https://phoenix-protocol-fi.vercel.app/)

---

## ✨ What is Phoenix?

**Phoenix** is a decentralized protocol bringing **autocall structured products** on-chain — a multi-trillion dollar TradFi market, now accessible to everyone. Powered by **Chainlink CRE** for fully automated settlement and the **Phoenix Memory Coupon** that remembers missed coupons and pays them back.

https://github.com/user-attachments/assets/589381ea-716c-4425-83d4-dac5af27ee98

---

## 💥 Start Earning Structured Yield

<p align="center">
  <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&size=20&duration=3000&pause=1000&color=FF6B35&center=true&vCenter=true&width=700&lines=🏛️+TradFi+structured+products+on-chain;🔗+Automated+by+Chainlink+CRE;🔥+Missed+coupons+remembered+%26+paid+back;💰+Idle+capital+earns+yield+on+Aave" alt="Typing SVG" />
</p>

[➡️ Explore Vaults](https://phoenix-protocol-fi.vercel.app/app)

---

## 🚀 Core Advantages

| 🏛️ Institutional Mechanics | 🔗 Fully Automated | 🔥 Phoenix Memory |
|---------------------------|--------------------|--------------------|
| Real autocall products with configurable **barriers**, **coupon rates**, and **schedules** — same products banks sell to institutions. | **Chainlink CRE** runs the full pipeline: cron observation, DON-consensus pricing, on-chain settlement. No keepers. | Missed coupons are **never lost** — they accumulate and get paid retroactively on the next favorable observation. |

---

## 🔥 Phoenix Memory Coupon

> *Missed a coupon? Phoenix remembers.*

| Period | Price | Action | Memory | Payout |
|:------:|:-----:|--------|:------:|--------|
| 1 | $0.85 | ✅ PAY_COUPON | 0 | **$0.05** |
| 2 | $0.65 | ⏸️ CONTINUE | 1 | $0.00 *(remembered)* |
| 3 | $0.68 | ⏸️ CONTINUE | 2 | $0.00 *(remembered)* |
| 4 | $0.90 | ✅ PAY_COUPON | 0 | **$0.15** *(current + 2 memory)* |

---

## ❓ Frequently Asked Questions

<details>
  <summary>🤔 What are structured products?</summary>
  <p>Derivatives with conditional payoffs based on an underlying asset's performance. A <strong>multi-trillion dollar market</strong> in TradFi — autocalls, reverse convertibles, capital-protected notes.</p>
</details>

<details>
  <summary>🔥 What is the Phoenix Memory Coupon?</summary>
  <p>When a coupon is missed, it's <strong>remembered, not lost</strong>. On the next favorable observation, all missed coupons are paid retroactively.</p>
</details>

<details>
  <summary>💰 How do deposits earn yield?</summary>
  <p>All USDC deposits are auto-supplied to <strong>Aave V3</strong>. Your capital earns yield while locked — on top of structured product coupons.</p>
</details>

<details>
  <summary>🚀 How do I start?</summary>
  <p>Connect your wallet, deposit USDC into a vault, and watch the automated observation lifecycle unfold.</p>
</details>

➡️ [See More FAQs](https://phoenix-protocol-fi.vercel.app/faq)

---

## 🔗 Built With Chainlink CRE

Phoenix is proudly **powered by Chainlink CRE** — the Compute Runtime Environment that automates price observation, barrier evaluation, and on-chain settlement across **13 vaults** and **5 data sources**.

Built as part of the [**Chainlink Convergence Hackathon**](https://chain.link/hackathon) — DeFi & Tokenization Track.

[🔍 Learn more about Chainlink CRE](https://chain.link)

---

## 🏗️ Tech Stack

- 🔐 **Solidity Smart Contracts** (Foundry + OpenZeppelin)
- 🔗 **Chainlink CRE** (TypeScript → WASM)
- ⚛️ **React + Vite + wagmi**
- 💰 **Aave V3 Yield Integration**
- ⛓️ **EVM Compatible**

---

## 🤝 Powered by & in Partnership With

<p align="center">
  <img src="https://raw.githubusercontent.com/phoenix-protocol-labs/.github/main/profile/assets/phoenix-white.svg" alt="Phoenix Protocol" height="100" />
</p>

<p align="center">
  <a href="https://phoenix-protocol-fi.vercel.app"><strong>Phoenix Protocol</strong></a> is proudly powered by <a href="https://chain.link"><strong>Chainlink CRE</strong></a>.
</p>

<p align="center">
  <img src="https://raw.githubusercontent.com/phoenix-protocol-labs/.github/main/profile/assets/Chainlink_Logo_White.svg" alt="Chainlink" height="30" />
</p>

---

> _"Phoenix doesn't just bring structured products on-chain — it makes them automated, transparent, and accessible to everyone."_ 🔥

<p align="center">
  <img src="https://img.shields.io/badge/DeFi_&_Tokenization-Track-375BD2?style=for-the-badge" />
  <a href="https://chain.link/hackathon"><img src="https://img.shields.io/badge/Chainlink-Convergence_Hackathon-375BD2?style=for-the-badge&logo=chainlink&logoColor=white" alt="Chainlink Convergence Hackathon" /></a>
  <img src="https://img.shields.io/badge/structured_products-on--chain-FF6B35?style=for-the-badge" />
</p>
