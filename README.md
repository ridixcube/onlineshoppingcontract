# ShoppingToken Contract

## Overview
The `ShoppingToken` contract is a basic implementation of a token on the Ethereum blockchain. It allows for minting (creating) and burning (destroying) tokens, managing balances, and keeping track of the total token supply.

## Requirements
1. **Token Details**: The contract stores information about the token, including its name (`Name`), identifier (`ID`), and total supply (`points`).
2. **Balance Mapping**: It uses a mapping (`balances`) to track token balances for each address.
3. **Mint Function**: Allows increasing the total supply and adding tokens to a specific address.
4. **Burn Function**: Allows decreasing the total supply and removing tokens from a specific address, with checks to ensure the address has sufficient balance.
5. **Security**: The burn function includes a conditional check to prevent burning more tokens than the sender owns.

## Contract Details
### Variables
- `Name`: A public string variable representing the name of the token.
- `ID`: A public string variable representing an identifier or abbreviation for the token.
- `points`: A public uint variable representing the total supply of tokens.

### Functions
- **Constructor**: Initializes the token with a name, identifier, and initial supply.
- **mint**: Function to mint new tokens to a specified address. Increases total supply and recipient's balance.
- **burn**: Function to burn tokens from a specified address. Decreases total supply and sender's balance, with a check to prevent over-burning.

### Usage
To use this contract:
1. Deploy it on an Ethereum-compatible blockchain.
2. Upon deployment, provide values for `_name`, `_ID`, and `_initialSupply` to initialize the token details.
3. Use the `mint` function to add tokens to specific addresses.
4. Use the `burn` function to remove tokens from specific addresses, ensuring the sender has enough tokens to burn.

### SPDX License Identifier
This contract uses the SPDX License Identifier `MIT`, meaning it is licensed under the MIT License.

### Solidity Version
The contract is implemented in Solidity version `0.8.18`.

## Author
This project is made by Riddhima Langer, student of BE-CSE at Chandigarh University.
