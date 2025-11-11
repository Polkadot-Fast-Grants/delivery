# Milestone Delivery 📬

> ⚡ Only the GitHub account that submitted the application is allowed to submit milestones. 
> 
> Don't remove any of the mandatory parts presented in bold letters or as headlines! Lines starting with `>`, such as this one, can be removed.

**The delivery is according to the official [milestone delivery guidelines](https://github.com/Polkadot-Fast-Grants/delivery/blob/master/delivery-guidelines.md).**  

* **Application Document:** https://github.com/Polkadot-Fast-Grants/apply/blob/master/applications/DotStriker!.md
* **Milestone Number:** 1
* **DOT Payment Address:** 16a2oZfA15Pj24mBrMdCD8bWdNvqB47xND3Z7TkDPywvhVZq

**Context** (optional)
In this milestone, we attempted to build out the gameplay from our proof of concept. We also did a play test with some members of the Polkadot community to see whattheir feedback was on a project of this scale. 

**Deliverables**
> Please provide a list of all deliverables of the milestone extracted from the initial application and a link to the deliverable itself. Ideally all links inside the below table should include a commit hash, which will be used for testing. If you don't provide a commit hash, we will work off the default branch of your repository. Thus, if you plan on continuing work after delivery, we suggest you create a separate branch for either the delivery or your continuing work.
> 
> Remember that milestone payments are capped at $5,000 USD and must be delivered within 3 months of approval.
> 
> If there is anything particular about any of the deliverables we or a future reader should know, use the respective `Notes` column.

| Number | Deliverable | Link | Notes |
| ------------- | ------------- | ------------- |------------- |
| 0a. | License |...| MIT| 
| 0b.  | Documentation | https://github.com/rio900/on-chain-game/blob/main/README.md?plain=1#L184-246 | We will provide both **inline documentation** of the Substrate pallet and client, along with a **setup guide** explaining mechanics and instructions to run local tests.                                 | 
| 0c.  | Testing and Testing Guide | https://github.com/rio900/on-chain-game/blob/main/README.md?plain=1#L282-290 | Testing will be conducted through a local in-person playtest (5–10 players). Feedback will be gathered on clarity, engagement, and replayability to guide future design.                              | 
| 0d.  | Article | https://oyonika.medium.com/dotstriker-building-a-fully-on-chain-multiplayer-space-game-on-polkadot-737b9c0ecb8e | We will publish an **article** summarizing what was built, how the mechanics work, and insights from player feedback during the live session. | 
| 1.  | Core Pallet Logic | https://github.com/rio900/on-chain-game/blob/main/pallets/template/src/lib.rs | A working Substrate pallet implementing:<br>• Resource spawning using `on_initialize`<br>• Energy-based ship movement<br>• Per-player resource tracking                               | 
| 2.  | Client Prototype  | https://github.com/rio900/on-chain-game/ | A basic Android and iOS client for real-time gameplay. Client reflects movement, fuel usage, and coin collection in sync with the chain state.                               | 
| 3.  | NFT Simulation & Feedback  | https://github.com/rio900/on-chain-game/tree/feature/resource-spawn | NFT drop logic based on number of active players. All players receive a basic simulated NFT; higher player counts increase rare drop chances. NFTs are not minted or tradable. Includes a live test event (e.g., Polkadot Hub Toronto) with real user feedback.                               | 

**Additional Information**
NOTE: Most of the commits were not made based on the milestone steps, so they may appear a little haphazard. So we have done our best to identify the specific files where the relevant code can be found. Most of the information should be present in the README, but feel free to reach out in case you face any issues!
