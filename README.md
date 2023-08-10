# Custom ERC20 Token Contract

The `CustomToken` contract is an example of an ERC20 token implementation with additional functionalities such as minting, transferring, and burning tokens. It uses the OpenZeppelin library to ensure security and compliance with ERC20 standards.

## Features

- **Minting Tokens**: The contract owner can mint new tokens and allocate them to specified addresses.

- **Transferring Tokens**: Any user can transfer tokens to other addresses.

- **Burning Tokens**: Any user can destroy a certain amount of their own tokens.

## Getting Started

To use the `CustomToken` contract, follow these steps:

1. Compile the Solidity code using a compatible compiler (Solidity version 0.8.0 or higher recommended).

2. Deploy the compiled contract to an Ethereum development environment or testnet.

3. Interact with the deployed contract using transactions to mint, transfer, and burn tokens.

## Contract Functions

### `constructor(string memory _name, string memory _symbol, uint256 initialSupply)`

- Initializes the contract with the specified name, symbol, and initial supply of tokens.
- `_name`: The name of the token.
- `_symbol`: The symbol of the token.
- `initialSupply`: The initial supply of tokens to be minted.

### `mint(address account, uint256 amount)`

- Allows the contract owner to mint new tokens and allocate them to a specified address.
- `account`: The address to which the tokens will be allocated.
- `amount`: The amount of tokens to mint and allocate.

### `transfer(address recipient, uint256 amount)`

- Allows any user to transfer tokens to a specified recipient's address.
- `recipient`: The address to which the tokens will be transferred.
- `amount`: The amount of tokens to transfer.

### `burn(uint256 amount)`

- Allows any user to burn (destroy) a certain amount of their own tokens.
- `amount`: The amount of tokens to burn.

## Usage Examples

```solidity
// Deploy the CustomToken contract
CustomToken contractInstance = new CustomToken("MyToken", "MTK", 1000000);

// Mint new tokens
contractInstance.mint(address1, 5000);

// Transfer tokens
contractInstance.transfer(address2, 2000);

// Burn tokens
contractInstance.burn(1000);
```

## Security Considerations

- Ensure you understand the implications of minting, transferring, and burning tokens.
- Test the contract thoroughly in a development environment before deploying to a production network.

