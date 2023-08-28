# DynamicNFT-Chainlink
---
Created a Dynamic NFT that shows the market trend using Chainlink Automation and Chainlink VRF services. Contracts deployed on Sepolia Testnet.
---

The NFT is minted to the Testnet Opensea using safeMint function.

There are 3 different Bull and 3 different Bear images in the IPFS files. Using BTC/USD pair, contract checks the market trend and determines whether it is Bearish or Bullish. Then, it RANDOMLY decides which of the 3 images will be re-minted to the testnet. This randomness procedure is determined using ChainlinkVRF (https://vrf.chain.link/). The interval used to monitor the market trend is determined using interval function, and the performUpkeep function can controll automatically using Chainlink Automation (https://automation.chain.link/).

A Mock price feed contract (MockPriceFeed.sol) is used in test procedures to control the BTC/USD pair manually. 

