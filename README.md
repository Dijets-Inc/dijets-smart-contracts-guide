<div align="center">
  <img src="resources/smart-contracts-repo.png?raw=true">
</div>

## Introduction

The goal of this guide is to lay out best practices regarding writing, testing and deployment of smart contracts to Dijets's Utility Chain. We'll be building smart contracts with development environment [Hardhat](https://hardhat.org).

## Prerequisites

### NodeJS and Yarn

First, install the LTS (long-term support) version of [nodejs](https://nodejs.org/en). This is `14.17.0` at the time of writing. NodeJS bundles `npm`.

Next, install [yarn](https://yarnpkg.com):

```zsh
npm install -g yarn
```

### DijetsNodeGo and Dijets-Up

[DijetsNodeGo](https://github.com/Dijets-Inc/dijetsnodego) is an Dijets node implementation written in Go. [Dijets-Up](https://docs.dijets.io/docs/guides/getting-started/tutorials/tools-utilities) is a tool to quickly deploy local test networks. Together, you can deploy local test networks and run tests on them.

### Solidity and Dijets

It is also helpful to have a basic understanding of [Solidity](https://docs.soliditylang.org) and [Dijets](https://docs.dijets.io).

## Dependencies

Clone the [quickstart repository](https://github.com/Dijets-Inc/dijets-smart-contracts-guide/) and install the necessary packages via `yarn`.

```zsh
$ git clone https://github.com/Dijets-Inc/dijets-smart-contracts-guide/.git
$ cd dijets-smart-contracts-guide
$ yarn
```

## Write Contracts

Edit the `Coin.sol` contract in `contracts/`. `Coin.sol` is an [Open Zeppelin](https://openzeppelin.com) [ERC20](https://eips.ethereum.org/EIPS/eip-20) contract. ERC20 is a popular smart contract interface. You can also add your own contracts.

## Hardhat Config

Hardhat uses `hardhat.config.js` as the configuration file. You can define tasks, networks, compilers and more in that file. For more information see [here](https://hardhat.org/config/).

In our repository we use a pre-configured file [hardhat.config.ts](https://github.com/Dijets-Inc/dijets-smart-contracts-guide//blob/main/hardhat.config.ts). This file configures necessary network information to provide smooth interaction with Dijets. There are also some pre-defined private keys for testing on a local test network.

## Hardhat Tasks

You can define custom hardhat tasks in [hardhat.config.ts](https://github.com/Dijets-Inc/dijets-smart-contracts-guide//blob/main/hardhat.config.ts).

## Documentation

There is a documentation under Dijets's official documentation repository:
[Using Hardhat with the Dijets Utility Chain](https://docs.dijets.io/docs/guides/developer-toolchains/hardhat-dijets-uc)