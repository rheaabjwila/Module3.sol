# Module3.sol
# ETH Proof: Beginner Course (Final Assessment Project)

Simple overview of use/purpose:

Eth Proof: is a blockchain-based computing platform that enables developers build and deploy decenralized applications.
We can use this as a useful program for minting or burning of tokens and NFT's.

## Description

ETH Proof is also connected into one example of a program that is called Solidity, 
it is a object-oriented programming language for implementing smart contracts on various blockchain platforms, most notably, the Ethereum.
It is especifically by the Ethereum Network team for constructing and designing on Blockchain platforms. 
Also, this program is the best choice to use when it comes to minting and burning of tokens in solidity programming.

## Getting Started

### Executing program

* How to run the program? to run this program, one of the best choice to use is Remix, an example of an online compiler that is compatible in Solidity Program.
Just go to their website https://remix.ethereum.org/.

* Step-by-step bullets

Steps of how I run this code;

* To run your code in this program, first is that use a compiler that is compatible to solidity and one example that you can use is Remix IDE.
* First step to run this code is go to Remix home, create a new file and rename that file any name that you want but do not forget to put .sol in the end.
* Second step is putting the code and checking the code if there is an error. You will see a red exclamation mark to those lines that have an error,
  so you will notice that there's an typo that need to be corrected.
* After checking the code click the solidity compiler and click the (blue box) with Compile and your file name inside. 
  And when a green check pop-up, it means that your code is correct.
* Next step is click the Deploy and Run Transactions which is you will see the output of your code. 
```

//SPDX-License-Identifier: MIT
pragma solidity ^0.8.18;

contract MyToken {

    // public variables here
    string public tokenName = "rhea";
    string public tokenAbbrv = "abjwila";
    uint public totalSupply;

    // mapping variable here
    mapping(address => uint) public balances;

    // mint function
    function mint (address _address, uint _value) public {
        totalSupply += _value;
        balances [_address] += _value;
    }

    // burn function
    function burn (address _address, uint _value) public {
        if (balances[_address] >= _value) {
            totalSupply -= _value;
            balances[_address] -= _value;
        }
    }
}
```

## Authors

Creator: Rhea Polteros Abjwila

Email: 8215057@ntc.edu.ph

Instagram:@Suapaaaao

Facebook: Rheaabjwila@yahoo.com

## License

This project is licensed under the [MIT] License - see the LICENSE.md file for details
