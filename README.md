# Crowdfunding
The react code resides in the client folder.

```
npx thirdweb@latest create --contract
```

This intialises a CLI that asks us questions and then set up the environment for us.

```
cd web3
npm install dotenv
```

Dotenv is an npm package that can be added to any NodeJs application. The main purpose of the Dotenv package is to allow developers to create a . env file that has custom environment files that are added into the process. [[1]](#1)

#### Smart Contracts
Smart contracts are simply programs stored on a blockchain that run when predetermined conditions are met. They typically are used to automate the execution of an agreement so that all participants can be immediately certain of the outcome, without any intermediary's involvement or time loss. [[2]](#2)

### Testnet
Testnets are used by developers to ensure that the smart contracts and dApps (Decentralized Applications) they deploy are functional and secure.  [[10]](#10)

<b>Note</b>: Goerli will be deprecated in Q1 2023 but will be supported until Q4 2023, so developers and users should migrate to Sepolia for testing and development purposes. [[11]](#11)

### RPC
Remote Procedure Call is a software communication protocol that one program can use to request a service from a program located in another computer on a network without having to understand the network's details. [[12]](#12)

#### Solidity
- Solidity is a statically-typed curly-braces programming language designed for developing smart contracts that run on Ethereum. [[3]](#3)
-  A struct is a creative data structure format in Solidity where variables of diverse data types can be bundled into one variable or a custom-made type. [[4]](#4)

```solidity
struct Person {
    string name;
    uint age;
    string address;
}
```

- An unsigned integer, declared with the uint keyword, is a value data type that must be non-negative; that is, its value is greater than or equal to zero. [[5]](#5)
- Mappings in Solidity are hash tables that store data as key-value pairs, where the key can be any of the built-in data types supported by Ethereum.  [[6]](#6)

```solidity
mapping (address => uint) public balances;
```

- In Solidity, we use the memory keyword to store the data temporarily during the execution of a smart contract. When a variable is declared using the memory keyword, it is stored in the memory area of the EVM Ethereum Virtual Machine . This is the default storage location for variables in Solidity. [[7]](#7)

- When writing a smart contract, you need to ensure that money is being sent to the contract and out of the contract as well. Payable does this for you, any function in Solidity with the modifier Payable ensures that the function can send and receive Ether. [[8]](#8)

```solidity
function receiveEther() public payable {
    // do something with the received Ether
}
```

- In Solidity, a function that only reads but doesn't alter the state variables defined in the contract is called a View Function. [[9]](#9)

```solidity
pragma solidity ^0.8.0;

contract MyContract {
  uint256 public myNumber = 42;

  function getNumber() public view returns (uint256) {
    return myNumber;
  }
}
```

## References
<a id="1">[1]</a> https://www.mickpatterson.com.au/blog/how-to-use-environment-variables-in-nodejs-with-express-and-dotenv#:~:text=Dotenv%20is%20an%20npm%20package,are%20added%20into%20the%20process.

<a id="2">[2]</a> https://www.ibm.com/in-en/topics/smart-contracts#:~:text=Next%20Steps-,Smart%20contracts%20defined,intermediary's%20involvement%20or%20time%20loss.

<a id="3">[3]</a> https://soliditylang.org/

<a id="4">[4]</a> https://www.alchemy.com/overviews/solidity-struct#:~:text=robust%20smart%20contracts.-,What%20is%20a%20Solidity%20struct%3F,subsets%20of%20variables%20in%20it.

<a id="5">[5]</a> https://blog.logrocket.com/ultimate-guide-data-types-solidity/#:~:text=An%20unsigned%20integer%2C%20declared%20with,up%20to%2032B%20by%20default.

<a id="6">[6]</a> https://www.alchemy.com/overviews/solidity-mapping#:~:text=Mappings%20in%20Solidity%20are%20hash,understand%20when%20learning%20Solidity%20development.

<a id="7">[7]</a> https://www.educative.io/answers/what-is-the-memory-keyword-in-solidity#:~:text=In%20Solidity%2C%20we%20use%20the,location%20for%20variables%20in%20Solidity.

<a id="8">[8]</a> https://codedamn.com/news/solidity/payable-function-in-solidity-example-how-to-use-it#:~:text=What%20is%20Payable%20in%20Solidity,can%20send%20and%20receive%20Ether.

<a id="9">[9]</a> https://www.educative.io/answers/what-is-a-view-function-in-solidity#:~:text=In%20Solidity%2C%20a%20function%20that,%2Fover%2Dwrite%20state%20variables.

<a id="10">[10]</a> https://www.alchemy.com/overviews/what-are-testnets#:~:text=Testnets%20are%20used%20by%20developers,operate%20on%20a%20separate%20ledger.

<a id="11">[11]</a> https://www.quicknode.com/guides/ethereum-development/getting-started/goerli-vs-sepolia-a-head-to-head-comparison/#:~:text=Goerli%20is%20one%20of%20the,for%20testing%20and%20development%20purposes.

<a id="12">[12]</a> https://www.techtarget.com/searchapparchitecture/definition/Remote-Procedure-Call-RPC#:~:text=Remote%20Procedure%20Call%20is%20a,systems%20like%20a%20local%20system.
