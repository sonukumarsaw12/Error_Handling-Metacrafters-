
# Error Handling Smart Contract : Statement & Implementation

This is Solidity Project "Error Handling : require(), assert() and revert() statements.


## Problem Statement
write a smart contract that implements the require(), assert() and revert() statements.
## Description

In solidity Error Handling their are three statement:

require(): Used to validate inputs and conditions before executing code.

assert(): Used to check for conditions that should never be false.It is typically used to check for invariants.
       
revert(): Used to handle situations where an error needs to be flagged and the current transaction should be reverted.
## Getting Started
## Executing Program
First to open any Browser and to open Remix IDE, it's an online Solidity Platform. link - https://remix.ethereum.org/.

then create a new file and file extension is .sol and save it. then copy and paste the code into the file:


## Running Tests

To run tests, run the following command

```

// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

//  write a smart contract that implements the require(), assert() and revert() statements.

/*     require(): Used to validate inputs and conditions before executing code.
       assert(): Used to check for conditions that should never be false. 
                 It is typically used to check for invariants.
       revert(): Used to handle situations where an error needs to be flagged 
                 and the current transaction should be reverted.
*/

contract Error_Handling {
       uint public value;


       function setValue(uint _value) public {
              require(_value > 0, "value must be greater then 0.");

              assert(_value != value);

              value = _value;
       }

       function perfomeDiv(uint _numerator, uint _denominator) public pure returns (uint){
              require(_denominator !=0, "cannot div by zero");

              if(_numerator % _denominator !=0)
              {
                     revert("numerotor must be div by donominator");
              }

              return _numerator / _denominator;     
       }


       
}

```
## Authors
Sonu Kumar Saw


## License
This project is licensed under the MIT License- see the LICENSE file for details.
