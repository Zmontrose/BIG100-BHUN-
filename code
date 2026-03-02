// SPDX-License-Identifier: MIT
pragma solidity ^0.8.24;

/*
 * BIG100 (BHUN)
 * ERC20 Token with:
 * - Custom 32 decimals
 * - Large initial supply
 * - Owner-only minting
 */

import "@openzeppelin/contracts/token/ERC20/ERC20.sol";
import "@openzeppelin/contracts/access/Ownable.sol";

contract BIG100 is ERC20, Ownable {

    uint8 private constant _CUSTOM_DECIMALS = 32;

    /**
     * @dev Constructor mints initial supply to deployer.
     * @param initialSupply The total initial supply (in smallest units).
     */
    constructor(uint256 initialSupply)
        ERC20("BIG100", "BHUN")
        Ownable(msg.sender)
    {
        _mint(msg.sender, initialSupply);
    }

    /**
     * @dev Returns custom decimals (32).
     */
    function decimals() public pure override returns (uint8) {
        return _CUSTOM_DECIMALS;
    }

    /**
     * @dev Owner-only mint function.
     * @param to Recipient address.
     * @param amount Amount to mint (in smallest units).
     */
    function mint(address to, uint256 amount) external onlyOwner {
        _mint(to, amount);
    }
}
