# Solidity-Assessment

# MyToken Smart Contract

This project is the first step for beginners in comprehending and understanding the working of functions, datatypes, loops, etc. in solidity and using these basics to create a token.

# Description


\ function with the target address and the number of tokens to burn:

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
