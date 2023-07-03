# MyToken 

This is a straightforward ERC-20 token contract written in Solidity. The contract provides for the generation and destruction of tokens, as well as the storage of token information.

## Prerequisites

1. The contract has public variables that contain information about the coin:
   - 'tokenName': A string providing the token's name.
   - 'abbrv': A string encoding the token's abbreviation.
   - 'totalSupply': An unsigned integer indicating the token's total supply.


2. The contract has an address-to-balance mapping:
   - 'balances' A mapping that connects addresses to their respective token balances.

3. The contract has a'mint' function that adds a specified amount to the total supply and balance of the "sender" address:
   - Settings:
     - '_address': The location where the tokens will be minted.
     - '_value': The number of tokens to be produced.
   - Actions: 'totalSupply' should be increased by '_value'.
     - Increase the '_address' balance by '_value'.


4. The contract has a 'burn' function that reduces the total supply and balance of the "sender" address by a specified amount:
   - Settings:
     - '_address': The location where the tokens will be destroyed.
     - '_value': The number of tokens to burn.
   - Actions: - Determine whether the balance of the '_address' is more than or equal to the '_value'.
     If true, reduce 'totalSupply' by '_value'.
     - Subtract '_value' from the balance of the '_address'.


## Usage

1. Deploy the 'MyToken' contract to an Ethereum network that supports it.

2. After the contract has been deployed, you can interact with it by invoking the following functions:

   -'mint': Generates fresh tokens and sends them to a given address.
     - Settings:
       - '_address': The location where the tokens will be minted.
       - '_value': The number of tokens to be produced.

   - 'burn': Destroys existing tokens by lowering the total supply and balance of a certain address.
     - Settings:
       - '_address': The location where the tokens will be destroyed.
       - '_value': The number of tokens to burn.



## License

This contract is licensed under the MIT License. SPDX-License-Identifier: MIT.
