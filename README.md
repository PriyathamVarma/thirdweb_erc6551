# ERC-6551 using thirdweb

![Main Image]()

## Introduction

The ERC-721 standard enabled an explosion of non-fungible token applications. Some notable use cases have included breedable cats, generative artwork, and liquidity positions.

Non-fungible tokens are increasingly becoming a form of on-chain identity. This follows quite naturally from the ERC-721 specification - each non-fungible token has a globally unique identifier, and by extension, a unique identity.

Unlike other forms of on-chain identity, ERC-721 tokens cannot act as an agent or associate with other on-chain assets. This limitation stands in contrast with many real-world instances of non-fungible assets. For example:

A character in a role-playing game that accumulates assets and abilities over time based on actions they have taken

> An automobile composed of many fungible and non-fungible components

> An automated investment portfolio composed of multiple fungible assets

> A punch pass membership card granting access to an establishment and recording a history of past interactions

Several proposals have attempted to give ERC-721 tokens the ability to own assets. Each of these proposals have defined an extension to the ERC-721 standard. This requires smart contract authors to include proposal support in their ERC-721 token contracts. As a result, these proposals are largely incompatible with previously deployed ERC-721 contracts.

This proposal grants every ERC-721 token the full capabilities of an Ethereum account while maintaining backwards compatibility with previously deployed ERC-721 token contracts. It does so by deploying unique, deterministically-addressed smart contract accounts for each ERC-721 token via a permissionless registry.

Each token bound account is owned by a single ERC-721 token, allowing the token to interact with the blockchain, record transaction history, and own on-chain assets. Control of each token bound account is delegated to the owner of the ERC-721 token, allowing the owner to initiate on-chain actions on behalf of their token.

Token bound accounts are compatible out of the box with nearly all existing infrastructure that supports Ethereum accounts, from on-chain protocols to off-chain indexers. Token bound accounts can own any type of on-chain asset, and can be extended to support new asset types created in the future.

## Important Resources

1. [Official ERC-6551 Link](https://eips.ethereum.org/EIPS/eip-6551)
