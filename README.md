# Solidity-Assessment

# MyToken Smart Contract

This repository contains a Solidity smart contract for a custom token called "MyToken." The contract implements functionality to mint and burn tokens based on specified requirements.

## Requirements

1. The contract maintains public variables to store essential details about the token, including:
   - Token Name: `tokenName`
   - Token Abbreviation: `tokenAbbriv`
   - Total Supply: `totalSupply`

2. A mapping of addresses to balances is utilized to store the token balances of each address: `balances`

3. **Mint Function:**
   - A function named `mint` is implemented, taking two parameters:
     - `accntaddr`: The address to mint tokens to
     - `val`: The value (number of tokens) to mint
   - The `mint` function increases the total supply by the specified value and increments the balance of the specified address by that amount.

4. **Burn Function:**
   - A function named `burn` is implemented, taking two parameters:
     - `accntaddr`: The address from which tokens will be burned
     - `val`: The value (number of tokens) to burn
   - The `burn` function decreases the total supply by the specified value and deducts the value from the balance of the specified address.

5. The `burn` function includes conditionals to ensure that the balance of the specified address is greater than or equal to the amount intended to be burned.

## Usage

To interact with this smart contract and utilize the mint and burn functions, deploy it on the Ethereum blockchain using a compatible Ethereum development environment.

### Minting Tokens

To mint new tokens, call the `mint` function with the target address and the number of tokens to mint:

```solidity
function mint(address accntaddr, uint val) public {
    totalSupply += val;
    balances[accntaddr] += val;
}
```

### Burning Tokens

To burn existing tokens, call the `burn` function with the target address and the number of tokens to burn:

```solidity
function burn(address accntaddr, uint val) public {
    if (balances[accntaddr] >= val) {
        totalSupply -= val;
        balances[accntaddr] -= val;
    }
}
```

Ensure that the balance of the specified address is sufficient to perform the burn operation.

## License

This smart contract is licensed under the [MIT License](LICENSE). See the [`LICENSE`](LICENSE) file for more details.
