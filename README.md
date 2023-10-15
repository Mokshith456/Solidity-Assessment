# Solidity-Assessment

# MyToken Smart Contract

This project is the first step for beginners in comprehending and understanding the working of functions, datatypes, loops, etc. in solidity and using these basics to create a token.

# Description

This is a simple program whuch is written in solidity that is used in creating smart contracts in Etherium based blockchain. In this prograsm we have created a token named LCOIN and given it an abbriviating and total supply value. Here, we use two functions, burn an mint functions, which are used to burn or mint the tokens that we have created int balances of th total supply of the account. This program is a very simple representation of ho to create a token using solidity.

## Get Started

Run the following program on a online IDE which supports solidiy ,  you can use REMIX which is an online IDE which allows you to code in solidity and deploy your smart contract.
You can simply visit https://remix.ethereum.org/. You can create a new file and copy paste the following code and deploy it.
You can use this code template to make your own token.

    // public variables here
     string public tokenName = "LCOIN";
     string public tokenAbbriv = "LCN";
     uint public totalSupply = 250;
    // mapping variable here
     mapping(address => uint) public balances;
    // mint function
     function mint (address accntaddr, uint val) public {
        totalSupply += val;
        balances[accntaddr] += val;
     }
    // burn function
       function burn (address accntaddr, uint val) public {
        if(balances[accntaddr]>= val){
        totalSupply -= val;
        balances[accntaddr] -= val;
         }
     }
You may compile the code simply by clicking Ctrl+S , then you can deploy the smart contract by clicking the deploy option on the lift sde of your screen. Once the smart contract is deployed you may give the parameters to the fuctions and play around and check how the code works.

## Authors

Mokshith P @mokshithlucky06@gmail.com

## License

This smart contract is licensed under the [MIT License](LICENSE). See the [`LICENSE`](LICENSE) file for more details.
