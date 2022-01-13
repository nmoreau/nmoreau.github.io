---
layout: post
title:  "Blockchain basics and tradeoffs"
description : "A small summary of what a blockchain is, and a simple explanation on the scalability trilemma. "
date: 2022-01-01
author: 
- Nicolas Moreau
published: true
---

In this post, I am trying to extract the essence of what makes blockchain similar and different from any other storage system. This is agnostic to any particular instantiation (Bitcoin, Ethereum, ...) and is a general definition.

## Basic definition

**A Permission less Distributed database** storing state. <br>
Anyone can participate on the infra side (hosting), anyone can have a slot to maintain his/her own state.

## Breaking down further

- **Storage** - Database storing state : What address has what.
- **Updating state** - You need to hold the key (private key) to a particular to initiate a tx from this address to another
- **Committing state** - Every period, the transaction in the backlog (mempool) a taken by minors/validators to update the state. 
- Miners/validators have incentives to secure the network and earn rewards (aka: block reward)
- **Execution layer** - Smart contact is code deployed on a blockchain an can interact with the chain. You can send a Tx or Data to a Smart Contact address.

## 3 Attributes of Blockchain
- **Persistent** / Irreversible / immutable - Cryptographicaly secure
- **Distributed** / No Downtime / Fault tolerant
- **Permissionless** / Decentralized - Anyone can participate - Censorship resistant

## A fine balance between 3 Trade offs

There is a fine balance to find between these 3 attributes.

- Decentralized - If you increase the bar for the min hardware/infra requirements (ex: storage capacity, min bandwidth, compute), then you exclude de factor actors to participate
- Scalable : # of Tx per sec, size of the data stored on Chain
- Secure : It cannot be compromised, vs some actors could decide to collude and influence / try to take control.

![](https://miro.medium.com/max/1000/1*JxrKTU2QczIo_kr1FcKKCg.png)
source [Michael Zochowski](https://medium.com/logos-network/everything-you-know-about-the-scalability-trilemma-is-probably-wrong-bc4f4b7a7ef)
