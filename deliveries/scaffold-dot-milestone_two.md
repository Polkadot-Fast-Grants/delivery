# Milestone Delivery 📬

**The delivery is according to the official [milestone delivery guidelines](https://github.com/Polkadot-Fast-Grants/delivery/blob/master/delivery-guidelines.md).**  

* **Application Document:** [scaffold-dot application](https://github.com/Polkadot-Fast-Grants/apply/tree/master/applications/scaffold-dot.md)
* **Milestone Number:** 2
* **DOT Payment Address:** 131RHY6iCnd9KrXuwXr7Pyo6dWP3k3rY9UcEqkG1eB9Uk9HJ

**Context** (optional)
The second milestone is a UI/UX scope of work. Includes 4 wallet providers with web2/social login AND browser extension wallets. Easy to configure out of the box. Quick access to PassetHub faucet.

**Deliverables**

- Add wallet providers: RainbowKit - original provider, Reown AppKit - rebranded WalletConnect, Privy - by stripe, Web3Auth - by MetaMask
- Add configuration logic for easy implementation of one of the four providers
- Providers support social and web2 embedded wallets AND browser extension wallets such as MetaMask. All inclusive approach 
- Updated readme for developer documentation and guidance to use toolkit
- UI to match Polkadot's branding identity in light mode and dark mode. Polkadot just rebranded their landing page but shouldn't affect scaffold-dot.
- Added Faucet functionality to quickly link to getting PAS tokens for Paseo PassetHub. Faucet button dynamically renders, when clicked, copies currently connected wallet address, opens faucet in new tab and redirects browser to page.

| Number | Deliverable | Link | Notes |
| ------------- | ------------- | ------------- |------------- |
| 0a. | License | Inherited open source licensing from scaffold-eth2
| 0b. | Documentation | Inherited inline documentation and added new inline documentation for all updates and new code. README provides guide to get started and link to deeper scaffold-eth documentation. 
| 0c. | Testing and Testing Guide | Repository includes default smart contract, deployment script, and test script of smart contract. Readme provides guide and scripts for getting started. 
| 0d. | Article | https://medium.com/@gotnoshoeson/scaffold-dot-bringing-ethereums-best-developer-toolkit-to-polkadot-364bc53ea0bc 
| 1.  | MVP | Forked the scaffold-eth 2 repository and configured hardhat with hardhat-polkadot, hardhat-polkadot-node and resolc. Added post install script to download latest node and eth-rpc binaries. [Open source repo](https://github.com/scaffold-dot/scaffold-dot)is available now under the scaffold-dot organization. run and deploy to local chain, deploy to Paseo Passet Hub with zero configuration, and test the dapp with the frontend that is generated from the contract ABI. Toolkit is capable of deploying to Polkadot and Kusama Hub when they're publicly available. There are many hooks and components that are also provided for frontend development. 
| 2.  | UI/UX |  Included 4 wallet providers with web2/social login AND browser extension wallets. Easy to configure out of the box. Integrated quick access to PassetHub faucet. UI updated to feel Polkadot native.

