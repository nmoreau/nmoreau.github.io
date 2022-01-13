# Nicolas Moreau Blog-ish Random notes and thoughts

This is the place where I will host some good reads, ideas, notes, and samples.

[![Blog](https://img.shields.io/badge/Blog-12100E?style=fplastic&logo=medium&logoColor=white)](http://blog.nmoreau.com)
[![LinkedIn](https://img.shields.io/badge/Linkedin-%230077B5.svg?style=fplastic&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/nicolasmoreau/)
[![Twitter](https://img.shields.io/badge/Twitter-%231DA1F2.svg?style=plastic&logo=Twitter&logoColor=white)](https://twitter.com/nicolasmoreau)
[![GitHub](https://img.shields.io/badge/github-%23121011.svg?style=plastic&logo=github&logoColor=white)](https://github.com/nmoreau/)

# include test 
{% include badges.md %}
{{ content }}

<!-- Index of Posts -->
<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url }}">{{ post.title }}</a>
    </li>
  {% endfor %}
</ul>
<!-- End index of Posts -->

# Crypto Reading list
## Core Crypto Paper
- [Bicoin Whitepaper](https://bitcoin.org/bitcoin.pdf) - October 2008
- [Ethereum Whitepaper](https://ethereum.org/en/whitepaper/) - 2013

## Books about Crypto 
These are a few book that read like thrillers and who provide good context on how this was build and the people behind.
- [The Infinite Machine](https://www.amazon.com/Infinite-Machine-Crypto-hackers-Building-Internet-ebook/dp/B07X8HS2WC) by Camila Russo <br> A thriller like story of how an army of Crypto-hackers is Building the next Internet with Ethereum 

- [The Blocksize War](https://www.amazon.com/Infinite-Machine-Crypto-hackers-Building-Internet-ebook/dp/B07X8HS2WC) by Jonathan Bier <br> The fight inside the Bitcoin dev community to scale Bitcoin to make it a payment network, vs the more conservative vision as a store a value
- [Kings of Crypto](https://www.amazon.com/Kings-Crypto-Startups-Cryptocurrency-Silicon-ebook/dp/B085TRJY8X) by Jeff John Roberts <br> The story of how Coinbase was created and how it became the biggest Crypto Exchange in the US

## Domain Breakdown
- Blockchain Tech and underlying principles
- Blockchain instances
  - L1 Core Chains : BTC, ETH
  - L1 Gen2 Chains : Solana, Ada, Algorand, Polkadot, Avalanche
- L2 Scaling - Get more througput, low latency at low cost, while still preserving security
  - [Ethereum L2 Scaling solutions](https://medium.com/coinmonks/easy-to-understand-ethereum-layer-2-scaling-solutions-channels-vs-plasma-vs-rollups-1dc1d4e9cb52) 
  - State Channels
  - Plasma
  - Rollups
    - Optimistic Rollup - "fraud proofs" (Arbitrum, Optimism)
    - ZK Rollups - "validity proofs": Zksync (Matterlabs), Starkware
- StableCoins
- DeFi


