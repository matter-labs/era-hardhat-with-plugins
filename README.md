# zkSync Hardhat project with plugins

## hardhat-deploy

For this plugin you need to configure your accounts in the .env file. `zksync-web3` is integrated in hardhat-deploy so there's no need to use the `Deployer` class from `hardhat-zksync-deploy`. Check deployment script `001-deploy-greeter.ts` file for reference.

Run `npx hardhat deploy --network zkSyncTestnet` 

Creates the `deployments` folder and saves info in different files so deployments can be cached and re-run.

## hardhat-contract-sizer

Creates a report of the contract bytecode size on compilation time.

`yarn hardhat compile`

## @typechain/hardhat

Creates Typescript type definitions in the `/typechain` folder. Runs on compilation.

## hardhat-abi-exporter

Exports contract ABI files to the `/abis` folder. Runs on compilation.


---

This project was scaffolded with [zksync-cli](https://github.com/matter-labs/zksync-cli).



### Environment variables

In order to prevent users to leak private keys, this project includes the `dotenv` package which is used to load environment variables. It's used to load the wallet private key, required to run the deploy script.

To use it, rename `.env.example` to `.env` and enter your private key.

```
WALLET_PRIVATE_KEY=123cde574ccff....
```

### Local testing

In order to run test, you need to start the zkSync local environment. Please check [this section of the docs](https://v2-docs.zksync.io/api/hardhat/testing.html#prerequisites) which contains all the details.

If you do not start the zkSync local environment, the tests will fail with error `Error: could not detect network (event="noNetwork", code=NETWORK_ERROR, version=providers/5.7.2)`

## Official Links

- [Website](https://zksync.io/)
- [Documentation](https://v2-docs.zksync.io/dev/)
- [GitHub](https://github.com/matter-labs)
- [Twitter](https://twitter.com/zksync)
- [Discord](https://discord.gg/nMaPGrDDwk)
