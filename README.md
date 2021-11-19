# Chainlink <> Arbitrum

This project demonstrates how to use Chainlink Price Feeds on Arbitrum Rinkeby Testnet Rollup.

## Getting started

### Prerequisites

Be sure to have installed the following

- [Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
- [Node.js](https://nodejs.org/en/download/)
- [Yarn](https://yarnpkg.com/getting-started/install) 

### Installation

1) Clone the repo
```
git clone https://github.com/andrejrakic/chainlink-arbitrum.git
cd chainlink-arbitrum
```
2) Install packages
```
yarn install
```
3) Compile contracts
```
npx hardhat compile
```

Additionally, try running some of the following tasks:

```shell
npx hardhat accounts
npx hardhat compile
npx hardhat clean
npx hardhat test
npx hardhat node
npx hardhat help
REPORT_GAS=true npx hardhat test
npx hardhat coverage
npx hardhat run scripts/deploy.ts
TS_NODE_FILES=true npx ts-node scripts/deploy.ts
npx eslint '**/*.{js,ts}'
npx eslint '**/*.{js,ts}' --fix
npx prettier '**/*.{json,sol,md}' --check
npx prettier '**/*.{json,sol,md}' --write
npx solhint 'contracts/**/*.sol'
npx solhint 'contracts/**/*.sol' --fix
```

## Deployment

In this project, copy the .env.example file to a file named .env, and then edit it to fill in the details. Enter your Chainlink Rinkeby node URL (eg from Alchemy), and the private key of the account which will send the deployment transaction.

```shell
hardhat run --network arbitrum_rinkeby scripts/deploy.ts
```

## Arbiscan verification

Enter your Arbiscan API key in .env file. Then, copy the deployment address and paste it in to replace `DEPLOYED_CONTRACT_ADDRESS` in this command:

```shell
npx hardhat verify --network arbitrum_rinkeby DEPLOYED_CONTRACT_ADDRESS 
```
