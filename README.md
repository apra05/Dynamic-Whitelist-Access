# Dynamic Whitelist Access

## Overview
The **Dynamic Whitelist Access** smart contract allows users to be dynamically added to a whitelist before an automated closing time. This contract is designed to ensure that only approved users gain access before the deadline.

## Features
- **Dynamic Whitelisting**: Users can be added to the whitelist before the closing time.
- **Automated Closing**: The contract automatically stops accepting new whitelist entries after a fixed duration (e.g., 7 days).
- **Minimal Deployment**: No constructor or input parameters are required at deployment.
- **Efficient Access Control**: Users can verify if they are whitelisted through a simple function call.
- **Immutable Closing Time**: The closing time is hardcoded and cannot be altered after initialization.

## Deployment Details
- **Deployed Address**: `0x74EBf615acd688d9EaB2f65004654bE441e9C039`
- **Blockchain**: Edu Chain

## Functions
### `init()`
Initializes the contract by setting the closing time. Can only be called once.

### `addToWhitelist(address user)`
Allows users to be added to the whitelist before the deadline.

### `isWhitelisted(address user) → bool`
Returns `true` if the given address is whitelisted.

## How It Works
1. The contract is deployed with a **predefined closing time** (e.g., 7 days from initialization).
2. Users can be **added dynamically** to the whitelist before the deadline.
3. Once the **closing time is reached**, new additions are blocked.
4. Anyone can check if an address is **whitelisted** using `isWhitelisted()`.

## License
This project is licensed under the MIT License.

---

