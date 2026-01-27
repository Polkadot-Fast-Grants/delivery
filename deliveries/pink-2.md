# Milestone Delivery 📬

**The delivery is according to the official [milestone delivery guidelines](https://github.com/Polkadot-Fast-Grants/delivery/blob/master/delivery-guidelines.md).**  

* **Application Document:** https://github.com/Polkadot-Fast-Grants/apply/blob/master/applications/pink.md
* **Milestone Number:** 2
* **DOT Payment Address:** 12vNuBb92bDf4WZpEeMcPmQGLhsC4N2hJrMCvjFbq8Sz5Fn9

## Deliverables

| Number | Deliverable | Link | Notes |
| ------------- | ------------- | ------------- |------------- |
| 2a.  | Grid view of owned NFTs |[Relevant files](https://github.com/pinksters/polkagodot-plugin/tree/master/ui/user_assets_grid_view) | Was already present in Milestone 1 | 
| 2b.  | Holographic card display of owned NFTs |[Relevant files](https://github.com/pinksters/polkagodot-plugin/tree/master/ui/nft_showcase_card) | Was already present in Milestone 1 | 
| 2c.  | Server-side verification of ownership |[PolkaGodot Backend](https://github.com/pinksters/polkagodot-backend)| Leaderboard scores include the hat that was equipped by the player during their last score submission | 
| 2d. | Game smart-contract with automated rewards distribution |[RewardsManager contract](https://github.com/pinksters/polkagodot-backend/blob/main/src/contracts/RewardsManager.sol) | Reward distribution for multiplayer matches happens automatically on match submission; Tournament-style reward distribution is triggered with an admin endpoint as it is game-specific. | 
| 2e.  | Full back-end and database for offchain score verification and on-chain score’s submission |[NodeJS backend](https://github.com/pinksters/polkagodot-backend/blob/main/src/server/index.js) | | 


## Quick testing guide

Some of the features of Milestone 2 (grid view, holographic card display, on-chain score submission) were already present and testable in the already-approved [Milestone 1](https://github.com/Polkadot-Fast-Grants/delivery/pull/27).

The main addition in Milestone 2 is the RewardsManager smart contract and automatic reward distribution.

The quickest way to test is through our open-source game - although the game itself is milestone 3, it also happens to be the best way to test the features of Milestone 2:

- https://snek.pinkiverse.pink/

At the top of every hour, the game will distribute rewards to top-10 players on the leaderboard, with bigger rewards for higher ranks.

An example reward distribution transaction, which rewarded 7 participants with diminishing rewards, from 1 PAS for the 1st place to 0.4 PAS for the 7th place:
- https://blockscout-passet-hub.parity-testnet.parity.io/tx/0x496d49e185f740f7b129ce6ae91a3fdab1d74cefa50a80b36e57e52b96cb0dc4

Your equipped hat will be worn by the snake during gameplay, while other players' equipped hats will be displayed on their avatar on the leaderboard.

If you need more hats (e.g. to test with more accounts), you can still mint them at https://polkagodot-demo.pinkiverse.pink .


## Full testing from scratch

If complete manual testing is desired, follow the README to set up your own instance of the game: https://github.com/pinksters/snek

