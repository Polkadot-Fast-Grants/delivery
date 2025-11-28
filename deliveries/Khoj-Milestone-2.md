# Milestone Delivery 📬

**The delivery is according to the official [milestone delivery guidelines](https://github.com/Polkadot-Fast-Grants/delivery/blob/master/delivery-guidelines.md).**  

* **Application Document:** https://github.com/Polkadot-Fast-Grants/apply/pull/61 
* **Milestone Number:** 2
* **DOT Payment Address:** 15oe4E5PbPGM2zqDcEv9d7thAig74MfVF5iax2P7SofFbKac (Polkadot Asset Hub)

**Context**

The main aim of this milestone was on improving the UX, fix issues that were reported in testing, add important features like clue progress sync and security fixes. Detailed deliverables are listed in the application as well as in the next section here.

- **Live 🔗**:  [playkhoj.com](https://playkhoj.com/)
- **Demo Video 📷**: [YouTube](https://youtu.be/98OJuvBur6s?si=Xdwb0zwuzRNJnvDh)
- **Article**: [Khoj-Polkadot-Fast-Grants-Milestone-2-Update](https://github.com/mittal-parth/Khoj/wiki/Khoj-Polkadot-Fast-Grants-Milestone-2-Update)

Feedback from the last milestone:

  1.   Conflicting leaderboard mentioned [here](https://github.com/Polkadot-Fast-Grants/delivery/pull/21#pullrequestreview-3407612518).

       We realised this was a bug due to the attestations not taking the chains into account. Thereby, if the hunt number was the same on two chains, it would honour those existing attestations. We have fixed this in [#171](https://github.com/mittal-parth/Khoj/pull/171)
  3. Passet Hub integration. This is now live with all the features.


**Deliverables**

| Number | Deliverable | Link | Notes |
| ------------- | ------------- | ------------- |------------- |
| 0a. | License |[61c246fa3e04707be1c3c7a423677dc39d8cc85a](https://github.com/mittal-parth/Khoj/commit/61c246fa3e04707be1c3c7a423677dc39d8cc85a)| | 
| 0b. | Documentation | [Khoj/wiki](https://github.com/mittal-parth/Khoj/wiki), [Readme](https://github.com/mittal-parth/Khoj/blob/main/README.md) | All the relevant documentation is available in the Khoj Wiki and [Readme](https://github.com/mittal-parth/Khoj/blob/main/README.md). | 
| 0c. | Testing and Testing Guide | [Product Guide](https://github.com/mittal-parth/Khoj/wiki/Product-Guide) | | 
| 0d. | Article | [Khoj-Polkadot-Fast-Grants-Milestone-2-Update](https://github.com/mittal-parth/Khoj/wiki/Khoj-Polkadot-Fast-Grants-Milestone-2-Update) |  | 
| 6.  | Team gated huddles | [d1a9045fb11d66b48aeb612a499addcd9beb7e73](https://github.com/mittal-parth/Khoj/commit/d1a9045fb11d66b48aeb612a499addcd9beb7e73) | We aren't using Huddle's NFT based gating but rather a simple backend solution to store the rooms so that team members join the same room. [PR](https://github.com/mittal-parth/Khoj/pull/134) | 
| 7.  | Reward Distribution	-> Leaderboard |[62d39f6b262df41a707c44710d7264621a70337a](https://github.com/mittal-parth/Khoj/commit/62d39f6b262df41a707c44710d7264621a70337a)| The leaderboard is powered by Sign Protocol Attestations. We were initially using TrueNetwork attestations but opted for Sign as we needed conditional querying of attestations, currently not available with TrueNetwork. These attestations also power the clue sync logic, and the score generation for reward distribution. This took a major chunk of our efforts involving the design of a good system and implementing it across. More details in [this PR](https://github.com/mittal-parth/Khoj/pull/120). | 
| 8.  | Treasure Hunt Creation Interface | [44e2848e03094f45c61da3ad29bc46f37db887c9](https://github.com/mittal-parth/Khoj/commit/44e2848e03094f45c61da3ad29bc46f37db887c9#diff-221dedf6cc861aeac0bc217b46a260025e80014e889323f66d79a0841e513eb9) | This was done in the milestone 1 itself since we needed a good way to create and test hunts ourselves. There have been no changes since then. | 
| 9.  | Unit Tests |[8cf9f9fc774ee72e8590ea0e7451912be0055247](https://github.com/mittal-parth/Khoj/commit/8cf9f9fc774ee72e8590ea0e7451912be0055247), [55d562792be0761930803181e2e51748872d0284](https://github.com/mittal-parth/Khoj/commit/55d562792be0761930803181e2e51748872d0284) | Extensive tests covering the smart contract and important baceknd logic like the leaderboard and Sign Protocol usage. | 
| 10. | Documentation | [Khoj/wiki](https://github.com/mittal-parth/Khoj/wiki), [Readme](https://github.com/mittal-parth/Khoj/blob/main/README.md) | Same as 0b. The diagram and the readme have been updated, made cleaner and easier to follow. [Commits](https://github.com/mittal-parth/Khoj/commits/main/README.md) | 
| 11. | UI Revamp | [PR 146](https://github.com/mittal-parth/Khoj/pull/146) | Although not part of the initial deliverables, we decided to give the UI a complete overhaul using the [neobrutalism](https://www.neobrutalism.dev/) styling, giving a more modern, consistent and professional finish. |


**Additional Information**

Contract addresses on PassetHub:
- KhojNFT: [0x3F7A5D9e2879530F7809282A26CaB68A35F574Cd](https://blockscout-passet-hub.parity-testnet.parity.io/address/0x3F7A5D9e2879530F7809282A26CaB68A35F574Cd)
- Khoj: [0x3bCE432154aC26E8A6B0bFFE1AA3c0AAE0BE0d6C](https://blockscout-passet-hub.parity-testnet.parity.io/address/0x3bCE432154aC26E8A6B0bFFE1AA3c0AAE0BE0d6C)
