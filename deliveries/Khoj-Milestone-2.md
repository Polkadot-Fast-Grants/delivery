# Milestone Delivery 📬

**The delivery is according to the official [milestone delivery guidelines](https://github.com/Polkadot-Fast-Grants/delivery/blob/master/delivery-guidelines.md).**  

* **Application Document:** https://github.com/Polkadot-Fast-Grants/apply/pull/61 
* **Milestone Number:** 2
* **DOT Payment Address:** 15oe4E5PbPGM2zqDcEv9d7thAig74MfVF5iax2P7SofFbKac (Polkadot Asset Hub)

**Context** (optional)

The main aim of this milestone was to add more features after the milestone 1 that add to the overall experience of the game fix pending issues. Detailed deliverables are listed in the application as well as in the next section here.

- Latest version of the application is **deployed live** on [playkhoj.com](https://playkhoj.com/).
- Also made a cool vlog style demo video! [Check it out here! 😉](https://youtu.be/98OJuvBur6s?si=Xdwb0zwuzRNJnvDh).



Some important considerations:
1. We have currently deployed it on Moonbase Alpha due to two reasons:
  i. Our team joining [logic](https://github.com/mittal-parth/Khoj/blob/main/contracts/src/Khoj.sol#L248-L286) requires the [ecrecover](https://github.com/mittal-parth/Khoj/blob/main/contracts/src/Khoj.sol#L242) precomplile. As noted in our first milestone, we are yet to solve this.
2. Moonbase Alpha Dev tokens can be obtained from [here](https://faucet.moonbeam.network/ ).
3. We offer some number of retries for solving a clue. It is configurable and currently set to 6. However, this number resets if the user goes back to the hunts page and resumes the game. It is a [known issue](https://github.com/mittal-parth/Khoj/issues/162) which we working on via [this PR](https://github.com/mittal-parth/Khoj/pull/163).
4. We had initially proposed to work on Reward Distribution	as the 7th deliverable in the application. However, we realised that having a leaderboard was more important. The system powering the leaderboard using attestations, was required even for storing clue progress across team members and accurate reward dsistribution. Rewards for now, can also be physical swags and we'll work on this later. This milestone, therefore delivers the leaderboard instead of reward distribution.

Instructions to test are mentioned below. We would love to hear any feedback!


**Deliverables**

| Number | Deliverable | Link | Notes |
| ------------- | ------------- | ------------- |------------- |
| 0a. | License |[61c246fa3e04707be1c3c7a423677dc39d8cc85a](https://github.com/mittal-parth/Khoj/commit/61c246fa3e04707be1c3c7a423677dc39d8cc85a)| | 
| 0b. | Documentation | [Khoj/wiki](https://github.com/mittal-parth/Khoj/wiki), [Readme](https://github.com/mittal-parth/Khoj/blob/main/README.md) | All the relevant documentation is available in the Khoj Wiki and [Readme](https://github.com/mittal-parth/Khoj/blob/main/README.md). | 
| 0c. | Testing and Testing Guide | [Product Guide](https://github.com/mittal-parth/Khoj/wiki/Product-Guide) | | 
| 0d. | Article | TBD |  | 
| 6.  | Team gated huddles | [d1a9045fb11d66b48aeb612a499addcd9beb7e73](https://github.com/mittal-parth/Khoj/commit/d1a9045fb11d66b48aeb612a499addcd9beb7e73) | We aren't using Huddle's NFT based gating but rather a simple backend solution to store the rooms so that team members join the same room. [PR](https://github.com/mittal-parth/Khoj/pull/134) | 
| 7.  | Reward Distribution	-> Leaderboard |[62d39f6b262df41a707c44710d7264621a70337a](https://github.com/mittal-parth/Khoj/commit/62d39f6b262df41a707c44710d7264621a70337a)| The leaderboard is powered by Sign Protocol Attestations. We were initially using TrueNetwork attestations but opted for Sign as we needed conditional querying of attestations, currently not available with TrueNetwork. These attestations also power the clue sync logic, and the score generation for reward distribution. This took a major chunk of our efforts involving the design of a good system and implementing it across. More details in [this PR](https://github.com/mittal-parth/Khoj/pull/120). | 
| 8.  | Treasure Hunt Creation Interface | [44e2848e03094f45c61da3ad29bc46f37db887c9](https://github.com/mittal-parth/Khoj/commit/44e2848e03094f45c61da3ad29bc46f37db887c9#diff-221dedf6cc861aeac0bc217b46a260025e80014e889323f66d79a0841e513eb9) | This was done in the milestone 1 itself since we needed a good way to create and test hunts ourselves. There have been no changes since then. | 
| 9.  | Unit Tests |[8cf9f9fc774ee72e8590ea0e7451912be0055247](https://github.com/mittal-parth/Khoj/commit/8cf9f9fc774ee72e8590ea0e7451912be0055247), [55d562792be0761930803181e2e51748872d0284](https://github.com/mittal-parth/Khoj/commit/55d562792be0761930803181e2e51748872d0284) | Extensive tests covering the smart contract and important baceknd logic like the leaderboard and Sign Protocol usage. | 
| 10. | Documentation | [Khoj/wiki](https://github.com/mittal-parth/Khoj/wiki), [Readme](https://github.com/mittal-parth/Khoj/blob/main/README.md) | Same as 0b. The diagram and the readme have been updated, made cleaner and easier to follow. [Commits](https://github.com/mittal-parth/Khoj/commits/main/README.md) | 
| 11. | UI Revamp | [PR 146](https://github.com/mittal-parth/Khoj/pull/146) | Although not part of the initial deliverables, we decided to give the UI a complete overhaul using the [neobrutalism](https://www.neobrutalism.dev/) styling, giving a more modern, consistent and professional finish. | 


**Additional Information**

Contract addresses:
- KhojNFT: [0x871e2B166a306f4657EbC842b52E8C2806cAa745](https://moonbase.moonscan.io/address/0x871e2B166a306f4657EbC842b52E8C2806cAa745#internaltx)
- Khoj: [0x9E7f33158e59FE51F7122EeD44542d2ef3320625](https://moonbase.moonscan.io/address/0x9E7f33158e59FE51F7122EeD44542d2ef3320625)
