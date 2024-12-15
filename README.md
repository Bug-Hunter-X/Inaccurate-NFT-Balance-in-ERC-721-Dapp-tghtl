# Inaccurate NFT Balance in ERC-721 Dapp

This repository demonstrates a common bug in Dapps involving ERC-721 tokens where the balance of NFTs is not accurately reflected.  The `balanceOf` function does not take into account the metadata associated with the tokens, leading to incorrect balance calculations.

## Bug Description
The `balanceOf` function in the provided Solidity smart contract simply returns the value from a mapping of addresses to balances.  It does not interact with the ERC-721 metadata standard, causing an inaccurate reflection of the number of NFTs held by an address.

## Solution
The solution involves using the `tokenURI` function from the ERC-721 standard to properly manage and display the metadata associated with each token. This ensures the correct number of NFTs is counted and displayed.

## How to reproduce
1.  Clone this repository.
2.  Compile the `bug.sol` contract using a Solidity compiler.
3.  Deploy the contract to a test network.
4.  Observe that the `balanceOf` function returns an incorrect NFT balance because it ignores metadata.
5.  Compile and deploy the `bugSolution.sol` contract to see the corrected implementation.
