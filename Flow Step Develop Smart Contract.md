### 1. Planning
Before start code, explain what the requirement for contract, like
- What main function/feature for smart contract? (e.g., Token, Voting, Marketplace, etc)
- Who will use it?
- What condition, limitations and permission that needs to be implements

**Pro Tips**:
- Write simple user stories for each feature
- if can, split feature into module. let it be scalable

### 2. Setup Environment
- Use hardhat or Foundry

### 3. Develop Smart Contract
Write smart contract with modular and DRY principle, for example create ERC20 token:
```solidity
// SPDX-License-Identifier: MIT

pragma solidity ^0.8.24

import "@openzeppelin/contracts/token/ERC20/ERC20.sol";

contract MyToken is ERC20 {
	constructor() ERC20("MyToken", "MTK")
}
```