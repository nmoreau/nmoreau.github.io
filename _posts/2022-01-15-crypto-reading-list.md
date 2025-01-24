---
layout: post
title:  "Crypto Reading list (Jan 2022)"
description : ""
date: 2022-01-15
author: 
-  Moreau
published: true
---
I gather in this page some of the key readings I believe can be helpful to others. <br>
This structure also helped me navigate in that field. Not every item have links.<br> 
Note this is a **living document**. Yes, this can be messy.

## Core Crypto Papers
- [Bicoin Whitepaper](https://bitcoin.org/bitcoin.pdf) - October 2008
- [Ethereum Whitepaper](https://ethereum.org/en/whitepaper/) - 2013

## Books about Crypto 
These are a few book that read like thrillers and who provide good context on how this was build and the people behind.
- [The Infinite Machine](https://www.amazon.com/Infinite-Machine-Crypto-hackers-Building-Internet-ebook/dp/B07X8HS2WC) by Camila Russo <br> A thriller like story of how an army of Crypto-hackers is Building the next Internet with Ethereum 

- [The Blocksize War](https://www.amazon.com/Infinite-Machine-Crypto-hackers-Building-Internet-ebook/dp/B07X8HS2WC) by Jonathan Bier <br> The fight inside the Bitcoin dev community to scale Bitcoin to make it a payment network, vs the more conservative vision as a store a value

- [Kings of Crypto](https://www.amazon.com/Kings-Crypto-Startups-Cryptocurrency-Silicon-ebook/dp/B085TRJY8X) by Jeff John Roberts <br> The story of how Coinbase was created and how it became the biggest Crypto Exchange in the US

## Critical thinking articles
- [Proof-of-Stake and Stablecoins: A Blockchain Centralization Dilemma](https://www.lynalden.com/proof-of-stake/) by Lyn Alden
- [An Economic Analysis of Ethereum](https://www.lynalden.com/ethereum-analysis/) by Lyn Alden

## Crypto Domain Breakdown
I am trying here to break down some of the key aspects of Crypto
- Blockchain Tech and underlying principles <br>
The key here is to understand the concepts behind : a distributed, permissionless, and cryptographicaly secure database. (TODO Blog post)
- Blockchain instances
  - L1 Core Chains : BTC, ETH
  - L1 Gen2 Chains : Solana, Ada, Algorand, Polkadot, Avalanche
- L2 Scaling - Get more throughput, low latency at low cost, while still preserving security
  - [Ethereum L2 Scaling solutions](https://medium.com/coinmonks/easy-to-understand-ethereum-layer-2-scaling-solutions-channels-vs-plasma-vs-rollups-1dc1d4e9cb52) 
  - State Channels
  - Plasma
  - Rollups
    - Optimistic Rollup - "fraud proofs" (Arbitrum, Optimism)
    - ZK Rollups - "validity proofs": Zksync (Matterlabs), Starkware <br>
    On Zero Knowledge Proofs, [here](https://github.com/matter-labs/awesome-zero-knowledge-proofs) is a great reading list maintained by Matterlabs
    
- ERC20 Token
- NFTs : ERC721 and ERC1155 

## Hands on Learning resources
This is based on hands on lab I have made and documented with samples [here](https://github.com/nmoreau/ethereumsamples)

- [Austin Griffith Eth.Build](https://sandbox.eth.build/) To understand the basics on how a Blockchain works and the cryptographic concept behind
- [Patrick Alpha Youtube Video](https://youtu.be/M576WGiDBdQ?t=5368) - Excellent 14 hours video to become a Solidity (aka: Smart contract programming language) developer

## TODO Below 

## Wallets
TODO

## StableCoins
- Centralized StableCoins peed by Fiat : USDT (Tether), USDC (Circle/Coinbase), BUSD
- Decentralized Stablecoins NOT pegged by Fiat : DAI, UST (Terra) which has some [fundamental flaws IMOs](https://www.semanticscholar.org/paper/SoK%3A-Decentralized-Finance-(DeFi)-Werner-Perez/e86439872d0f7ae3339d7215ce8729fb11949c1e)

## DeFi
- Dex
- Liquidity mining
- Lending
- Borrowing

## Web3.js API Namespace
https://web3js.readthedocs.io/en/v1.5.2/
