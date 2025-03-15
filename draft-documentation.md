# Cardano-CLI Documentation Draft

## Overview

The cardano-cli is the command-line interface (CLI) tool for interacting with the Cardano blockchain, a secure and scalable platform for decentralized applications (dApps) and smart contracts. This tool enables users to perform a wide range of operations on the Cardano blockchain, including key management, transaction processing, stake delegation, and querying blockchain data.

## Key Features

Payment Key Management: Create and manage payment keys for secure transactions.

Transaction Handling: Send and receive ADA (Cardano’s native cryptocurrency).

Stake Delegation: Delegate stake to participate in Cardano’s proof-of-stake (PoS) consensus mechanism.

Blockchain Queries: Retrieve blockchain data, such as transaction history, stake pool information, and network status.

Smart Contract Interaction: Interact with Plutus smart contracts and Marlowe financial contracts.

## Getting Started

1. Downloading Binaries
   Compatible Versions: Download the latest cardano-cli binaries compatible with specific versions of cardano-node from the Cardano Node Release Notes.

All Versions: Access binaries for all versions of cardano-cli from the Cardano-CLI Release Notes.

2. Installation
   Ensure cardano-node is installed and running.

Place the cardano-cli executable in your system’s PATH for easy access.

Command Reference
For a comprehensive list of commands and their options, refer to the following resources:

Command List: List of All Commands

Command Options: Description of Command Options

Development Documentation
Cardano Node Wiki: Detailed development documentation is available in the Cardano Node Wiki.

Haddock Documentation: Explore the Haddock documentation for cardano-cli at Haddock Docs.

Contributing
We welcome contributions to the cardano-cli repository! To get started:

Review the Contributing Guide.

Fork the repository and create a new branch for your changes.

Submit a pull request with a detailed description of your contribution.

Example Commands
Here are some common cardano-cli commands to get you started:

1. Generate Payment Keys
   bash
   Copy
   cardano-cli address key-gen \
    --verification-key-file payment.vkey \
    --signing-key-file payment.skey
2. Create a Wallet Address
   bash
   Copy
   cardano-cli address build \
    --payment-verification-key-file payment.vkey \
    --out-file payment.addr \
    --mainnet
3. Query Blockchain Data
   bash
   Copy
   cardano-cli query tip --mainnet
4. Send ADA
   bash
   Copy
   cardano-cli transaction build \
    --tx-in <input-utxo> \
    --tx-out <recipient-address>+<amount-in-ada> \
    --change-address <your-address> \
    --mainnet \
    --out-file tx.raw
5. Delegate Stake
   bash
   Copy
   cardano-cli stake-address delegation-certificate \
    --stake-verification-key-file stake.vkey \
    --stake-pool-id <pool-id> \
    --out-file delegation.cert
   Support and Community
   GitHub Issues: Report bugs or request features in the GitHub Issues section.

Cardano Forum: Join the Cardano Forum for discussions and support.

Discord: Engage with the community on the Cardano Discord.

Conclusion
The cardano-cli is a powerful tool for interacting with the Cardano blockchain, offering a wide range of functionalities for developers and users alike. Whether you’re managing keys, sending transactions, or interacting with smart contracts, cardano-cli provides the flexibility and control needed to build on Cardano.

For more information, explore the official documentation and join the Cardano community to stay updated on the latest developments. Happy building!
