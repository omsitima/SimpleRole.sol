# SimpleRole.sol
How to deploy a contract on Base Chain SimpleRole.sol
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.20;

contract SimpleRole {
    address public admin;

    constructor() {
        admin = msg.sender;
    }

    function setAdmin(address _newAdmin) public {
        require(msg.sender == admin, "Not admin");
        admin = _newAdmin;
    }
}
