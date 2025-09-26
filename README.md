# HaikuNFT

ERC-721 NFT implementation for unique Haiku poems with sharing system and uniqueness validation.

## Description

This contract implements an ERC-721 NFT collection where each token represents a unique three-line Haiku poem. The contract enforces uniqueness by preventing any line from being reused across different haikus and includes a sharing mechanism for users to share their haiku collections.

## Features

- **ERC-721 NFT**: Each haiku is a unique, tradeable NFT
- **Uniqueness Enforcement**: No line can be used twice across all haikus
- **Haiku Structure**: Three lines (line1, line2, line3) with author tracking
- **Sharing System**: Share haikus with other addresses
- **Author Attribution**: Each haiku tracks its original author

## Haiku Structure

Each Haiku NFT contains:
- `author` - Address of the haiku creator
- `line1` - First line of the haiku
- `line2` - Second line of the haiku  
- `line3` - Third line of the haiku

## Uniqueness Rules

- Each line across all haikus must be completely unique
- If any line matches a previously used line, minting will fail
- This ensures every haiku contributes original content to the collection

## NFT Details

- **Name**: HaikuNFT
- **Symbol**: HAIKU
- **Token ID**: Sequential starting from 1
- **Metadata**: Stored on-chain in Haiku struct

## Deployment Instructions

1. Open [Remix IDE](https://remix.ethereum.org/)
2. Create a new file and copy-paste the contract code
3. Compile the contract using Solidity ^0.8.0
4. Deploy on **Base Sepolia Testnet**
5. Interact with the functions:
   - `mintHaiku(string line1, string line2, string line3)` - Create new haiku NFT
   - `shareHaiku(address _to, uint256 _haikuId)` - Share your haiku with others
   - `getMySharedHaikus()` - View haikus shared with you
   - `getHaiku(uint256 _haikuId)` - View specific haiku details
   - `getTotalHaikus()` - Get total number of minted haikus


## Submit Exercise

[📖 Submit ERC-721 Tokens Exercise](https://docs.base.org/learn/token-development/erc-721-token/erc-721-exercise)
