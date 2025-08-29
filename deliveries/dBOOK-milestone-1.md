# dBOOK – Milestone Delivery 1

> The delivery is according to the official [milestone delivery guidelines](https://github.com/Polkadot-Fast-Grants/delivery/blob/master/delivery-guidelines.md).

- **Name of the grant project:** dBOOK – AI-powered Intelligence Engine for Wallets  
- **Application Document:** [dBOOK Application](https://github.com/Polkadot-Fast-Grants/apply/blob/master/applications/dBOOK.md)  
- **Milestone Number:** 1  
- **DOT Payment Address:** `15a1c6oA9Ue7VHMbEhptbQCqFf9iKq3qEhqARqD377ezveTb` 
  > We kindly request that the grant funds be transferred using our **live MVP on Polkadot**, as this would serve as a real-world demonstration of the product in action.  

---

## 📌 Context

This milestone delivers the first step towards **dBOOK’s conversational intent-to-execution layer** for Polkadot.  
It demonstrates how users can:

- Query on-chain statistics via plain-language chat, and  
- Execute native asset transfers on Polkadot parachains.  

### ❗ Note on Deliverable 1a
The originally proposed **Intent Pallet** was **not implemented**.  
Through development we determined that a dedicated pallet does not add value at this stage.  
Intents are currently better represented through **schema mapping + off-chain resolution**, with parachain integration to be revisited in later milestones.  

Instead, we focused on strengthening **1b** and **1c** to provide a working foundation for **intent parsing** and **execution flows**.

---

## ✅ Pre-Deliverables

| Number | Deliverable | Link | Notes |
|--------|-------------|------|-------|
| 0.a | License | [Frontend LICENSE](https://github.com/dbooklabs/polkadot_frontend/blob/main/LICENSE.md) · [MCP LICENSE](https://github.com/dbooklabs/polkadot_mcp/blob/main/LICENSE) | MIT |
| 0.b | Documentation | [Frontend](https://github.com/dbooklabs/polkadot_frontend/blob/main/README.md) · [MCP](https://github.com/dbooklabs/polkadot_mcp/blob/main/README.md) | Setup, usage & integration |
| 0.c | Testing Guide | [Testing Website](https://polkadot.nomo.now) |The app can be tested on here |

---

## 🚀 Deliverables

| Number | Deliverable | Link | Notes |
| ------ | ----------- | ---- | ----- |
| 1.a | Intent Pallet | ❌ Not delivered | Re-scoped (see context note above) |
| 1.b | Query On-chain Statistics | [Query Module](https://github.com/dbooklabs/polkadot_mcp/tree/main/src/tools/services) | Supports portfolio balance queries & chain-level analytics (e.g. DOT balance). Demonstrated via chat interface. |
| 1.c | Native Asset Transfer | [Transfer Module](https://github.com/dbooklabs/polkadot_mcp/tree/main/src/tools/transfers) | Supports native transfers across AssetHub, Acala, and Astar. Example: `Send 10 ASTAR to 16B...` → intent parsed → signed via wallet → executed. [Video Demo](https://docsend.com/v/jrb5g/polkadotm1). |

---

### Key Features Delivered
- Natural-language queries like _“What’s my DOT balance?”_ → wallet + chain state.  
- Native DOT transfer flow through conversational UI.  
- Integration with **Polkadot**, **Paseo (Testnet)**, and **Astar** parachains.  
- Full testing and developer documentation.  

---

## 🔮 Next Steps

Milestone 2 will build on this foundation by:  
- Adding **protocol bindings & execution adapters** (swap, lending, staking, bridges).  
- Enabling **advanced analytics** (LP positions, yield earned, protocol-level stats).  

---

## 📢 Disclaimer

Since submitting this grant application, **dBOOK has rebranded to Nomo**.  
The Polkadot-focused intent work continues under this grant, while in parallel we have also launched our **EVM integration live on Berachain**.  

You can follow ongoing updates here:  
- 🌐 [nomo.now](https://nomo.now)  
- 🐦 [x.com/nomoHQ](https://x.com/nomoHQ)  

---

**Team:**  
Angad Singh Agarwal • Harshit Singhal • Gurkaran Sahni  
[Website](https://nomo.now) • [X](https://x.com/nomoHQ)
