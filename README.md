# ETH-AVAX-Module-3
# Create and Mint Token

## Description

For this project, you will write a smart contract to create your own ERC20 token and deploy it using HardHat or Remix. Once deployed, you should be able to interact with it for your walk-through video. From your chosen tool, the contract owner should be able to mint tokens to a provided address and any user should be able to burn and transfer tokens.

## Getting Started

### State Variables

- name: The name of the token, set to "Pratap".
- symbol: The symbol of the token, set to "PRO".
- totalSupply: The total supply of tokens, initialized to 10^11.
- owner: The address of the contract owner, set to the address that deploys the contract.
- balanceOf: A mapping that keeps track of the token balance of each address.

### Constructor

The constructor initializes the contract state. It assigns the total supply of tokens to the contract owner's balance when the contract is deployed.

### Modifiers

onlyOwner: A modifier that restricts access to certain functions to only the contract owner. It checks if the sender (msg.sender) is the owner, and if not, it reverts the transaction with an error message.


## Functions
### Transfer Function

- Allows any user to transfer tokens to another address.
- Checks that the recipient address is not the zero address and that the sender has sufficient balance.
- Updates the balances accordingly and returns true upon success.


### Burn Function

- Allows any user to burn their tokens.
- Checks that the sender has sufficient balance.
- Decreases the sender's balance and the total supply of tokens accordingly and returns true upon success.


### Mint Function

- Allows the owner to mint new tokens.
- Increases the balance of the specified address and the total supply of tokens.
- Contains a logical error: it should check the owner before increasing the balance and total supply. As written, it reverts the transaction if _to is not the owner, but this check should be performed before modifying the balances and supply.

## Working
Working and deployment of the code is shown in the video.

## Authors

Pratap Singh  
[@pratapsingh24](https://github.com/pratapsingh24/ETH-AVAX-Module-3)


## License
This project is licensed under the MIT License - see the LICENSE.md file for details
