# Token-Deploy-ERC20
Solidity contract for deploying fungible tokens on Ethereum, BSC, Polygon, and other EVM chains
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

import "@openzeppelin/contracts/token/ERC20/ERC20.sol";
import "@openzeppelin/contracts/access/Ownable.sol";

contract MyToken is ERC20, Ownable {
    constructor(string memory name, string memory symbol, uint256 initialSupply) ERC20(name, symbol) {
        _mint(msg.sender, initialSupply * 10 ** decimals());
    }

    // Fungsi tambahan bisa ditambahkan di sini
}
