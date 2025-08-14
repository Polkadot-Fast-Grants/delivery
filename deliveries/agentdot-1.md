# Milestone Delivery 📬

**The delivery is according to the official [milestone delivery guidelines](https://github.com/Polkadot-Fast-Grants/delivery/blob/master/delivery-guidelines.md).**

* **Application Document:** https://github.com/Polkadot-Fast-Grants/apply/blob/master/applications/AgentDot.md.
* **Milestone Number:** 1
* **DOT Payment Address:** 14XNJmoUzkvmh9cYoqG4axBRR4BWzWRbnFP79oiZgKu7V9bz

**Context**
The deliverables of this milestone allows the users of AgentDOT to translate prompts written in plain English specifically constrained to achieve the following:

 1. Balance Transfers(**Natural Language to transfer Parser**)
   * Keep Alive balance transfers
 2. Teleporting (**Natural Language to XCM Parser**)
  * Teleport DOT, PAS, WND from their relay chains to System chains and back.
 3. Reserve backed asset transfer(**Natural Language to XCM Parser**)
  * transfer assets like USDT and USDC from Polkadot Assethub to Moonbeam and Hydration.
 4. Staking(**Natural Language to Staking Parser**)
  * bond tokens
  * Fetch the list of nominators to validate and the nominate them.
  * unbond tokens
 5. Nominations Pools
  * join a pool.
  * bond extra tokens
  * unbond tokens.
 6. **Wallet connector and extrinsic broadcaster**
  * This allows the application to install and connect signers like Polkadot.js extension and wallets like Talisman SubWallet etc. Once the user approves and provides the signature the transaction is submitted to the node. Its a bridge between the UI and the network ensuring parsed prompts are executed.

**Deliverables**

| Number | Deliverable | Link | Notes |
| ------------- | ------------- | ------------- |------------- |
| 1a. | Natural Language to Transfer Parser |feature/polkadot-ai-agent|Kindly test on the feature/polkadot-ai-agent branch|
| 1b.  | Natural Language to Staking Parser |feature/polkadot-ai-agent|Kindly test on the feature/polkadot-ai-agent branch|
| 1c.  | Natural Language to XCM Parser |feature/polkadot-ai-agent|Kindly test on the feature/polkadot-ai-agent branch|
| 1d.  | Wallet connector and extrinsic broadcaster |feature/polkadot-ai-agent|Kindly test on the feature/polkadot-ai-agent branch |

**Additional Information**

We have worked on Milestone 2a which is to build a Next.js-based interface to make it possible to test the Milestone 1.
Live deployment: https://agent-dot.vercel.app/
