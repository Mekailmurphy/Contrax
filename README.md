# 👷Contrax👷
---
## Solidity Contracts / Contracts that are EVM compatible.

Tinkering with Hardhat (having previously used truffle) a framework the helps with the devlopement, compilation, debugging, and testing of code
through virtual enviorments. We will also be utilizing the Remix-IDE directly, as well as other various methods.

These contracts will be used as a base.

## 721RandomURI.sol
RandomURI achieved through mapping. Mixing up and create an array the size of the collection was not gas effecient. 

The generateRandomTokenNumber() function uses the current timestamp, block difficulty, and sender address to generate a pseudo-random number between 1 and maxSupply. If the generated number has already been used for an existing token, the function increments the number by 1 (wrapping around to 1 if the number exceeds maxSupply) until it finds an unused number. Once an unused number is found, the function marks it as used in the usedTokenNumbers mapping and returns it.

The mintRandom() function uses the generateRandomTokenNumber() function to generate a random token number for each NFT being minted. This ensures that each NFT has a unique and a semi-unpredictable token number.
