# kichain-t-2

Thank you for submitting a gentx!
This guide will provide instructions to setup your validator for the testnet challenge.

**Please have your validator up and ready by August 18 2021, at 13:00 UTC.**

## TLDR

On this repository, you can find:
- [the genesis file](./genesis.json) (hash: `ae0e4eeb6aebb0bcb0356279d851b2ddd5631a678045da1d2cd0592146d6f1b6`)
- [peers](./peer-nodes.txt)
- [seeds](./seed-nodes.txt)

## Start your node

This guide assumes that you have followed the step from our [tutorial](https://github.com/KiFoundation/ki-testnet-challenge/blob/main/tutorials/gentx.md). Otherwise, please adapt commands according to your setup.

To download the Genesis:
```
curl https://raw.githubusercontent.com/KiFoundation/ki-networks/v0.1/Testnet/kichain-t-2/genesis.json > ./kid/config/genesis.json
```
```
sha256sum ./kid/config/genesis.json
ae0e4eeb6aebb0bcb0356279d851b2ddd5631a678045da1d2cd0592146d6f1b6  ./kid/config/genesis.json
```

You can find persistent peers (and add your own if you want) in [this file](./peer-nodes.txt)

To launch your node:
```
kid start --home ./kid/ &> ./kilogs/ki-node.log &
```

If you need any help, please ask on Discord