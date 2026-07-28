<h1 align="center">Arpit Anand</h1>
<p align="center"><b>Blockchain Developer · Smart Contract Engineer</b></p>
<p align="center">
  I build smart contracts that hold user funds — wallets, AMMs and derivatives protocols — on both Move and EVM chains.
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/anand-arpit">LinkedIn</a> ·
  <a href="https://www.twitter.com/arpit_333">Twitter</a> ·
  <a href="mailto:arpitanand333@gmail.com">arpitanand333@gmail.com</a>
</p>

---

## About

Blockchain developer with **4.5+ years** of experience building and deploying production smart contracts. I work in **Move** on Aptos and Supra, **Solidity** on Ethereum and BSC, and **Rust** on Solana — and I've shipped the same protocol twice across two virtual machines when a product needed to run on both.

- **Current focus** — wallet infrastructure and account abstraction, automated market maker design, and on-chain derivatives
- **What I'm good at** — protocol accounting, fee and settlement logic, contract size and gas constraints, and the pre-deployment review pass that catches what tests miss
- **Also ship** — the specification and the test suite alongside the contract, so other teams can build against it
- Based in Ahmedabad, India · M.Sc. Computer Science, Central University of South Bihar

---

## Tech Stack

**Languages**

![Solidity](https://img.shields.io/badge/Solidity-363636?style=flat-square&logo=solidity&logoColor=white)
![Move](https://img.shields.io/badge/Move-Aptos%20%7C%20Supra%20%7C%20Sui-4FC3F7?style=flat-square)
![Rust](https://img.shields.io/badge/Rust-000000?style=flat-square&logo=rust&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)

**Chains**

![Ethereum](https://img.shields.io/badge/Ethereum-3C3C3D?style=flat-square&logo=ethereum&logoColor=white)
![BNB Chain](https://img.shields.io/badge/BNB%20Chain-F0B90B?style=flat-square&logo=binance&logoColor=black)
![Aptos](https://img.shields.io/badge/Aptos-06F7F7?style=flat-square&logoColor=black)
![Supra](https://img.shields.io/badge/Supra-DC2626?style=flat-square)
![Solana](https://img.shields.io/badge/Solana-14F195?style=flat-square&logo=solana&logoColor=black)
![Sui](https://img.shields.io/badge/Sui-4DA2FF?style=flat-square)

**Tooling**

![Foundry](https://img.shields.io/badge/Foundry-1C1C1C?style=flat-square)
![Hardhat](https://img.shields.io/badge/Hardhat-FFF100?style=flat-square&logoColor=black)
![Anchor](https://img.shields.io/badge/Anchor-2A2A2A?style=flat-square)
![Aptos CLI](https://img.shields.io/badge/Aptos%20CLI-06F7F7?style=flat-square&logoColor=black)
![Remix](https://img.shields.io/badge/Remix%20IDE-2A2C33?style=flat-square)
![OpenZeppelin](https://img.shields.io/badge/OpenZeppelin-4E5EE4?style=flat-square&logo=openzeppelin&logoColor=white)
![ethers.js](https://img.shields.io/badge/ethers.js-2535A0?style=flat-square)

---

## What I Work On

| Domain | Work |
| --- | --- |
| **Wallets** | HD key generation (BIP-32/39/44), smart contract wallets, guardian-based social recovery, relayer-paid gasless transactions |
| **AMMs & Markets** | Liquidity-sensitive LMSR pricing, multi-outcome prediction markets, fee splits and settlement, dispute resolution |
| **Derivatives** | Perpetual futures, leverage and liquidation engines, funding rates, LP pool accounting, oracle price feeds |
| **Security** | Pre-deployment contract review, accounting and access-control audits, Move and Foundry test suites, gas and contract size optimization |

---

## Selected Work

Most of this is client and product work under private repositories, so it is described rather than linked.

### Multi-Chain Non-Custodial Wallet — key generation and smart contract wallet
`TypeScript` · `BIP-32/39/44` · `Move` · `Solidity` · `Rust (Anchor)`

Built the key pair generation layer on the BIP-39, BIP-32 and BIP-44 standards, so a single 12-word recovery phrase deterministically generates accounts on every supported chain. Reviewed the cryptographic libraries behind it, confirmed randomness comes from the platform's secure random generator in browser and Node.js, and verified that phrases created in the wallet restore the same accounts in MetaMask, Phantom and Sui Wallet. Wrote the specification the extension and mobile teams build against.

Developed the accompanying smart contract wallet on **three virtual machines** — Aptos Move, Solidity and Solana Anchor — with guardian-based recovery that restores access to a compromised wallet without exposing private keys, signature verification with replay protection, daily transaction and spending limits, owner and sub-owner roles, and relayer-paid transactions so new users can transact without funding an account first.

### Multi-Outcome Prediction Market — Move and EVM
`Move (Supra, Aptos)` · `Solidity` · `Foundry` · `OpenZeppelin`

A prediction market where users trade outcome shares directly against the contract through a liquidity-sensitive LMSR automated market maker, so prices move with demand and reflect the implied probability of each outcome. Covers the full lifecycle: proposal with escrowed liquidity, admin approval, a liquidity bootstrap window that refunds providers if the minimum isn't reached, trading, resolution and settlement — plus a capped three-way fee split and a dispute process with a bounded admin response window.

Delivered the same protocol in Solidity for EVM chains behind upgradeable proxies, with role-based admin access, reentrancy protection and a modular structure that fits EVM contract size limits. Found and fixed two accounting defects during pre-deployment review: a fee split that overpaid liquidity providers, and a vault balance mismatch between buys and sells that would have produced incorrect payouts at settlement.

### Perpetual Futures Trading Protocol — Move
`Move (Supra)` · `Supra Oracle`

Leveraged long and short positions against a shared liquidity pool that acts as counterparty to every trade, with entry and liquidation prices calculated on-chain. Includes pro-rata LP token issuance and redemption, open interest limits that keep pool exposure within what it can cover, oracle price feeds with staleness validation, market and limit orders with entry and exit triggers, forced closure for liquidations, and periodic funding rate settlement.

### On-Chain Reward Distribution with Verifiable Randomness — Move
`Move (Supra)` · `Supra dVRF`

A reward vault that selects winners using a verifiable random function, with the proof verified on-chain before any reward is assigned, so outcomes cannot be influenced by the operator. Implements the full randomness request and callback flow, including fee funding, per-user request tracking and handling for requests that fail to return.

### Earlier work

EVM application contracts before moving to Move: a BSC IDO launchpad with automated liquidity locking and LP staking, DAO governance contracts with time-locked proposal voting, and an ERC-721 NFT marketplace with IPFS metadata, pack minting and auctions.

---

## GitHub

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=arpitanand333&show_icons=true&count_private=true&hide_border=true&title_color=0891b2&icon_color=0891b2" alt="GitHub stats" height="160" />
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=arpitanand333&layout=compact&langs_count=8&hide_border=true&title_color=0891b2" alt="Top languages" height="160" />
</p>

---

<p align="center">
  Open to smart contract engineering and protocol work — <a href="mailto:arpitanand333@gmail.com">arpitanand333@gmail.com</a>
</p>
