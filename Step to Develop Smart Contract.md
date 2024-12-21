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
	constructor() ERC20("MyToken", "MTK") {
		_mint(msg.sender, 1000 * 100 ** decimals());
	}
}
```

**Pro TIps**:
- Use openzeppelin for standard feature(e.g., ERC20, AccessControl)
- Add modifier to check permission or limitations

### 4. Testing
Before deploy, always test your contract
- Use framework like **Mocha** and **Chai** in Hardhat
- Write unit test for all important function, include edge case

Example simple test file for `MyToken`/`MyToken.test.js` :
```js
const { expect } = require("chai");

describe("MyToken", function () {
  it("Should mint initial supply to owner", async function () {
    const [owner] = await ethers.getSigners();
    const MyToken = await ethers.getContractFactory("MyToken");
    const token = await MyToken.deploy();
    await token.deployed();

    expect(await token.balanceOf(owner.address)).to.equal(
      ethers.utils.parseUnits("1000", 18)
    );
  });
});
```

Run testing:
```bash
npx hardhat test
```


### 5. Deploy to Testnet
Setup network config on Hardhat, and then deploy to network/chain like **Goerli** or **Sepolia**.

```js
require("@nomiclabs/hardhat-ethers");

module.exports = {
  networks: {
    sepolia: {
      url: "https://eth-sepolia.alchemyapi.io/v2/YOUR_ALCHEMY_API_KEY",
      accounts: [`0x${YOUR_PRIVATE_KEY}`],
    },
  },
  solidity: "0.8.0",
};
```

Script deploy `deploy.js`:
