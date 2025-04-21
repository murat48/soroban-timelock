# Timelock Claimable Balance Contract

A simple and functional smart contract implementation for the Soroban platform that demonstrates the "timelock" concept and provides a streamlined "Claimable Balance" mechanism.

### Contract
- Skipping install because wasm already installed
- Using wasm hash ea259882219c262bd32656f94671d05be4734b7ac8a875fdef05bfdc87566418
- Simulating deploy transaction…
- Transaction hash is b4e49a7151b37bb53d30ff0404a9e8183881135006197ddbc5618f9c7a4766c5
- https://stellar.expert/explorer/testnet/tx/b4e49a7151b37bb53d30ff0404a9e8183881135006197ddbc5618f9c7a4766c5
- Signing transaction: b4e49a7151b37bb53d30ff0404a9e8183881135006197ddbc5618f9c7a4766c5
- Submitting deploy transaction…
- https://stellar.expert/explorer/testnet/contract/CASPLM37TLBEKY7EEJ7CIAWCNYLGHF4P2DNCTIHYJNJD6SFPMILW4AXJ
- Deployed!
CASPLM37TLBEKY7EEJ7CIAWCNYLGHF4P2DNCTIHYJNJD6SFPMILW4AXJ

## Overview

This contract allows users to deposit a specified amount of tokens and enables other accounts to claim them either before or after a specific time point. The contract implements a basic timelock mechanism while maintaining a clean and efficient design.

## Features

- Deposit tokens with specified time conditions
- Set multiple claimant addresses (up to 10)
- Two types of time bounds:
  - `Before`: Claimable only before a specified timestamp
  - `After`: Claimable only after a specified timestamp
- Secure authorization checks
- Simple one-time initialization

## Contract Structure

### Data Structures

- **DataKey**: Defines storage keys used in the contract
  - `Init`: Marks the contract as initialized
  - `Balance`: Stores claimable balance information

- **TimeBoundKind**: Specifies the type of time constraint
  - `Before`: Claimable before the timestamp
  - `After`: Claimable after the timestamp

- **TimeBound**: Combines the time bound type and its timestamp
  - `kind`: The type of time bound
  - `timestamp`: The specific timestamp value

- **ClaimableBalance**: Stores all details of the claimable balance
  - `token`: Address of the token
  - `amount`: Token amount
  - `claimants`: List of addresses that can claim the balance
  - `time_bound`: Time condition for claiming

## Technical Details

- Built using the Soroban SDK for Stellar's smart contract platform
- Implemented with `#![no_std]` for efficient operation in blockchain environments
- Uses Rust's type system for safety and reliability

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.
