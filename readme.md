# 📊 Solana Portfolio Tracker & Challenge NFT Badge System (WIP)

This is a unified **Solana-based dApp project** focused on:

- ✅ Tracking DeFi wallet activity (positions, rewards)
- ✅ Issuing **on-chain NFT badges** for user achievements
- ✅ Integrating a **Twitter bot** for notifications and tracking
- ✅ Giving users **verifiable, non-transferable proof** of performance

> ⚠️ This project is **in progress**. Some features are already working, others are under development.

---

## 🔥 Components

### 1. 🏅 `nft_badge_system` — Challenge-Based NFT Badge Program (Anchor)

This is an **on-chain badge system** that rewards users with **non-transferable NFTs** as proof of their achievements.

#### ✅ Motivation

In Web2, badges and certificates are just images — easily faked and shared.  
In Web3, **NFTs minted to your wallet can't be faked or impersonated.**

#### ✅ What It Does

- Mints a **"Welcome NFT"** automatically when a user registers (triggered via backend).
- Admins can **create new challenges** (levels) with URI/metadata.
- When a user **completes a challenge**, the system mints a badge NFT to their wallet.
- The NFTs are **soulbound-style** (non-transferable, verifiably tied to the user).
- **No need to store user data on-chain** — the backend handles challenge validation.


---

### 2. 🤖 `twitter-bot` — Position + Rewards Tracker

This is a **Twitter bot** that helps users **track their DeFi positions and rewards**.

#### ✅ What It Does

- Takes a **Solana pool ID** (Orca, Raydium, etc.)
- Tracks user's **single-sided LP token positions** in a given range.
- Retrieves and monitors **related farm rewards**.
- Future feature: **Notify users via tweet or DM** when rewards are claimable.

#### 🔧 Status

- [x] Pool ID input
- [x] Position tracking
- [x] Reward fetching
- [ ] Notification triggers
- [ ] Alert for pending claims

---

## 🔗 System Design Overview

### Flow

1. **Backend** verifies user challenge completion (likes, swaps, staking, etc.)
2. If completed → call `nft_badge_system` to mint NFT
3. NFT is minted with:
   - Challenge URI
   - Non-transferable token
   - Ownership = user wallet
4. Users can display NFTs on their profile as **Web3 achievements**

---

## 🧠 Why This Matters

- Turns **gamified dApps** into **verifiable on-chain portfolios**
- Proof of work in Web3 is **transparent, non-fakeable**, and wallet-linked
- Opens up new ways to **showcase progress**, **motivate users**, and **unlock rewards**

---

## 🛠️ Tech Stack

- 🧱 Solana + Anchor (v0.30+)
- 🎨 Metaplex Token Metadata
- 🧠 Backend: Node.js/Express + PostgreSQL (for challenge tracking)
- ⚡ Twitter API (for the bot)
- 🌐 Frontend: Next.js + Tailwind CSS (WIP)

---

## ✅ Next Steps

- [ ] Add frontend UI for NFT gallery
- [ ] Add admin dashboard for challenge management
- [ ] Expand Twitter bot to multiple pools + wallets
- [ ] Auto-sync claimable rewards to badge mints

---

## 💡 Use Cases

- 🧑‍🎓 Education platforms mint "Course Completed" NFTs
- 🧠 DAOs mint proof-of-contribution NFTs
- 🧪 DeFi protocols issue yield farming progress NFTs
- 🏆 Competitions mint proof of win/placement badges

---

## 🙌 Contributing

PRs and ideas welcome. Just raise an issue or get in touch!

---

## 🚧 WIP Disclaimer

This is a **Work In Progress** project. The on-chain program and bot logic are actively evolving. Watch this space.


