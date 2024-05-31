## myToken Contract

This is a basic Ethereum blockchain token contract. Functions for minting fresh tokens and burning old ones are provided by the contract.

## Contract Details

• Token Name:VILLALINO

• Token Abbvreviation:CLAR

• Total Supply:0

# Description
This program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. The contract has a functions.

Mint Function: This function raises the recipient address's balance in accordance with a specified increase in the total quantity of tokens.

Burn Function: Lowers the address's balance in accordance with a predetermined reduction in the total number of tokens available. To guarantee that the balance is higher than or equal to the amount to be burned, this function has conditionals.

## Executing program
To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at 
https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., HelloWorld.sol). Copy and paste the following code into the file:

pragma solidity 0.8.18;

contract MyToken {

    // public variables here
string public tokenName = "VILLALINO";
string public tokenAbbrv = "CLAR";
uint public totalSupply = 0;

    // mapping variable here
mapping(address => uint) public balances;

    // mint function
function mint (address _address, uint _value)public {
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

## Authors

NTC STUDENT   
Villalin, Clarens Lerwin S. BSIT 2.1

## License

This project is licensed under the MIT License - see the LICENSE.md file for details
