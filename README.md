# Project: Create a Token

 in this project I have created a token named my token which have mint and burn function. In this token contract I have defind the total suplay for the token and the short hand form for the token.
 
       REQUIREMENTS
    1. Your contract will have public variables that store the details about your coin (Token Name, Token Abbrv., Total Supply)
    2. Your contract will have a mapping of addresses to balances (address => uint)
    3. You will have a mint function that takes two parameters: an address and a value. 
       The function then increases the total supply by that number and increases the balance 
       of the “sender” address by that amount
    4. Your contract will have a burn function, which works the opposite of the mint function, as it will destroy tokens. 
       It will take an address and value just like the mint functions. It will then deduct the value from the total supply 
       and from the balance of the “sender”.
    5. Lastly, your burn function should have conditionals to make sure the balance of "sender" is greater than or equal 
       to the amount that is supposed to be burned.

## Getting Started

# Overview

The MyToken smart contract is a simple implementation of an ERC20-like token on the Ethereum blockchain. It allows for minting and burning tokens, tracking the total supply, and maintaining balances of addresses.

# Contract Details

    Token Name: MyToken
    Token Abbreviation: MT
    Total Supply: 1,000,000 MT (initial supply)


### Installing

* use the git command to install the programe localy 

        git clone https://github.com/surafeldev/soltasks/blob/main/mytoken.sol

* Any modifications needed to be made to files/folders

## Features

    1, Public Variables:

        tokenName: Stores the name of the token.
        tokenAbbrv: Stores the abbreviation of the token.
        totalSupply: Stores the total supply of the token.

    2, Mapping:

        balances: Maps addresses to their respective token balances.

    3, Mint Function:

        Takes two parameters: an address and a value.

        Increases the total supply by the given value.

        Increases the balance of the specified address by the given value.

    4, Burn Function:

        Takes two parameters: an address and a value.
        Decreases the total supply by the given value if the address balance is greater than or equal to the value.
        Decreases the balance of the specified address by the given value if the address balance is greater than or equal to the value.

# Functions

mint(address _address, uint256 _value)
Increases the total supply and the balance of the specified address.

    function mint(address _address, uint256 _value) public {
        totalSupply += _value;
        balances[_address] += _value;   
    }

burn(address _address, uint256 _value)
Decreases the total supply and the balance of the specified address if the balance is sufficient.

    function burn(address _address, uint256 _value) public {
    if (balances[_address] >= _value) {
        totalSupply -= _value;
        balances[_address] -= _value;
    }
    }

Usage
Minting Tokens
To mint new tokens, call the mint function with the recipient address and the amount of tokens to be minted.

Example:

    mint(0xRecipientAddress, 1000);

# Burning Tokens

To burn tokens, call the burn function with the holder's address and the amount of tokens to be burned.

Example:

    burn(0xHolderAddress, 500);

## Authors

Surafel Nigusie

[@nigusesurafel](https://x.com/NiguseSurafel?t=8gJm0F0rEzZ5CcCIzWIDfg&s=09)
