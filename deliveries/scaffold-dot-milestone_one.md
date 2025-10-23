# Milestone Delivery 📬

**The delivery is according to the official [milestone delivery guidelines](https://github.com/Polkadot-Fast-Grants/delivery/blob/master/delivery-guidelines.md).**  

* **Application Document:** [scaffold-dot application](https://github.com/Polkadot-Fast-Grants/apply/tree/master/applications/scaffold-dot.md)
* **Milestone Number:** 1
* **DOT Payment Address:** 131RHY6iCnd9KrXuwXr7Pyo6dWP3k3rY9UcEqkG1eB9Uk9HJ

**Context** (optional)
The first milestone forked scaffold-eth2 and modified configuration to support the dot-sama ecosystem. Major configurations implemented and yarn workspace commands updated to provide zero config dev environment.

**Deliverables**

- Forked scaffold-eth2 into public scaffold-dot organization and repository
- Updated readme for developer documentation and guidance to use toolkit
- Added packages for hardhat-polkadot, resolc support
- Configuration to support the dot-sama ecosystem chains including local chain
- Automate downloading the appropriate prebuilt node and eth-rpc binaries for Linux and Mac users
- Updates throughout code to use substrate pre funded accounts, required to retain burner wallet and local faucet functionality for good DX. Updates to deployment scripts to support hardhat-ignition
- Some debugging of pre-built binaries and bug reports while integrating and testing.
- Made most of the updates to UI, but not claiming that milestone yet.

| Number | Deliverable | Link | Notes |
| ------------- | ------------- | ------------- |------------- |
| 0a. | License | Inherited open source licensing from scaffold-eth2
| 0b. | Documentation | Inherited inline documentation and added new inline documentation for all updates and new code. README provides guide to get started and link to deeper scaffold-eth documentation. 
| 0c. | Testing and Testing Guide | Repository includes default smart contract, deployment script, and test script of smart contract. Readme provides guide and scripts for getting started. 
| 0d. | Article | https://medium.com/@gotnoshoeson/scaffold-dot-bringing-ethereums-best-developer-toolkit-to-polkadot-364bc53ea0bc 
| 1.  | MVP | Forked the scaffold-eth 2 repository and configured hardhat with hardhat-polkadot, hardhat-polkadot-node and resolc. Added post install script to download latest node and eth-rpc binaries. [Open source repo](https://github.com/scaffold-dot/scaffold-dot)is available now under the scaffold-dot organization. run and deploy to local chain, deploy to Paseo Passet Hub with zero configuration, and test the dapp with the frontend that is generated from the contract ABI. Toolkit is capable of deploying to Polkadot and Kusama Hub when they're publicly available. There are many hooks and components that are also provided for frontend development. 

**Additional Information**
After lots of testing, I have submitted a bug report for the eth-rpc and node having issues with gas estimation which causes transaction failures.
