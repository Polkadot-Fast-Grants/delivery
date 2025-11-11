# Milestone Delivery 📬

**The delivery is according to the official [milestone delivery guidelines](https://github.com/Polkadot-Fast-Grants/delivery/blob/master/delivery-guidelines.md).**  

* **Application Document:** https://github.com/Polkadot-Fast-Grants/apply/blob/master/applications/pink.md
* **Milestone Number:** 1
* **DOT Payment Address:** 12vNuBb92bDf4WZpEeMcPmQGLhsC4N2hJrMCvjFbq8Sz5Fn9

## Deliverables

| Number | Deliverable | Link | Notes |
| ------------- | ------------- | ------------- |------------- |
| 1a.  | Godot plugin with EVM wallet connectivity and automatic NFTs querying for in-game use |[PolkaGodot plugin](https://github.com/pinksters/polkagodot-plugin)| MIT-Licensed plugin for Godot Engine| 
| 1b.  | In-game list view of owned NFTs |[Relevant files](https://github.com/pinksters/polkagodot-plugin/tree/master/ui/user_assets_list_view)| | 
| 1c.  | Back-end with full database integration accessible through API endpoints |[PolkaGodot Backend](https://github.com/pinksters/polkagodot-backend)| MIT-Licensed NodeJS server + SQLite database | 
| 1d. | NFT contract for wearable cosmetics and equippables |[.sol file](https://github.com/pinksters/polkagodot-backend/blob/main/src/contracts/hat.sol)| MIT license specified within the contract | 
| 1e.  | Game smart-contract with on-chain recording of games played deployed and verified on Paseo (or directly on Polkadot Hub if available at that time) |[.sol file](https://github.com/pinksters/polkagodot-backend/blob/main/src/contracts/GameManager.sol)| MIT license specified within the contract| 


## Quick testing guide

For convenience of testing, a fully set-up minimal demo is available at https://polkagodot-demo.pinkiverse.pink/
You can use the demo to see the PolkaGodot extension in action, mint NFTs, and submit scores on-chain.

The relevant smart contracts are deployed and verified on Paseo:
- https://blockscout-passet-hub.parity-testnet.parity.io/address/0xbE1bf5bfE6D14Cf6c8Cd89e22935725fC366F62a?tab=contract
- https://blockscout-passet-hub.parity-testnet.parity.io/address/0xeA78C032fb2a446140EA692957E6D983f9C6DEfb?tab=contract

The database endpoint will output general stats and recently submitted games:
- https://pinkhat.some-kind-of-server.com:3002/db/info


## Full testing guide (if desired)

### Token metadata setup
1. Create `.json` files with desired token metadata, in `{tokenID}.json` format.
2. Upload the `.json` files to your server.
3. (Optional) Run `metadata-server.js` on your server to support an infinite number of minted tokens with finite metadata files.

### On-chain setup
1. Point the URL in `hat.sol` (line 79) to your metadata server
2. Deploy `hat.sol` first
3. Deploy `GameManager.sol` with the address of the deployed `hat.sol` contract
4. Call `mint()` on HatNFT to mint NFTs for testing

### Backend setup
Run `index.js` on your server or locally - a list of available endpoints will be output to the console.

### In-game setup
1. Follow the setup instructions for the PolkaGodot extension, or use [PolkaGodot minimal template](https://github.com/pinksters/polkagodot-minimal-template) to get started quickly.
2. Create a PolkaConfig file and configure it for your chain and contract addresses
3. Enjoy!


## Additional info / next steps

Milestones 2 and 3 are nearing completion and will be submitted shortly after.

As part of the final milestone (milestone 3), we will deliver and deploy a minimalistic open-source game that demonstrates a practical use of this suite to equip in-game cosmetics.
