Oracle(ORC) - Simple ERC20 Token
Oracle is a simple  ERC20 token smart contract implemmented in Solidity. This Solidity contract allows you to create and implements a basic token called MyToken, with the functionality of minting and burning tokens.The contract is implemented in Solidity, a programming language used for writing smart contracts on the Ethereum blockchain.

Description
Oracle(ORC) - Simple ERC20 Token is a type of cryptocurrency token created using the ERC20 standard on the Ethereum blockchain. ERC20 stands for "Ethereum Request for Comment 20" and is a standard interface for creating tokens on the Ethereum platform. It defines a set of rules and functions that a token must follow to be considered ERC20 compliant.
A Simple ERC20 Token is similar to other ERC20 tokens in that it can be programmed to represent any fungible asset or currency. It can be used for various purposes, such as creating a native currency for a decentralized application (DApp), facilitating tokenized assets, or enabling token-based incentives and rewards in a blockchain ecosystem.
The simplicity of a Simple ERC20 Token lies in its adherence to the ERC20 standard, which provides a basic set of functions like transferring tokens, checking account balances, and approving token allowances. By conforming to this standard, developers can ensure compatibility and interoperability with other ERC20-compatible wallets, exchanges, and smart contracts.
Creating a Simple ERC20 Token typically involves writing and deploying a smart contract on the Ethereum blockchain that defines the token's behavior and attributes, such as its name, symbol, total supply, and decimals. Once deployed, the token can be transferred, bought, sold, or used within the defined parameters of the smart contract and the Ethereum ecosystem.

Getting Started
Executing program
To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., HelloWorld.sol). Copy and paste the following code into the file:

// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

contract MyToken {

// public variables here
string public tokenName = "Oracle";
string public tokenAbbrv = "ORC";
uint public totalSupply = 0;

// mapping variable here
mapping (address => uint) public balances;
// mint function
function mint (address _address, uint _value) public {
    totalSupply += _value;
    balances [_address] += _value;    
}
// burn function
function burn (address _address, uint _value) public {
    if (balances[_address] >= _value){
    totalSupply -= _value;
    balances [_address] -= _value;  
        }   
    }
}
To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.4" (or another compatible version), and then click on the "mytoken.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "mytoken" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by calling the mytoken function. Click on the "mytoken" contract in the left-hand sidebar, and then click on the "mytoken" function.Copy the account and paste under address click transact. You may now check the burn and mint function.You can also call Balances,tokeAbbrv,tokeName and totalSupply function click on the "transact" button to execute the function and retrieve the "mytoken.(constructor)value" message with the status of true Transaction mined and execution succeed.

Authors
Metacrafter rpanado
@metacraftersio

License
This project is licensed under the MIT License - see the LICENSE.md file for details
