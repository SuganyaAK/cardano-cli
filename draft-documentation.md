# Cardano-CLI Documentation Draft

## Overview

The cardano-cli is the command-line interface (CLI) tool for interacting with the Cardano blockchain, a secure and scalable platform for decentralized applications (dApps) and smart contracts. This tool enables users to perform a wide range of operations on the Cardano blockchain, including key management, transaction processing, stake delegation, and querying blockchain data.

## Key Features

**Payment Key Management**: Create and manage payment keys for secure transactions.

**Transaction Handling**: Send and receive ADA (Cardano’s native cryptocurrency).

**Stake Delegation**: Delegate stake to participate in Cardano’s proof-of-stake (PoS) consensus mechanism.

**Blockchain Queries**: Retrieve blockchain data, such as transaction history, stake pool information, and network status.

**Smart Contract Interaction**: Interact with Plutus smart contracts and Marlowe financial contracts.

## Getting Started

1.**Download Binaries**

- **Compatible Versions**: Download the latest cardano-cli binaries compatible with specific versions of cardano-node from [cardano-node's release notes](https://github.com/IntersectMBO/cardano-node/releases).

- **All Versions**: Access binaries for all versions of `cardano-cli` from [cardano-cli's release notes](https://github.com/IntersectMBO/cardano-cli/releases).

  2.**Installation**

- Ensure cardano-node is installed and running.

- Place the cardano-cli executable in your system’s PATH for easy access.

## Command Reference

For a comprehensive list of commands and their options, refer to the following resources:

Command List: [List of all commands](cardano-cli/test/cardano-cli-golden/files/golden/help.cli)

Command Options: [Description of each command's options](cardano-cli/test/cardano-cli-golden/files/golden/help)

Development Documentation : [Cardano Node Wiki](https://github.com/input-output-hk/cardano-node-wiki/wiki).

Haddock Documentation: [Haddock Documentation](https://cardano-cli.cardano.intersectmbo.org/)

## Example Commands

Here are some common cardano-cli commands to get you started:

1. Generate Payment Keys
   ```bash
   cardano-cli address key-gen \
    --verification-key-file payment.vkey \
    --signing-key-file payment.skey
   ```
2. Create a Wallet Address
   ```bash
   cardano-cli address build \
    --payment-verification-key-file payment.vkey \
    --out-file payment.addr \
    --mainnet
   ```
3. Query Blockchain Data
   ```bash
   cardano-cli query tip --mainnet
   ```
4. Send ADA
   ```bash
   cardano-cli transaction build \
    --tx-in <input-utxo> \
    --tx-out <recipient-address>+<amount-in-ada> \
    --change-address <your-address> \
    --mainnet \
    --out-file tx.raw
   ```
5. Delegate Stake
   ```bash
   cardano-cli stake-address delegation-certificate \
    --stake-verification-key-file stake.vkey \
    --stake-pool-id <pool-id> \
    --out-file delegation.cert
   ```

## Support and Community

- GitHub Issues: Report bugs or request features in the [GitHub Issues section](https://github.com/IntersectMBO/cardano-cli/issues).

- Discord: Engage with the community on the Cardano Discord [Dev Ex Working Group](https://discord.com/channels/1136727663583698984/1250047836339306526)

## Contributing

We welcome contributions to the cardano-cli repository!
To get started:

- Review the [Contributing guide](CONTRIBUTING.md).

- Fork the repository and create a new branch for your changes.

- Submit a pull request with a detailed description of your contribution.

## Conclusion

The cardano-cli is a powerful tool for interacting with the Cardano blockchain, offering a wide range of functionalities for developers and users alike. Whether you’re managing keys, sending transactions, or interacting with smart contracts, cardano-cli provides the flexibility and control needed to build on Cardano.

For more information, explore the official documentation and join the Cardano community to stay updated on the latest developments. Happy building!
