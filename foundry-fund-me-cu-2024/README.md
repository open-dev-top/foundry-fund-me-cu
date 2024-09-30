## 4 types of testing

1. Unit: Testing a single function
2. Integration: Testing multiple functions
3. Forked: Testing on a forked network
4. Staging: Testing on a live network (testnet or mainnet)

## Use Fork test on Sepolia Testnet

```
forge test --match-test testPriceFeedVersionIsAccurate -vvvvv --fork-url $SEPOLIA_RPC_URL
```

```
forge coverage -vvvvv --fork-url $SEPOLIA_RPC_URL
```

## Others

```
forge snapshot --match-test testWithdrawWithFromMultipleFunders

forge snapshot
```

```
forge inspect FundMe storageLayout
```

```
anvil

forge script script/DeployFundMe.s.sol --fork-url http://127.0.0.1:8545 --private-key 0xac0974bec39a17e36ba4a6b4d238ff944bacb478cbed5efcae784d7bf4f2ff80 --broadcast

cast storage 0xe7f1725E7734CE288F8367e1Bb143E90bb3F0512 2

forge script script/Interactions.s.sol:FundFundMe --fork-url http://127.0.0.1:8545 --private-key 0xac0974bec39a17e36ba4a6b4d238ff944bacb478cbed5efcae784d7bf4f2ff80 --broadcast
```

## Foundry

**Foundry is a blazing fast, portable and modular toolkit for Ethereum application development written in Rust.**

Foundry consists of:

- **Forge**: Ethereum testing framework (like Truffle, Hardhat and DappTools).
- **Cast**: Swiss army knife for interacting with EVM smart contracts, sending transactions and getting chain data.
- **Anvil**: Local Ethereum node, akin to Ganache, Hardhat Network.
- **Chisel**: Fast, utilitarian, and verbose solidity REPL.

## Documentation

https://book.getfoundry.sh/

## Usage

### Build

```shell
$ forge build
```

### Test

```shell
$ forge test
```

### Format

```shell
$ forge fmt
```

### Gas Snapshots

```shell
$ forge snapshot
```

### Anvil

```shell
$ anvil
```

### Deploy

```shell
$ forge script script/Counter.s.sol:CounterScript --rpc-url <your_rpc_url> --private-key <your_private_key>
```

### Cast

```shell
$ cast <subcommand>
```

### Help

```shell
$ forge --help
$ anvil --help
$ cast --help
```
