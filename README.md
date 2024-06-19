
ETH PROOF: Beginner EVM Course

The Ethereum blockchain is programmable, enabling limitless potential. Programmers use the Solidity programming language to build applications for Ethereum. Ethereum Virtual Machines, or EVMs, are used as the foundation for a variety of blockchains. In this course, we will take you from basic coding knowledge to a beginner Solidity developer

DESCRIPTION

In this project we will have public variables that stores the details about your (Token name, Token Abbreviation, Total supply. Our contract will have a mapping of address to balances (address => uint) we will have a mint function that takes two paramemteres an address and a value . The function then increase the total supply number and increase the balance of the address by the amount. Our contract will have a burn function,which works the opposite of the mint function,as it will destroytokens.It will take an address and value just like the mint function.It will then deduct the value the total supply and from the balance of the amount.

CODE

// SPDX-License-Identifier: MIT pragma solidity 0.8.18;

/* REQUIREMENTS 1. Your contract will have public variables that store the details about your coin (Token Name, Token Abbrv., Total Supply) 2. Your contract will have a mapping of addresses to balances (address => uint) 3. You will have a mint function that takes two parameters: an address and a value. The function then increases the total supply by that number and increases the balance of the “sender” address by that amount 4. Your contract will have a burn function, which works the opposite of the mint function, as it will destroy tokens. It will take an address and value just like the mint functions. It will then deduct the value from the total supply and from the balance of the “sender”. 5. Lastly, your burn function should have conditionals to make sure the balance of "sender" is greater than or equal to the amount that is supposed to be burned. */

contract MyToken {

// public variables here
string public tokenName = "META";
string public tokenAbbrv = "MTA";
uint public totalsupply = 0;

// mapping variable here
mapping (address => uint) public balances;

// mint function
function mint (address _address, uint _value) public {
    totalsupply += _value;
    balances[_address] += _value;  
}

// burn function
function burn (address _address, uint _value) public {
    if (balances [_address] >= _value) {
       totalsupply -= _value;
       balances[_address] -= _value;  
    }
}
}

CODE EXPLANATION

Here we create a string variable for those and it says to make it public and we'll call this Token name And then the same thing for our abbreviation,

So we'll go ahead and plug that is as well,and then we will call this total supply and we'll give it an initial supply of zero.

So for number two, your contact will have a mapping of address to balances,and look like we're gonna be mapping address public

So it is easier to check our work later when we're demoing this.

So what this is gonna do if you pass an address into here, since every address is associated with a U end,when you give it the address,its gonna return the token amount that address.

So number three we have mint function that takes two parameter An address and a value. the function increase the total supply by that number and increases the balance by that amount.

So our next requirement is our Contract will have a burn function,which works the opposite of mint function as it will destroy tokens it will take an address in value, just like the mint function it will deduct the value from total supply and from the balance of the address.

And lastly ,our burn function should have a conditional to make sure the balance of account is greater than or equal to amount.

Executing program

To run this program, we can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

once our contact will deployed ,we will interact it with put the value in function and check the increasing or decreasing of mint function and burn function

Authors

@Anishakki01

LICENCE

// SPDX-License-Identifier: MIT
